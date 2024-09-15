# maize_task
Contains the code implementation of the coding question


# Simple Entity and Legal Reference Extractor for Italian Constitution (Beginner Version)

This is a very basic program to find some entities (like "Governo" and "Parlamento") and legal references (like "l. cost. 17 giugni 1947, n.2") in the text of the Italian Constitution PDF.

## How It Works

1. **Reads the PDF**: The program uses `PyPDF2` to extract text from the PDF file.
2. **Finds Entities**: It looks for specific words, like "Presidente della Repubblica" or "Regione", in the text and records where they appear.
3. **Finds Legal References**: It uses a very simple regular expression to match legal references like "l. cost. DD Month YYYY, n.X".
4. **Outputs the Results**: It saves the results in a file called `output.json`.

### What the Output Looks Like

The output is saved in a JSON file. Here's what an example output looks like:

```json
{
    "entities": [
        {
            "label": "Presidente della Repubblica",
            "span_start": 12345,
            "span_end": 12370
        }
    ],
    "legal_references": [
        {
            "reference": "l. cost. 17 giugni 1947, n.2",
            "span_start": 54321,
            "span_end": 54345
        }
    ]
}

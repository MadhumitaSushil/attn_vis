# Importance Visualizer

This is a tool to visualize the distribution of importance scores over timesteps (example words) in a sequence classification task. As you hover your mouse over the decoded words, the tool shows a heatmap of importance scores over the source words.

## To run

To run the visualizer, run
```
python -m SimpleHTTPServer
```
from this directory then navigate to `http://localhost:8000/` in browser. The visualizer will show some example data.

## To use your own data

To visualize your own data, you need to replace `imp_scores_test.json` with a similar file which provides the importance scores over the sequences, the sequences themselves, and the gold and the predicted labels. In particular `imp_scores_test.json` should contain the following fields:

*  `seq_lst`: multiple sequences as a list of list of words.
*  `imp_scores`: the importance scores of every word for every sequence. List of list.
*  `pred`: List of predicted labels for every sequence
*  `gold`: List of gold labels for every sequence


WARNING: Make sure that none of the strings in `seq_lst`, `imp_scores`, `pred` or `gold` contain `<angled brackets>`. These will interfere with the HTML and can result in text not being displayed.

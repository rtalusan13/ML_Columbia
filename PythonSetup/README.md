# Python Setup

1. Install Anaconda https://www.anaconda.com/products/individualLinks to an external site.. Anaconda comes with all of our required packages (and a lot more) and hence takes much more storage space.
2. Launch a terminal with the conda virtual environment (Windows: search “Anaconda Powershell” in start menu; Mac OS: just start a terminal and you should see “(base)” before your username, if not, try the command source activate conda). Make sure you see something similar to this when you run the command conda list:


3. If you installed Anaconda, NumPy and Scikit-Learn should both be installed. To install any other packages enter the following command
        conda install -c conda-forge scikit-learn.
4. Download the notebook (i.e., the .ipynb file) from
https://scikit-learn.org/stable/auto_examples/linear_model/plot_poisson_regression_non_normal_loss.htmlLinks to an external site..
You do not need to know what this example does.
5. Open the notebook using the command
       jupyter notebook ../your/path/to/plot poisson regression non normal loss.ipynb.
6. Try to run the notebook. Install any missing package(s) (maybe none, maybe Pandas). It can be installed similarly - just Google “conda install pandas” if you are not sure. Run the entire notebook and keep the outputs.

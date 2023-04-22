## Instructions how to use PDF_Report_Generator_for_Finnhub:

1) Get a free API key from Finnhub. Refer to my other repository https://github.com/dvasser/Finnhub-API-Connector for more details.
2) Clone this repository, open an IDE and navigate to the directory with the files. Pip install -r requirements.txt
3) You are now ready to generate the report! Simply run the finn_pdf_generator.py file in the command line or by pressing 'run'. You will be prompted to input your Finnhub API key, a list of stocks separated by commas (could just enter one stock), start and end dates (I recommend for them to be at least 6 months apart), the DPI (100 is a good value to see how the report looks like, 300 generates a high quality report but takes a while. 500 is super sharp, and could take hours).

Additional notes: How the program works - makes API calls using the API connector in this repo and your personal API key. All the data frames created from making these calls will be within the given date range. It then plots all the data using MatPlotLib and takes screenshots while neatly formatting for better visualization, saves to the current directory. After that it creates an empty PDF report and uploads all the screenshots one by one (you will be able to track the logs once the program is running). DPI is the quality with which the screenshots are uploaded to the report. Read through the code comments in finn_pdf_generator.py for more details on how the code works. Also feel free to play around with the formatting (there is a link to MatplotLib colors on line #584). You will also find two attached PDF reports in this repo that I generated earlier for display. Also, as of right now there is a glitch in the Finnhub API which messes up the data for ev - Embedded Value of stocks and makes the graph look quite bizarre. I wrote them an email, hopefully they'll be able to fix it soon since the glitch wasn't there a few days prior. Enjoy your research!

## Identification
The identification stage is where we test queries against databases to develop a corpus of relevant studies 

### Executing Search
1. Execute query in database using agreed upon limiters (date, type of publication, language, etc)
2. Export results with abstract - it is best to do this as a CSV
3. Load the CSV into Sheets
4. Add a variable that is "source" and add the database name
5. Name the sheet after the databases
6. Create a new sheet and repeat for all databases that will be used in the review

### Cleaning Data
Each database will likely export data in a different structure
[ Need to discuss how to clean the data ]

## Screening & Eligibility 

### Screening
The initial screening stage is a simple binary decision about relevance based on inclusion / exclusion criteria. The decision is based on a quick reading of each paper's abstract.
Screening should eliminate many false positives from the Identification stage.

For screening we are going to use an interface that can speed up the process for reading abstracts (and it has some built in AI assistance we could use in the future)

Steps for downloading and using `ASReview`
1. Make sure you have Python version 3.6 or higher installed
2. Start python
3. Run `pip install asreview`
4. Run `asreview lab`
5. A browser should open with the ASReview interface. If not check what port is running - it will look something like this:

```
> nmweber@is-nmweberm14x ~ % asreview lab
> Port 5000 is in use.
> * Trying to start at 5001
> Start browser at http://localhost:5001/
```

6. Open a browser and go to `http://localhost:5000/projects`

🎉 - ASReview is running on your local machine!

Using ASReview to screen papers
1. Create a new project
2. Under "Project Information" be sure to select the mode `Oracle`
3. Add a dataset (e.g. your assigned CSV)
4. The oracle mode will ask you to label 1 relevant and irrelevant paper (tip: Select random in the prior knowledge screen to select papers. You only have to do 1 of each label before closing the window)
5. Model - Leave these settings the same
6. After hitting next you should see a link at the bottom that says "start reviewing"
6. Reviewing is dead simple - just choose relevant or irrelevant for each paper's abstract. If you aren't sure add note "maybe" and chose Relevant
7. ☕️ - Screen away
7. When you're finished screening - you can export your dataset as a csv and deposit in dropbox

A few tips:
- ASReview is local to your machine. As long as you don't move any of its configuration and log files you can start and end a session whenver you want. All of your screening should be saved.
- The anaytics page is helpful to see progress

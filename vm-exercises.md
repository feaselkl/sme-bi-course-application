# Virtual Machine (VM) Exercises

## 1st VM Exercise

#### Dataset

- [x] Add datasets used to the `datasets/` folder

#### Files

- [x] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.twbx` or `ex-1-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [x] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix`

#### Learning Objective

*One measurable learning objective that this exercise assesses*

Create a variant on a date dimension:  a year table.

#### Motivation

*3 - 4 sentence description of why it’s important to learn how to do this task (linking back to the learning objective). Explain how this would be used in a real-life situation. Why is it useful, what problem does it solve?*

Date and time tables are common in data analysis because they simplify date calculations.  Facts are almost always time-sensitive, as we generally care about when the fact was recorded and over what time period the fact was valid.  Date and time tables allow us to slice data with ease and consistency:  every report can use the same calculations for fiscal year and we won't need to calculate what day Easter fell on in a given year if we include these attributes in a date table.

#### Steps to be executed by the student (max 6)

*Each bulleted instruction is a complete sentence that describes a specific task.*

- In the *Data* view, navigate to the `Year` table.
- Use the `Table tools` menu to add a new column called `Decade`, which will represent the decade associated with a given year.  Use the first year of the decade as the identifier, so that, for example, 1978 is in the decade 1970.
- Add another new column called `Century`, which will represent the century associated with a given year.  Use the first year of the century as the identifier.  For the sake of simplicity, assume that 1900 and 2000 are the first years of the 20th and 21st centuries, respectively.
- In the *Report* view, select the **Number of establishments** visual and add `Decade` to the Axis.
- Find the decade with the largest number of establishments with ages between 6-10 years old.  Provide the number of such establishments.

#### End goal:

*Add an image of the final visualization here.*

![The number of establishments by decade with an age in the 6-10 years range.](Exercise1EndGoal.jpg)

## 2nd VM Exercise

#### Dataset

- [x] Add datasets used to the `datasets/` folder

#### Files

- [x] **Initial**: Add file to the `exercises/`  folder with the name `ex-2-intial.twbx` or `ex-2-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [x] **Solution**: Add file to the `exercises/`  folder with the name `ex-2-sol.twbx` or `ex-2-sol.pbix`

#### Learning Objective

*One measurable learning objective that this exercise assesses*

Define relationships between tables, including composite key relationships.

#### Motivation

*3 - 4 sentence description of why it’s important to learn how to do this task (linking back to the learning objective). Explain how this would be used in a real-life situation. Why is it useful, what problem does it solve?*

Defining relationships is critical in Power BI for several reasons.  Data models with well-defined relationships allow for cross-table filtering and slicing while maximizing performance.  Because data in Power BI may come from a variety of sources, we sometimes need to reshape or redefine the key columns used to form these relationships.

#### Steps to be executed by the student (max 6)

*Each bulleted instruction is a complete sentence that describes a specific task.*

- In the *Data* view, select **Get data** and choose **Text/CSV**.
- Import the **Establishments By State.txt** file.  Select **Transform Data** to open the Power Query Editor.
- Remove the **Changed Type** applied step.  Merge together the Geography columns into a new column called `GEOID`.  Change the `Employment size of establishments code`, `Year`, and `Number of establishments` columns' types to **Whole Number**.
- In the *Relationships* view, create relationships between `Establishments by State` and `Geography` as well as `Year`.
- In the *Report* view, create a new page called `Establishments by State` and include a visual which answers the following question:  How many manufacturing establishments were there in the state of Ohio which operated with 50-99 employees?

#### End goal:

*Add an image of the final visualization here.*

![The number of manufacturing establishments in the state of Ohio which operated with 50-99 employees.](Exercise2EndGoal.jpg)
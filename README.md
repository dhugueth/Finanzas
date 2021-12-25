# Personal Finance 

To access the report [click here](https://app.powerbi.com/view?r=eyJrIjoiMDUzMDY5ZTAtYmE4Zi00MTRlLWI3NTMtNDAyOTIxOWEwOGMzIiwidCI6ImJhYjBiNjc5LWJkNWYtNGZlOC1iNTE2LWM2YjhiMzE3Yzc4MiIsImMiOjR9&pageName=ReportSection)

## What was used? 

The project was developed and published using Power BI, one of the top leader in business Intelligence.

### Data

_The data used was provided for educational purposes by Power BI - Data Analysis and Business Intelligence course on the Udemy platform._

- [Finanzas-Final.xlsx](https://github.com/dhugueth/Finanzas/files/7746845/Finanzas-Final.xlsx)
- [Categorias.xlsx](https://github.com/dhugueth/Finanzas/files/7746854/Categorias.xlsx)
- [Calendario2019.xlsx](https://github.com/dhugueth/Finanzas/files/7746849/Calendario2019.xlsx)
- [Calendario2020.xlsx](https://github.com/dhugueth/Finanzas/files/7746850/Calendario2020.xlsx)

Some pre-established background pictures given in the course was used. 

### Data Preparation

Modifications were made to the original data using the Power Query editor to be able to use them appropriately. 

The modifications were: 

- A custom column called *Tipo* was added to the "TablaGastos" table.
- A custom column called *Tipo* was added to the "TablaIngresos" table.
- A new table called *Finanzas* was created appending the information from the tables "TablaGastos" and "TablaIngresos".
- In "TablaMetas" table, the unpivot columns option is used to transform the *Remuneracion* and *Online* columns into other columns, one for category and the other for quantity.
- A custom column called *Tipo* was added to the "TablaMetas" table.
- In "TablaPresupuesto" table, the unpivot columns option is used to transform twenty-five columns into two columns, one for category and the other for quantity.
- A custom column called *Tipo* was added to the "TablaPresupuesto" table.
- A new table called *Expectativas* was created appending the information from the tables "TablaPresupuesto" and "TablaMetas".
- A prefix was added to the column called *Fecha* from table "Expectativas" to establish the data type like date. 
- The year of the dates that appear in the *Fecha* column of the "Calendario" table is exported to a new column. 
- The number of the month of the dates that appear in the *Fecha* column of the "Calendario" table is exported to a new column.  
- The name of the month of the dates that appear in the *Fecha* column of the "Calendario" table is exported to a new column.
- From the column with the name of the month of the "Calendario" table, three characters are extracted and formed a new column. 
- In the *Fecha* column of the "Calendario" table, the data is extracted from a delimiter in a new column.
- A blank table was created called "Cuotas%"
- A blank table called "Categorias" was created and the data found in the excel file categories.xlsx was copied 

## Data Modeling

It was required to relate common data between the files:

- The data named *Fecha* of the "Calendario" and "Expectativas" sheet were related. 
- The data named *Fecha* of the "Calendario" and "Finanzas" sheet were related. 
- The data named *Categoria* of the "Calendario" and "Finanzas" sheet were related. 
- The data named *Categoria* of the "Calendario" and "Expectativas" sheet were related. 

**DAX - Data Analysis Expressions**

- A new measure was created using `SUM` function in "Finanzas" sheet.
- Two new measure was created using `CALCULATE` function in "Finanzas" sheet.
- A new measure was created using `SUM` function in "Expectativas" sheet.
- Two new measure was created using `CALCULATE` function in "Expectativas" sheet.
- A subtraction operation was used to create a new measure in the "Finanzas" sheet called *Utilidad* 
- A subtraction operation was used to create a new measure in the "Expectativas" sheet called *Ut. Esperada*
- A division operation was used to create a new measure in the "Cuotas%" sheet called *Cuota Ingresos*
- A division operation was used to create a new measure in the "Cuotas%" sheet called *Cuota Gastos* 
- A division operation was used to create a new measure in the "Cuotas%" sheet called *Cuota Utilidad* 
- A division operation was used to create a new measure in the "Cuotas%" sheet called *Cuota Saldo* 
- A new column was created using `CALCULATE`, `FILTER`, `ALL` and `MAX` functions in "Finanzas" sheet 
- A new column was created using `CALCULATE`, `FILTER`, `ALL` and `MAX` functions in "Expectativa" sheet 

## Description

For the Personal Finance report different visualizations such as gauge, multi-row card, button, slicer, table, area chart, line chart, clustered column chart, matrix, line ad stacked column chart were used to make the exposed analysis. 

The project had the goal of developing an interactive report on personal finances, which allows visualizing the behavior of some indicators of income, expenses, profit, and balance through the months of 2019 and 2020.  


https://user-images.githubusercontent.com/93662295/147392819-a66ee86f-9989-4794-8050-e27ff65ef147.mp4




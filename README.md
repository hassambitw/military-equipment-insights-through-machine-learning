# military equipment insights through machine learning

To run the notebook, you'll need the appropriate dependencies, and retrieve the dataset from your saved directory. 

The dataset used for this project contains information on surplus military equipment transferred to local law enforcement agencies through the Defense Logistics Agency (DLA). It includes a wide range of items from specialized military gear to common office supplies. The goal was to extract as much useful information as possible. Data was first understood and information such as the state value count, DEMIL (Demilitarization) count, total cost, shipments per year, most common items sold, etc. were plotted and determined.

Next, the data was cleaned where unnecessary columns were removed, null value rows were removed and blank cells were filled with a placeholder value. Outliers were detected and categorical columns were label encoded and feature columns were standardized.

One of the goals was also to predict the DEMIL code. To achieve this, a train/test split of 70/30 was created and a Sequential ANN was used. Multiple models were used with a random number of layers and nodes with differing epochs and batch sizes each time to fine-tune accuracy and loss, which in the end resulted in a predictive accuracy increase from 93% to 98% and a loss rate reduction of 8% from 19%.

Based on the analysis, my recommendation was to increase the shipment of items with DEMIL Code C if generating revenue is the main focus; Mine Resistant Vehicles particularly generate a disproportionate amount of revenue when compared to other items. If generating volume is the main focus, then focus on shipments with DEMIL Code D as they are far more frequently shipped historically. A special case is the Unmanned Vehicle which falls into DEMIL code Q but also generates significant revenue.

# Hotel Booking Cancellation Prediction
## Outline
[Data Background](https://github.com/vinahuang97/final_project_data_science?tab=readme-ov-file#data-background)</br>

[Data Preprocessing and analysis](https://github.com/vinahuang97/final_project_data_science?tab=readme-ov-file#data-preprocessing-and-analysis)</br>
  * [EDA](https://github.com/vinahuang97/final_project_data_science/tree/main#eda)</br>
    - [Where do the guest come from?](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#--where-do-the-guest-come-from)</br>
    - [How much do guests pay for a room per night?](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#--how-much-do-guests-pay-for-a-room-per-night)</br>
    - [how much the price vary over the year?](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#--how-much-the-price-vary-over-the-year)</br>
    - [Which are the busy month ?](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#--which-are-the-busy-month-)</br>
    - [How many booking are cancel?](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#--how-many-booking-are-cancel)</br>
  * [Matrix corellation](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#matrix-correlation)</br>
  
[Machine learning model](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#machine-learning-model)</br>
  * [Baseline model](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#baseline-model)</br>
  * [best model confusion matrix](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#confusion-matrix)</br>
  * [feature importance](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#feature-importance)</br>

[Action & Recomendation](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#action--recommendation)</br>

[Appendix](https://github.com/vinahuang97/final_project_data_science/tree/main?tab=readme-ov-file#appendix)

## Data Background
The data comes from two different hotels. One resort hotel and one city hotel. The two hotels are located in Portugal, namely the Algarve resort hotel and the Lisbon city hotel. the data contains bookings that will arrive between 1 July 2015 and 31 August 2017, including bookings that have effectively arrived and bookings that have been cancelled. The data contains 32 variables and 119.390 hotel reservations.</br>
</br>
There are 24.025 (27.5%) customers who cancel their bookings</br>
</br>
## Data Preprocessing and analysis
### EDA
#### - Where do the guest come from?
![Guest Map](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/map.png)
The guests come from all over the worlds, but most come from Portugal and Europe.</br>
</br>

#### - How much do guests pay for a room per night?
![Guest Pay](https://github.com/vinahuang97/final_project_data_science/raw/main/final%20project%20pic/room%20rate.png)
From the data above we know that the room rate depends on the room type</br>
</br>

#### - how much the price vary over the year?
![hotel prices](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/Screenshot%202024-02-19%20230948.png)
![hotel prices graph](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/room%20per%20night%20over%20the%20year.png)
  - The prices in the Resort Hotel are much higher during the summer
  - The prices in the city hotel varies less and is most expensive during Spring to Autumn
</br>

#### - Which are the busy month ?
![busy month](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/Screenshot%202024-02-19%20231047.png)
![busy month graph](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/Total%20guest%20per%20mo.png)
  - The City hotel has more guests during spring to autumn, , In July and August there are less visitors.</br>
  - Guest numbers for the Resort hotel go down slightly from June to September. Both hotels have the fewest guests during the winter.
</br>

#### - How many booking are cancel?
![booking cancel](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/percentage%20cancel%20booking.png)
  - Total bookings canceled: 24,025 (27 %)
  - Resort hotel bookings canceled: 7,976 (23 %)
  - City hotel bookings canceled: 16,049 (30 %)

### Matrix correlation
![matrix correlaiton](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/matrix%20correlation.png)

There are no high correlation (>0.83) between features

## Machine learning model
### Baseline model
In this case, we need to see some metric evaluation:
- Precision(false positive): to know the exact model in cancelation booking
- Recall(false negative): to find out the number of errors in determining cancel bookings

![baseline model](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/baseline%20model.png)

The best model is Catboost, Because it’s has the biggest recall and model accuracy

### Confusion Matrix
![confusion matrix catboost](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/cm%20catboost.png)

- 19035 bookings were correctly predicted as not canceled (True Negatives).
- 16 bookings were incorrectly predicted as canceled when they were actually not canceled (False Positives).
- 114  bookings were incorrectly predicted as not canceled when they were actually canceled (False Negatives).
- 7004 bookings were correctly predicted as canceled (True Positives).

## feature importance
![feature importance](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/feature%20importance.png)

## Action & Recommendation
![action & recommendation](https://github.com/vinahuang97/final_project_data_science/blob/main/final%20project%20pic/action%20%26%20recommendation.png)

## appendix
https://www.kaggle.com/code/marcuswingen/eda-of-bookings-and-ml-to-predict-cancelations (dataset)</br>
https://www.sciencedirect.com/science/article/pii/S2352340918315191 (about dataset)



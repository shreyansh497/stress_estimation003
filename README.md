# stress_estimation003
# About_model
i made two model which predict the stress level of the person based on some inputes like ["Social_interaction_score","gender","student_type","sleep_quality","sleephoursimputed","screentimeimputedinhours","physicalactmin","moodscore"]. from this model we can predict the stress level of the person ["Low":0,"Medium":1,"High":2] so that early precautions can be taken to minimise it.In today's time majority of individual is suffering from some kind of stress and mental hardships.this is just a small step to cure it as soon as possible. 
My first model:model.lr
-it use logistic regression for prediction
My second model:model.rf
-it use RandomTreeClassifier algorithm for prediction

# Feature use
["sleephoursimputed","screentimeimputedinhours","physicalactmin","moodscore"]:Random imputation to fill null values
["Social_interaction_score","moodscore"]:these two columns were not giving good pdf curve so application of power transformer,method:yue-johnson is there
["sleep_quality"]: as this column consist of poor,average,good value so ordinal encoding is applied
["gender","student_type"]:as they are categorical columns so onehot encoding is applied
["stress_level"]:this is the output column which is categorical so label encoding is applied

# others
use GridSearchCV to predict best inputs for logistic regression, the prediction was wrong then applied hit and trial by myself and accuracy increased

# Accuracy
model.lr:82.5%
model.rf:85%




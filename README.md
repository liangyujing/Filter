# idem only for correctly solved trials
preliminary_data<-experimental_df%>%
  filter(ACC == 1)%>%
  group_by(solution_type)%>%
  summarise(mean_conf = mean(confidence), mean_RT = mean(RT))

summary(preliminary_data)

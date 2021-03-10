# hw1
target_data = list(filter(lambda i: i['TEMP'] != '-99.000', data)) 
#filt the data which equals to -99.000 in 'TEMP', and put all the data into target_data

target_data = list(filter(lambda i: i['TEMP'] != '-999.000', target_data))
#filt the data which equals to -999.000 in 'TEMP', and put all the data into target_data

target_data_C0A880 = list(filter(lambda i: i['station_id'] == 'C0A880', target_data)) 
#filt the target_data which is in station 'C0A880', and put all the data into target_data_C0A880

target_data_C0F9A0 = list(filter(lambda i: i['station_id'] == 'C0F9A0', target_data)) 
#filt the target_data which is in station 'C0F9A0', and put all the data into target_data_C0F9A0

target_data_C0G640 = list(filter(lambda i: i['station_id'] == 'C0G640', target_data)) 
#filt the target_data which is in station 'C0G640', and put all the data into target_data_C0G640

target_data_C0R190 = list(filter(lambda i: i['station_id'] == 'C0R190', target_data)) 
#filt the target_data which is in station 'C0R190', and put all the data into target_data_C0R190

target_data_C0X260 = list(filter(lambda i: i['station_id'] == 'C0X260', target_data)) 
#filt the target_data which is in station 'C0X260', and put all the data into target_data_C0X260

result = [] #create a list of 'result' which is for the output
data_temp = [] #create a list for the temporary data for each station

for temp in target_data_C0A880:                       #running through all the data in station C0A880
   data_temp.append(float(temp['TEMP']))              #change all the data from char to float 
result.append(('C0A880',max(data_temp)))              #find the maiximum tempurature of that station
del data_temp[:]                                      #erase the data in data_temp

for temp in target_data_C0F9A0:                       #running through all the data in station C0F9A0
   data_temp.append(float(temp['TEMP']))              #change all the data from char to float 
result.append(('C0F9A0',max(data_temp)))              #find the maiximum tempurature of that station
del data_temp[:]                                      #erase the data in data_temp

for temp in target_data_C0G640:                       #running through all the data in station C0G640
   data_temp.append(float(temp['TEMP']))              #change all the data from char to float
result.append(('C0G640',max(data_temp)))              #find the maiximum tempurature of that station
del data_temp[:]                                      #erase the data in data_temp

for temp in target_data_C0R190:                       #running through all the data in station C0R190
   data_temp.append(float(temp['TEMP']))              #change all the data from char to float
result.append(('C0R190',max(data_temp)))              #find the maiximum tempurature of that station
del data_temp[:]                                      #erase the data in data_temp

for temp in target_data_C0X260:                       #running through all the data in station C0X260
   data_temp.append(float(temp['TEMP']))              #change all the data from char to float
result.append(('C0X260',max(data_temp)))              #find the maiximum tempurature of that station

result.sort()                                         #sort the result list


print(result)                                         #print the result.





RESULTS: 
[('C0A880', 26.7), ('C0F9A0', 31.2), ('C0G640', 31.4), ('C0R190', 34.6), ('C0X260', 31.7)]

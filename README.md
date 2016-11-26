# NHTSA-API
from urllib2 import urlopen
from json import load
apiUrl = "http://www.nhtsa.gov/webapi/api/SafetyRatings"
apiParam = " "
outputFormat = "?format=json"
/parameterName1/parameterValue1/parameterName2/parameterValue2/parameterName3/parameterValue3.
response = urlopen("http://www.nhtsa.gov/webapi/api/SafetyRatings" + "/modelyear/2013" + "/modelyear/2013/make/audi" + "/modelyear/2013/make/audi/model/a4" +  "/VehicleId/7045"
 +"?format=json")
 json_obj = load(response)
 print '------------------------------'
print '           Result			 '
print '------------------------------'
for objectCollection in json_obj['Results']:
	# Loop each vehicle in the vehicles collection
    for safetyRatingAttribute, safetyRatingValue in objectCollection.iteritems():
        print safetyRatingAttribute, ": ", safetyRatingValue
        

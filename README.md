# opk-thermofisher-pdr1500-cli

An Open Pipe Kit command line interface for interacting with the ThermoFisher pDR-1500 optical dust sensor over USB

Example: 

     ./stream -i 1 -j
 
> {"concentrationUgM":3.12,"temperatureC":26.9,"relativeHumidityPercent":36,"pressureMmHG":763}
> {"concentrationUgM":3.27,"temperatureC":26.9,"relativeHumidityPercent":36,"pressureMmHG":763}

Or to push to Phant.js:

     ./stream -i 1 -j  | ./opk-phant-cli/push --url data.sparkfun.com --public_key g6Gn19yp9yU6WaObjlYO --private_key XXXXXXXXXXXXX --field_name misc --stream --json

In Phant, you'll need the following fields:

* "concentrationugm"
* "temperaturec"
* "relativehumiditypercent"
* "pressuremmhg"

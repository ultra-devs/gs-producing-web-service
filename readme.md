## how to run the application
go to : https://github.com/ultra-devs/gs-producing-web-service.git
download the zip file 
open command prompt :
go to /complete/src/main/
run : `java -jargs-producing-web-service-0.1.0.jar`
wait till you get following message like this
`2018-07-14 11:40:36.221  INFO 16212 --- [nio-8080-exec-1] o.s.w.t.http.MessageDispatcherServlet    : FrameworkServlet 'messageDispatcherServlet': initialization compl
eted in 530 ms`

The service will start listening @8080

sample req:


<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
				  xmlns:gs="http://spring.io/guides/gs-producing-web-service">
   <soapenv:Header/>
   <soapenv:Body>
      <gs:getCountryRequest>
         <gs:name>Spain</gs:name>
      </gs:getCountryRequest>
   </soapenv:Body>
</soapenv:Envelope>



sample response
<?xml version="1.0"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header/>
  <SOAP-ENV:Body>
    <ns2:getCountryResponse xmlns:ns2="http://spring.io/guides/gs-producing-web-service">
      <ns2:country>
        <ns2:name>Spain</ns2:name>
        <ns2:population>46704314</ns2:population>
        <ns2:capital>Madrid</ns2:capital>
        <ns2:currency>EUR</ns2:currency>
      </ns2:country>
    </ns2:getCountryResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>







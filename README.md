RPV Turbo
===================

The RealPhoneValidation Turbo API uses HTTP GET/POST methods and supports both HTTPS and plain HTTP.  Determines connectivity in a flash and you get the industry best in connect/disconnect information in about 2 seconds.


**Required Input Parameters:**

Parameter | Description
-------- | ---
Output | (OPTIONAL) set to “json” or “xml”. Omitting this defaults to XML
Phone    | 10 numeric digits ONLY
Token     | unique PW given by us


**Response Fields:**

Response Fields | Description
-------- | ---
Status | (See appendix A)
error_text    | (See appendix A)
iscell     | “Y” means Cell phone, “N” means Landline (“V” is for VoIP if enabled on account)
cnam | The caller ID of the phone
carrier | Service provider. Such as Verizon, AT&T, etc.


**Example: Connected Phone Line**

```
https://api.realvalidation.com/rpvWebService/RealPhoneValidationTurbo.php?output=xml&phone=7275555555&token=1234ABCD-1234-ABCD-1234-123456ABCDEF 
```

**Result in XML**

```
<?xml version="1.0" encoding="UTF-8"?>
<response>
	<status>connected</status>
	<error_text></error_text>
	<iscell>Y</iscell>
	<cnam>WIRELESS CALLER</cnam>
	<carrier>Verizon Wireless:6006 - SVR/2</carrier>
</response>
```

**Result in JSON**

```
{
"status":"connected",
"error_text":{},
"iscell":"Y",
"cnam":"WIRELESS CALLER",
"carrier":"Verizon Wireless:6006 - SVR\/2"
}```



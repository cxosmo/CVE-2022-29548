Proof of concept exploit for CVE-2022-29548: A reflected XSS issue exists in the Management Console of several WSO2 products. This affects API Manager 2.2.0, 2.5.0, 2.6.0, 3.0.0, 3.1.0, 3.2.0, and 4.0.0; API Manager Analytics 2.2.0, 2.5.0, and 2.6.0; API Microgateway 2.2.0; Data Analytics Server 3.2.0; Enterprise Integrator 6.2.0, 6.3.0, 6.4.0, 6.5.0, and 6.6.0; IS as Key Manager 5.5.0, 5.6.0, 5.7.0, 5.9.0, and 5.10.0; Identity Server 5.5.0, 5.6.0, 5.7.0, 5.9.0, 5.10.0, and 5.11.0; Identity Server Analytics 5.5.0 and 5.6.0; and WSO2 Micro Integrator 1.0.0.

# References
[MITRE](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-29548)

[Vendor Advisory](https://docs.wso2.com/display/Security/Security+Advisory+WSO2-2021-1603)

[Fix Implementation](https://github.com/wso2/carbon-kernel/pull/3145)

# PoC Notes
* Tested against: `WSO2 API Manager 4.0.0`
* Payload snippet: `https://localhost:9443/carbon/admin/login.jsp?loginStatus=false&errorCode=%27);alert(document.domain)//`

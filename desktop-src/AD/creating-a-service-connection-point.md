---
title: Creazione di un punto di connessione del servizio
description: Nell'esempio di codice seguente viene illustrato come creare e inizializzare un punto di connessione del servizio.
ms.assetid: 6ab1e72f-22e8-499a-916e-c2ba8e2c2aff
ms.tgt_platform: multiple
keywords:
- Creazione di un punto di connessione del servizio AD
- Punto di connessione del servizio, creazione di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ec4e9097414ea8131b3dd1cbd832e73b388e5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046541"
---
# <a name="creating-a-service-connection-point"></a>Creazione di un punto di connessione del servizio

Nell'esempio di codice seguente viene illustrato come creare e inizializzare un punto di connessione del servizio. L'esempio di codice esegue passaggi aggiuntivi che consentono al servizio di aggiornare i valori SCP in fase di esecuzione. In genere, un programma di installazione del servizio esegue questi passaggi come parte dell'installazione di un'istanza del servizio in un computer host.

Questo esempio di codice crea l'oggetto SCP come oggetto figlio per l'oggetto del computer locale. Usa la funzione [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) per ottenere il nome distinto dell'oggetto computer locale. USA quindi il DN per eseguire l'associazione a un puntatore [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) per l'oggetto computer. Il metodo [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) crea il SCP e specifica i valori iniziali per gli attributi SCP importanti.

[**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) restituisce un puntatore al nuovo SCP, usato nell'esempio di codice per recuperare un puntatore [**IADs**](/windows/desktop/api/iads/nn-iads-iads) per SCP. Nell'esempio di codice vengono utilizzati i metodi **IADs** per recuperare gli attributi **objectGUID** e **Distinguishname** del SCP. L'esempio di codice usa **objectGUID** per comporre una stringa usata per l'associazione al SCP, quindi memorizza nella cache la stringa di binding GUID nel registro di sistema locale in cui può essere recuperata dal servizio in fase di esecuzione. Il **Distinguishname** viene restituito al chiamante della funzione per l'utilizzo nella composizione di un nome dell'entità servizio (SPN) per l'istanza del servizio.

Nell'esempio di codice seguente viene chiamata questa funzione come parte dei passaggi di base per l'installazione di un servizio abilitato per la directory. Per ulteriori informazioni, vedere [installazione di un servizio in un computer host](installing-a-service-on-a-host-computer.md).


```C++
// ScpCreate
//
// Create a new service connection point as a child object of the 
// local server computer object.
//
DWORD
ScpCreate(
       USHORT usPort, // Service's default port to store in SCP.
       LPTSTR szClass, // Service class string to store in SCP.
       LPTSTR szAccount, // Logon account that must access SCP.
       UINT ccDN, // Length of the pszDN buffer in characters
       TCHAR *pszDN) // Returns distinguished name of SCP.
{
DWORD dwStat, dwAttr, dwLen;
HRESULT hr;
IDispatch *pDisp;          // Returned dispinterface of new object.
IDirectoryObject *pComp;   // Computer object; parent of SCP.
IADs *pIADsSCP;            // IADs interface on new object.

if(!szClass || !szAccount || !pszDN || !(ccDN > 0))
{
       hr = ERROR_INVALID_PARAMETER;
       ReportError(TEXT("Invalid parameter."), hr);
       return hr;
}

// Values for SCPs keywords attribute.
TCHAR* KwVal[]={
        TEXT("83C29870-1DFC-11d3-A193-0000F87A9099"), // Vendor GUID.
        TEXT("A762885A-AA44-11d2-81F1-00C04FB9624E"), // Product GUID.
        TEXT("Microsoft"), // Vendor Name.
        TEXT("Windows 2000 Auth-O-Matic"), // Product Name.
};

TCHAR       szServer[MAX_PATH];
TCHAR       szDn[MAX_PATH];
TCHAR       szAdsPath[MAX_PATH];
TCHAR       szPort[6];

HKEY        hReg;
DWORD       dwDisp;

ADSVALUE cn,objclass,keywords[4],binding,classname,dnsname,nametype;

// SCP attributes to set during creation of SCP.
ADS_ATTR_INFO   ScpAttribs[] = 
{
    {
        TEXT("cn"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &cn,
        1
    },
    {
        TEXT("objectClass"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &objclass,
        1
    },
    {
         TEXT("keywords"),
         ADS_ATTR_UPDATE,
         ADSTYPE_CASE_IGNORE_STRING,
         keywords,
         4
    },
    {
         TEXT("serviceDnsName"),
         ADS_ATTR_UPDATE,
         ADSTYPE_CASE_IGNORE_STRING,
         &dnsname,
         1
    },
    {
        TEXT("serviceDnsNameType"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &nametype,
        1
    },
    {
        TEXT("serviceClassName"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &classname,
        1
    },
    {
        TEXT("serviceBindingInformation"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &binding,
        1
    },
};

BSTR bstrGuid = NULL;
TCHAR pwszBindByGuidStr[1024]; 
VARIANT var;

// Get the DNS name of the local computer.
dwLen = sizeof(szServer);
if (!GetComputerNameEx(ComputerNameDnsFullyQualified,szServer,&dwLen))
    return GetLastError();
_tprintf(TEXT("GetComputerNameEx: %s\n"), szServer);
    
// Enter the attribute values to be stored in the SCP.
keywords[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[2].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[3].dwType = ADSTYPE_CASE_IGNORE_STRING;

keywords[0].CaseIgnoreString=KwVal[0];
keywords[1].CaseIgnoreString=KwVal[1];
keywords[2].CaseIgnoreString=KwVal[2];
keywords[3].CaseIgnoreString=KwVal[3];

cn.dwType                   = ADSTYPE_CASE_IGNORE_STRING;
cn.CaseIgnoreString         = TEXT("SockAuthAD");
objclass.dwType             = ADSTYPE_CASE_IGNORE_STRING;
objclass.CaseIgnoreString   = TEXT("serviceConnectionPoint");

dnsname.dwType              = ADSTYPE_CASE_IGNORE_STRING;
dnsname.CaseIgnoreString    = szServer;
classname.dwType            = ADSTYPE_CASE_IGNORE_STRING;
classname.CaseIgnoreString  = szClass;

_stprintf_s(szPort,TEXT("%d"),usPort);
binding.dwType              = ADSTYPE_CASE_IGNORE_STRING;
binding.CaseIgnoreString    = szPort;
nametype.dwType             = ADSTYPE_CASE_IGNORE_STRING;
nametype.CaseIgnoreString   = TEXT("A");

/*
Get the distinguished name of the computer object for the local 
computer.
*/
dwLen = sizeof(szDn);
if (!GetComputerObjectName(NameFullyQualifiedDN,szDn,&dwLen))
    return GetLastError();
_tprintf(TEXT("GetComputerObjectName: %s\n"), szDn);

/*
Compose the ADSpath and bind to the computer object for the local 
computer.
*/
_tcsncpy_s(szAdsPath,TEXT("LDAP://"),MAX_PATH);
_tcsncat_s(szAdsPath,szDn,MAX_PATH - _tcslen(szAdsPath));
hr = ADsGetObject(szAdsPath, IID_IDirectoryObject, (void **)&pComp);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to bind Computer Object."),hr);
    return hr;
}

//*******************************************************************
// Publish the SCP as a child of the computer object
//*******************************************************************

// Calculate attribute count.
dwAttr = sizeof(ScpAttribs)/sizeof(ADS_ATTR_INFO);  

// Complete the action.
hr = pComp->CreateDSObject(TEXT("cn=SockAuthAD"),
                           ScpAttribs, dwAttr, &pDisp);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to create SCP:"), hr);
    pComp -> Release();
    return hr;
}

pComp -> Release();

// Query for an IADs pointer on the SCP object.
hr = pDisp->QueryInterface(IID_IADs,(void **)&pIADsSCP);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to QueryInterface for IADs:"),hr);
    pDisp->Release();
    return hr;
}
pDisp->Release();

// Set ACEs on the SCP so a service can modify it.
hr = AllowAccessToScpProperties(
        szAccount,     // Service account to allow access.
        pIADsSCP);     // IADs pointer to the SCP object.
if (FAILED(hr)) {
    ReportError(TEXT("Failed to set ACEs on SCP DACL:"), hr);
    return hr;
}

// Get the distinguished name of the SCP.
VariantInit(&var); 
hr = pIADsSCP->Get(CComBSTR("distinguishedName"), &var); 
if (FAILED(hr)) {
    ReportError(TEXT("Failed to get distinguishedName:"), hr);
    pIADsSCP->Release();
    return hr;
}
_tprintf(TEXT("distinguishedName via IADs: %s\n"), var.bstrVal);

// Return the DN of the SCP, which is used to compose the SPN.
// The best practice is to either accept and return the buffer
// size or do this in a _try / _except block, both omitted here
// for clarity.
_tcsncpy_s(pszDN, var.bstrVal, ccDN);

// Retrieve the SCP objectGUID in format suitable for binding. 
hr = pIADsSCP->get_GUID(&bstrGuid); 
if (FAILED(hr)) {
    ReportError(TEXT("Failed to get GUID:"), hr);
    pIADsSCP->Release();
    return hr;
}

// Build a string for binding to the object by GUID.
_tcsncpy_s(pwszBindByGuidStr, 
    TEXT("LDAP://<GUID="),
    1024);
_tcsncat_s(pwszBindByGuidStr, 
    bstrGuid, 
    1024 -_tcslen(pwszBindByGuidStr));
_tcsncat_s(pwszBindByGuidStr, 
    TEXT(">"), 
    1024 -_tcslen(pwszBindByGuidStr));
_tprintf(TEXT("GUID binding string: %s\n"), 
    pwszBindByGuidStr);

pIADsSCP->Release();

// Create a registry key under 
// HKEY_LOCAL_MACHINE\SOFTWARE\Vendor\Product.
dwStat = RegCreateKeyEx(HKEY_LOCAL_MACHINE,
            TEXT("Software\\Fabrikam\\Auth-O-Matic"),
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            KEY_ALL_ACCESS,
            NULL,
            &hReg,
            &dwDisp);
if (dwStat != NO_ERROR) {
    ReportError(TEXT("RegCreateKeyEx failed:"), dwStat);
    return dwStat;
}

// Cache the GUID binding string under the registry key.
dwStat = RegSetValueEx(hReg, TEXT("GUIDBindingString"), 0, REG_SZ,
                           (const BYTE *)pwszBindByGuidStr, 
                           2*(_tcslen(pwszBindByGuidStr)));
if (dwStat != NO_ERROR) {
    ReportError(TEXT("RegSetValueEx failed:"), dwStat);
    return dwStat;
}

RegCloseKey(hReg);

// Cleanup should delete the SCP and registry key if an error occurs.

return dwStat;
}
```



 

 
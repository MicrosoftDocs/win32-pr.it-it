---
title: Esempio di codice per l'utilizzo di messaggi di errore ADSI
description: Nell'esempio di codice seguente viene illustrato come recuperare un messaggio di errore ADSI.
ms.assetid: c09fea2e-b6c1-4318-a7a6-b1c4c30ef4cb
ms.tgt_platform: multiple
keywords:
- messaggi di errore e codice di esempio per ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aed5285a41dc51b8c42a82f7c1f600d1bae33e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855337"
---
# <a name="code-example-for-working-with-adsi-error-messages"></a><span data-ttu-id="f2da1-104">Esempio di codice per l'utilizzo di messaggi di errore ADSI</span><span class="sxs-lookup"><span data-stu-id="f2da1-104">Code Example for Working with ADSI Error Messages</span></span>

<span data-ttu-id="f2da1-105">Nell'esempio di codice seguente viene illustrato come recuperare un messaggio di errore ADSI.</span><span class="sxs-lookup"><span data-stu-id="f2da1-105">The following code example shows how to retrieve an ADSI error message.</span></span>


```C++
CString GetErrorMessage( HRESULT hr )
{
    BOOL bRet;
    CString s;
    LPTSTR lpBuffer=NULL;
 
    if ( SUCCEEDED(hr) )
    {
        return _T("Success");
    }
 
    
    if ( hr & 0x00005000) // standard ADSI Errors 
    {
        s = GetADSIError(hr);
    }
    else if ( HRESULT_FACILITY(hr)==FACILITY_WIN32 )
    {
 
 
        /////////////////////////////////////////////
        // Retrieve the Win32 Error message
        /////////////////////////////////////////////
 
        bRet = FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER | 
                             FORMAT_MESSAGE_FROM_SYSTEM,
                             NULL,  hr,
                             MAKELANGID(LANG_NEUTRAL, 
                             SUBLANG_SYS_DEFAULT),
                             (LPTSTR) &lpBuffer, 0, NULL);
 
        if ( !bRet )
        {
            s.Format(_T("Error %ld"), hr );
        }
 
        if ( lpBuffer )
        {
            s = lpBuffer;
            LocalFree( lpBuffer );
        }
    }
    else // Non Win32 Error
    {
        s.Format("%X", hr );
        return s;
    }
 
    //////////////////////////////////////////////////////////////////
    //
    // Extended error message may be returned. 
    //
    // IADs, IADsContainer, IDirectoryObject or IDirectorySearch may 
    // return this extended error message
    //
    /////////////////////////////////////////////////////////////////
    WCHAR szBuffer[MAX_PATH];
    WCHAR szName[MAX_PATH];
    DWORD dwError;
    
 
    hr = ADsGetLastError( &dwError, szBuffer, (sizeof(szBuffer)/sizeof(WCHAR))-1,
                          szName, (sizeof(szName)/sizeof(WCHAR))-1 );
 
    
    if ( SUCCEEDED(hr) && dwError != ERROR_INVALID_DATA  && 
                                     wcslen(szBuffer))
    {
        USES_CONVERSION;
        s += _T("  -- Extended Error --- ");
        s += OLE2T(szName);
        s += _T(" : ");
        s += OLE2T( szBuffer );
    }
 
 
    return s;
}
 
 
typedef struct tagADSERRMSG
{
    HRESULT    hr;
    LPCTSTR    pszError;
}ADSERRMSG;
 
#define ADDADSERROR(x)   x, _T(#x)
 
ADSERRMSG adsErr[] = 
{
    ADDADSERROR(E_ADS_BAD_PATHNAME),
    ADDADSERROR(E_ADS_INVALID_DOMAIN_OBJECT),
    ADDADSERROR(E_ADS_INVALID_USER_OBJECT),
    ADDADSERROR(E_ADS_INVALID_COMPUTER_OBJECT),
    ADDADSERROR(E_ADS_UNKNOWN_OBJECT),
    ADDADSERROR(E_ADS_PROPERTY_NOT_SET),
    ADDADSERROR(E_ADS_PROPERTY_NOT_SUPPORTED),
    ADDADSERROR(E_ADS_PROPERTY_INVALID),
    ADDADSERROR(E_ADS_BAD_PARAMETER),
    ADDADSERROR(E_ADS_OBJECT_UNBOUND),
    ADDADSERROR(E_ADS_PROPERTY_NOT_MODIFIED),
    ADDADSERROR(E_ADS_PROPERTY_MODIFIED),
    ADDADSERROR(E_ADS_CANT_CONVERT_DATATYPE),
    ADDADSERROR(E_ADS_PROPERTY_NOT_FOUND),
    ADDADSERROR(E_ADS_OBJECT_EXISTS),
    ADDADSERROR(E_ADS_SCHEMA_VIOLATION),
    ADDADSERROR(E_ADS_COLUMN_NOT_SET),
    ADDADSERROR(E_ADS_INVALID_FILTER),
    ADDADSERROR(0),
};
 
 
/////////////////////////////////////////////
//
// Error message specific to ADSI 
//
////////////////////////////////////////////
CString GetADSIError( HRESULT hr )
{
    CString s;
 
 
    if ( hr & 0x00005000 )
    {
        int idx=0;
        while (adsErr[idx].hr != 0 )
        {
            if ( adsErr[idx].hr == hr )
            {
                return adsErr[idx].pszError;
            }
            idx++;
        }
    }
 
    return _T("");
  
 
}
```



 

 





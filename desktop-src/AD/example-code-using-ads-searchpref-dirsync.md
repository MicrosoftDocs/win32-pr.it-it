---
title: Codice di esempio con ADS_SEARCHPREF_DIRSYNC
description: Nell'esempio di codice seguente viene utilizzata l'implementazione ADSI del controllo di sincronizzazione della directory (DirSync) per eseguire la ricerca nella partizione di dominio locale di un server Active Directory per gli oggetti utente modificati dalla chiamata precedente.
ms.assetid: 8bf9dae7-426c-4018-ad6d-b20395beba01
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, usando ADS_SEARCHPREF_DIRSYNC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c9e7ea0ce262be9268ddc2e7a9c63af213c3b3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472555"
---
# <a name="example-code-using-ads_searchpref_dirsync"></a><span data-ttu-id="c569b-104">Esempio di codice con ADS \_ SEARCHPREF \_ dirsync</span><span class="sxs-lookup"><span data-stu-id="c569b-104">Example Code Using ADS\_SEARCHPREF\_DIRSYNC</span></span>

<span data-ttu-id="c569b-105">Nell'esempio di codice seguente viene utilizzata l'implementazione ADSI del controllo di sincronizzazione della directory (DirSync) per eseguire la ricerca nella partizione di dominio locale di un server Active Directory per gli oggetti utente modificati dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="c569b-105">The following code example uses the ADSI implementation of the directory synchronization (DirSync) control to search the local domain partition of an Active Directory server for user objects changed since the previous call.</span></span>

<span data-ttu-id="c569b-106">Nell'esempio di codice viene utilizzata l'interfaccia [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per eseguire la ricerca dalla radice della partizione di dominio.</span><span class="sxs-lookup"><span data-stu-id="c569b-106">The code example uses the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface to search from the root of the domain partition.</span></span> <span data-ttu-id="c569b-107">Prima di chiamare il metodo [**ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) , nell'esempio viene chiamato il metodo [**SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) per specificare le preferenze di ricerca Ads **\_ SEARCHPREF \_ \_**, **Ads \_ SEARCHPREF \_ dirsync** e **ADS SEARCHPREF per la \_ \_ rimozione definitiva** .</span><span class="sxs-lookup"><span data-stu-id="c569b-107">Before calling the [**ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) method, the example calls the [**SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) method to specify the **ADS\_SEARCHPREF\_SEARCH\_SCOPE**, **ADS\_SEARCHPREF\_DIRSYNC**, and **ADS\_SEARCHPREF\_TOMBSTONE** search preferences.</span></span> <span data-ttu-id="c569b-108">L'ambito deve specificare una ricerca di sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="c569b-108">The scope must specify a subtree search.</span></span> <span data-ttu-id="c569b-109">Con la preferenza di ricerca di **Ads \_ SEARCHPREF \_ dirsync** , specificare una struttura [**\_ \_ specifica di ADS**](/windows/win32/api/iads/ns-iads-ads_prov_specific) che contenga la lunghezza del cookie e un puntatore.</span><span class="sxs-lookup"><span data-stu-id="c569b-109">With the **ADS\_SEARCHPREF\_DIRSYNC** search preference, specify an [**ADS\_PROV\_SPECIFIC**](/windows/win32/api/iads/ns-iads-ads_prov_specific) structure that contains the length of the cookie and a pointer to it.</span></span>

<span data-ttu-id="c569b-110">La prima volta che l'applicazione viene chiamata, specifica un cookie null e una lunghezza pari a zero.</span><span class="sxs-lookup"><span data-stu-id="c569b-110">The first time this application is called, it specifies a null cookie and a zero length.</span></span> <span data-ttu-id="c569b-111">In questo modo l'operazione di ricerca esegue una lettura completa, restituendo tutti gli attributi richiesti per tutti gli oggetti che corrispondono al filtro.</span><span class="sxs-lookup"><span data-stu-id="c569b-111">This causes the search operation to perform a full read, returning all the requested attributes for all objects that match the filter.</span></span> <span data-ttu-id="c569b-112">Insieme ai risultati della ricerca, il server restituisce un cookie valido e la lunghezza del cookie.</span><span class="sxs-lookup"><span data-stu-id="c569b-112">Along with the search results, the server returns a valid cookie and the cookie length.</span></span> <span data-ttu-id="c569b-113">Nelle esecuzioni successive il programma recupera il cookie e la lunghezza memorizzati nella cache e li usa per recuperare le modifiche dall'esecuzione precedente.</span><span class="sxs-lookup"><span data-stu-id="c569b-113">On subsequent runs, the program retrieves the cached cookie and length and uses them to retrieve changes since the previous run.</span></span>

<span data-ttu-id="c569b-114">Tenere presente che in questo esempio vengono semplicemente memorizzati nella cache il cookie e la lunghezza dei cookie nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c569b-114">Be aware that this sample simply caches the cookie and cookie length in the registry.</span></span> <span data-ttu-id="c569b-115">In un'applicazione di sincronizzazione reale, archiviare i parametri nello stesso spazio di archiviazione che si mantiene coerente con il server Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c569b-115">In a real synchronization application, store the parameters in the same storage that you are keeping consistent with the Active Directory server.</span></span> <span data-ttu-id="c569b-116">In questo modo si garantisce che i parametri e i dati oggetto rimangano sincronizzati se il database viene ripristinato da un backup.</span><span class="sxs-lookup"><span data-stu-id="c569b-116">This ensures that the parameters and object data remain in sync if your database is ever restored from a backup.</span></span>


```C++
//  Add adsiid.lib to project
//  Add activeds.lib to project

#include "stdafx.h"
#include "windows.h"
#include "stdio.h"
#include "activeds.h"
#include "adshlp.h"
#include "atlbase.h"
#include "iads.h"
#include "tchar.h"
#include "string.h"
#include "mbstring.h"
#include "stdlib.h"

typedef struct {WCHAR objectGUID[40];
                WCHAR ADsPath[MAX_PATH];
                WCHAR phoneNumber[32];
                BOOL  isDeleted;
               } MyUserData;

//  Forward declaration.
VOID BuildGUIDString(WCHAR *szGUID, LPBYTE pGUID);
VOID WriteObjectDataToStorage(MyUserData *userdata, BOOL bUpdate);

//  DoDirSyncSearch
HRESULT DoDirSyncSearch(
            LPWSTR pszSearchFilter,  //  Search filter.
            LPWSTR *pAttributeNames, //  Attributes to retrieve.
            DWORD dwAttributes,      //  Number of attributes.
            PUCHAR *ppCookie,        //  Pointer to previous cookie.
            PULONG pulCookieLength,  //  Length of previous cookie.
            LPWSTR szDC)             //  Name of DC to bind to.
{
    IADs *pRootDSE = NULL;
    IDirectorySearch *pSearch = NULL;
    ADS_SEARCH_HANDLE hSearch = NULL;
    ADS_SEARCHPREF_INFO arSearchPrefs[3];
    ADS_PROV_SPECIFIC dirsync;
    ADS_SEARCH_COLUMN col;
    HRESULT hr = S_OK;
    VARIANT var;
    MyUserData userdata;
    BOOL bUpdate = FALSE;
    DWORD dwCount = 0;
    
    //  Validate input parameters.
    if (!pulCookieLength || !ppCookie || !szDC) 
    {
        wprintf(L"Invalid parameter.\n");
        return E_FAIL;
    }
    
    LPOLESTR szDSPath = new OLECHAR[MAX_PATH];
    LPOLESTR szServerPath = new OLECHAR[MAX_PATH];
    VariantInit(&var);
    
    //  If cookie is non-NULL, this is an update. Otherwise, it is a full-read.
    if (*ppCookie)
        bUpdate = TRUE;
    CoInitialize(NULL);
    
    //  If there is a DC name from the previous USN sync, 
    //  include it in the binding string.
    if (szDC[0]) 
    {
        wcsncpy_s(szServerPath,MAX_PATH,L"LDAP://",MAX_PATH);
        wcsncat_s(szServerPath, MAX_PATH,szDC,MAX_PATH-wcslen(szServerPath));
        wcsncat_s(szServerPath, MAX_PATH,L"/",MAX_PATH-wcslen(szServerPath));
    }
    else
        wcsncpy_s(szServerPath, MAX_PATH,L"LDAP://",MAX_PATH);
    
    // Bind to root DSE.
    wcsncpy_s(szDSPath,MAX_PATH,szServerPath,MAX_PATH);
    wcsncat_s(szDSPath, MAX_PATH,L"rootDSE",MAX_PATH-wcslen(szDSPath));
    wprintf(L"RootDSE binding string: %s\n", szDSPath);
    hr = ADsGetObject(szDSPath, 
                  IID_IADs,
                  (void**)&pRootDSE);
    if (FAILED(hr)) 
    {
        wprintf(L"failed to bind to rootDSE: 0x%x\n", hr);
        goto cleanup;
    }
    
    //  Save the name of the DC connected to in order to connect to 
    //  the same DC on the next dirsync operation.
    if (! szDC[0])
    {
        hr = pRootDSE->Get(CComBSTR("DnsHostName"), &var);
        wcsncpy_s(szServerPath,MAX_PATH,L"LDAP://",MAX_PATH);
        wcsncat_s(szServerPath, MAX_PATH,var.bstrVal, MAX_PATH-wcslen(szServerPath));
        wcsncat_s(szServerPath, MAX_PATH,L"/", MAX_PATH-wcslen(szServerPath));
    }
    
    //  Get an IDirectorySearch pointer to the root of the domain partition.
    hr = pRootDSE->Get(CComBSTR("defaultNamingContext"), &var);
    wcsncpy_s(szDSPath,MAX_PATH,szServerPath,MAX_PATH);
    wcsncat_s(szDSPath, MAX_PATH,var.bstrVal, MAX_PATH - wcslen(szDSPath));
    hr = ADsGetObject(szDSPath, IID_IDirectorySearch, (void**) &pSearch);
    if (FAILED(hr)) 
    {
        wprintf(L"failed to get IDirectorySearch: 0x%x\n", hr);
        goto cleanup;
    }
    
    //  Initialize the structure to pass in the cookie.
    //  On the first call, the cookie is NULL and the length is zero.
    //  On later calls, the cookie and length are the values returned by 
    //  the previous call.
    dirsync.dwLength = *pulCookieLength;
    dirsync.lpValue = *ppCookie;
    arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
    arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER; 
    arSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE; 
    arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_DIRSYNC; 
    arSearchPrefs[1].vValue.dwType = ADSTYPE_PROV_SPECIFIC;
    arSearchPrefs[1].vValue.ProviderSpecific = dirsync;
    hr = pSearch->SetSearchPreference(arSearchPrefs, 2);
    if (FAILED(hr)) 
    {
        wprintf(L"failed to set search prefs: 0x%x\n", hr);
        goto cleanup;
    }
    
    // Search for the objects indicated by the search filter.
    hr = pSearch->ExecuteSearch(pszSearchFilter,
                    pAttributeNames, dwAttributes, &hSearch );
    if (FAILED(hr)) 
    {
        wprintf(L"failed to set execute search: 0x%x\n", hr);
        goto cleanup;
    }
    
    //  Loop through the rows of the search result
    //  Each row is an object that has changed since the previous call.
    hr = pSearch->GetNextRow( hSearch);
    while ( SUCCEEDED(hr) && hr != S_ADS_NOMORE_ROWS )
    {
        ZeroMemory(&userdata, sizeof(MyUserData) );
        
        //  Retrieve the attributes for each object.
        //  With a DirSync search, a GetColumn call can return success even
        //  though no values are set for the specified attribute. If this
        //  happens, col.pADsValues is NULL; the following code checks
        //  col.pADsValues before trying to access it.
        //  Get the telephone number.
        hr = pSearch->GetColumn( hSearch, L"telephoneNumber", &col );
        if ( SUCCEEDED(hr) ) 
        {
            if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING && col.pADsValues)
                wcscpy_s(userdata.phoneNumber, col.pADsValues->CaseIgnoreString);
            pSearch->FreeColumn( &col );
        }
        
        //  Get the isDeleted attribute.
        hr = pSearch->GetColumn( hSearch, L"isDeleted", &col );
        if ( SUCCEEDED(hr) ) 
        {
            if (col.dwADsType == ADSTYPE_BOOLEAN && col.pADsValues)
                userdata.isDeleted = col.pADsValues->Boolean;
            pSearch->FreeColumn( &col );
        }
        
        //  Get the ADsPath.
        hr = pSearch->GetColumn( hSearch, L"ADsPath", &col );
        if ( SUCCEEDED(hr) ) 
        {
            if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING && col.pADsValues)
                wcscpy_s(userdata.ADsPath, col.pADsValues->CaseIgnoreString);
            pSearch->FreeColumn( &col );
        }
        
        //  Get the objectGUID number.
        hr = pSearch->GetColumn( hSearch, L"objectGUID", &col );
        if ( SUCCEEDED(hr) ) 
        {
            WCHAR szGUID[40]; //  string version of the objectGUID attribute
            if ((col.dwADsType == ADSTYPE_OCTET_STRING) && col.pADsValues &&
                (col.pADsValues->OctetString.lpValue))
            {
                BuildGUIDString(szGUID, (LPBYTE) col.pADsValues->OctetString.lpValue);
                wcscpy_s(userdata.objectGUID, szGUID);
            }
            pSearch->FreeColumn( &col );
        }
        
        WriteObjectDataToStorage(&userdata, bUpdate);
        dwCount++;
        hr = pSearch->GetNextRow( hSearch);
    }
    wprintf(L"dwCount: %d\n", dwCount);

    //  After looping through the results, get the cookie.
    if (hr == S_ADS_NOMORE_ROWS ) 
    {
        hr = pSearch->GetColumn( hSearch, ADS_DIRSYNC_COOKIE, &col );
        if ( SUCCEEDED(hr) ) {
            if (col.dwADsType == ADSTYPE_PROV_SPECIFIC && col.pADsValues) 
            {
                wprintf(L"Got cookie\n");
                *pulCookieLength = col.pADsValues->ProviderSpecific.dwLength;
                *ppCookie = (PUCHAR) AllocADsMem (*pulCookieLength);
                memcpy(*ppCookie, col.pADsValues->ProviderSpecific.lpValue, 
                    *pulCookieLength);
            }
            pSearch->FreeColumn( &col );
        } else
            wprintf(L"no cookie: 0x%x\n", hr);
    }

cleanup:
    if (pRootDSE)
        pRootDSE->Release();
    if (hSearch)
        pSearch->CloseSearchHandle(hSearch);
    if (pSearch)
        pSearch->Release();

    VariantClear(&var);
    CoUninitialize();
    delete [] szServerPath;
    delete [] szDSPath;

    return hr;
}

//  WriteObjectDataToStorage routine
VOID WriteObjectDataToStorage(MyUserData *userdata, BOOL bUpdate)
{
    if (bUpdate)
        wprintf(L"UPDATE:\n");
    else
        wprintf(L"INITIAL DATA:\n");
    wprintf(L"   objectGUID: %s\n", userdata->objectGUID);
    wprintf(L"   ADsPath: %s\n", userdata->ADsPath);
    wprintf(L"   phoneNumber: %s\n", userdata->phoneNumber);
    if (userdata->isDeleted)
        wprintf(L"   DELETED OBJECT\n");
    wprintf(L"---------------------------------------------\n");
    return;

}

//  WriteCookieAndDCtoStorage routine
//  This example caches the cookie in the registry. In a real 
//  synchronization application, store these parameters in the
//  same storage that you are keeping consistent with Active Directory.
//  This ensures that the parameters and object data remain in sync if 
//  the storage is ever restored from a backup.
DWORD WriteCookieAndDCtoStorage(UCHAR *pCookie, 
                                ULONG ulLength,
                                WCHAR *pszDCName) 
{
    HKEY hReg = NULL;
    DWORD dwStat = NO_ERROR;

    //  Create a registry key under 
    //  HKEY_CURRENT_USER\SOFTWARE\Vendor\Product.
    dwStat = RegCreateKeyExW(HKEY_CURRENT_USER,
                             L"Software\\Microsoft\\Windows 2000 AD-Synchro-DirSync",
                             0,
                             NULL,
                             REG_OPTION_NON_VOLATILE,
                             KEY_ALL_ACCESS,
                             NULL,
                             &hReg,
                             NULL);
    if (dwStat != NO_ERROR) 
    {
        wprintf(L"RegCreateKeyEx failed: 0x%x\n", dwStat);
        return dwStat;
    }

    //  Cache the cookie as a value under the registry key.
    dwStat = RegSetValueExW(hReg, L"Cookie", 0, REG_BINARY,
                            (const BYTE *)pCookie, ulLength);
    if (dwStat != NO_ERROR)
        wprintf(L"RegSetValueEx for cookie failed: 0x%x\n", dwStat);

    //  Cache the cookie length as a value under the registry key.
    dwStat = RegSetValueExW(hReg, L"Cookie Length", 0, REG_DWORD,
                            (const BYTE *)&ulLength, sizeof(DWORD) );
    if (dwStat != NO_ERROR)
        wprintf(L"RegSetValueEx for cookie length failed: 0x%x\n", dwStat);

    //  Cache the DC name as a value under the registry key.
    dwStat = RegSetValueExW(hReg, L"DC name", 0, REG_SZ,
        (const BYTE *)pszDCName, 2*(wcslen(pszDCName)) );
    if (dwStat != NO_ERROR)
        wprintf(L"RegSetValueEx for DC name failed: 0x%x\n", dwStat);
    RegCloseKey(hReg);
    return dwStat;
}

//  GetCookieAndDCfromStorage routine
DWORD GetCookieAndDCfromStorage(PUCHAR *ppCookie,        //  Receives pointer to cookie.
                                PULONG pulCookieLength,  //  Receives length of cookie.
                                WCHAR *pszDCName)        //  Receives name of DC to bind to.
{ 
    HKEY hReg = NULL;
    DWORD dwStat;
    DWORD dwLen;

    //  Open the registry key.
    dwStat = RegOpenKeyExW(HKEY_CURRENT_USER,
                           L"Software\\Microsoft\\Windows 2000 AD-Synchro-DirSync",
                           0,
                           KEY_QUERY_VALUE,
                           &hReg);
    if (dwStat != NO_ERROR) 
    {
        wprintf(L"RegOpenKeyEx failed: 0x%x\n", dwStat);
        return dwStat;
    }

    //  Get the length of the cookie from the registry.
    dwLen = sizeof(DWORD);
    dwStat = RegQueryValueExW(hReg, L"Cookie Length", NULL, NULL, 
                              (LPBYTE)pulCookieLength, &dwLen );
    if (dwStat != NO_ERROR) {
        wprintf(L"RegQueryValueEx failed to get length: 0x%x\n", dwStat);
        return dwStat;
    }

    //  Allocate a buffer for the cookie value.
    *ppCookie = (PUCHAR) GlobalAlloc(GPTR, *pulCookieLength);
    if (!*ppCookie) 
    {
        wprintf(L"GlobalAlloc failed: %u\n", GetLastError() );
        return dwStat;
    }

    //  Get the cookie from the registry.
    dwStat = RegQueryValueExW(hReg, L"Cookie", NULL, NULL, 
                              (LPBYTE)*ppCookie, pulCookieLength );
    if (dwStat != NO_ERROR) {
        wprintf(L"RegQueryValueEx failed to get cookie: 0x%x\n", dwStat);
        return dwStat;
    }

    //  Get the DC name from the registry.
    dwLen = MAX_PATH;
    dwStat = RegQueryValueExW(hReg, L"DC name", NULL, NULL, 
                              (LPBYTE)pszDCName, &dwLen );
    if (dwStat != NO_ERROR) {
        wprintf(L"RegQueryValueEx failed to get DC name: 0x%x\n", dwStat);
        return dwStat;
    }
    else
        pszDCName[dwLen] = 0;
    RegCloseKey(hReg);
    return NO_ERROR;
}

//  BuildGUIDString
//  Routine that makes the GUID into a string in directory service bind form
VOID 
    BuildGUIDString(WCHAR *szGUID, LPBYTE pGUID)
{
    DWORD i = 0x0;
    DWORD dwlen = sizeof(GUID);
    WCHAR buf[4];

    wcscpy_s(szGUID,MAX_PATH,L"");

    for (i;i<dwlen;i++) 
    {
        swprintf_s(buf, L"%02x", pGUID[i]);
        wcscat_s(szGUID, MAX_PATH,buf);
    }
}

//  Entry point for application
int main(int argc, char* argv[])
{
    DWORD dwStat;
    ULONG ulLength;
    UCHAR *pCookie;
    WCHAR szDCName[MAX_PATH];
    HRESULT hr;

    if (argc==1) 
    {
        //  Perform a full synchronization.
        //  Initialize the synchronization parameters to zero or NULL.
        wprintf(L"Performing a full sync.\n");
        szDCName[0] = '\0';
        ulLength = 0;
        pCookie = NULL;
    } 
    else
    {
        //  Perform an incremental synchronization.
        //  Initialize synchronization parameters from storage.
        wprintf(L"Retrieving changes only.\n");
        dwStat = GetCookieAndDCfromStorage(&pCookie, &ulLength, szDCName);
        if (dwStat != NO_ERROR) 
        {
            wprintf(L"Could not get the cookie: %u\n", dwStat);
            goto cleanup;
        }
    }

    //  Perform the search and update the synchronization parameters.
    hr = DoDirSyncSearch(L"(objectClass=user)",
                         NULL,       //  Retrieve all attributes.
                         -1, 
                         &pCookie, 
                         &ulLength,
                         szDCName);
    if (FAILED(hr)) 
    {
        wprintf(L"DoDirSyncSearch failed: 0x%x\n", hr);
        goto cleanup;
    }

    //  Cache the returned synchronization parameters in storage.
    wprintf(L"Caching the synchronization parameters.\n");
    dwStat = WriteCookieAndDCtoStorage(pCookie, ulLength, szDCName);
    if (dwStat != NO_ERROR) 
    {
        wprintf(L"Could not cache the cookie: %u\n", dwStat);
        goto cleanup;
    }

cleanup:
    if (pCookie)
        GlobalFree (pCookie);
    return 1;
}
```



 

 
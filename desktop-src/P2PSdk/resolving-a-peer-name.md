---
description: Questo argomento illustra i metodi per la risoluzione di un nome peer usando le API del provider dello spazio dei nomi PNRP.
ms.assetid: 7b21ec52-bc29-447e-9c46-34b9115574e0
title: Risoluzione di un nome di peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7f3aa59d3dc3be89f35ce9d6eca58bed1ce137
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883649"
---
# <a name="resolving-a-peer-name"></a>Risoluzione di un nome di peer

Questo argomento illustra i metodi per la risoluzione di un nome peer usando le API del provider dello spazio dei nomi PNRP.

Quando si risolve un nome peer, è necessario fornire le seguenti informazioni:

-   [Nome peer](peer-names.md)
-   [Criteri di risoluzione](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)
-   Nome del cloud in cui risolvere il nome peer
-   Indirizzo IP, facoltativo e utilizzato come hint

## <a name="resolving-a-peer-name"></a>Risoluzione di un nome di peer

Dopo aver fornito un nome peer, i criteri di risoluzione, il nome del cloud e l'indirizzo IP facoltativo, è necessario eseguire i passaggi seguenti per completare la risoluzione di un nome peer:

-   Chiamare [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) per avviare il processo e restituire un handle.
-   Chiamare [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) per risolvere il nome peer.
-   Chiamare [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) per completare il processo.

## <a name="an-example-of-resolving-a-peer-name"></a>Esempio di risoluzione di un nome peer

Il frammento di codice seguente illustra come risolvere un nome peer. Nell'esempio si presuppone che venga restituito un indirizzo TCP/IP.


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment( lib, "ws2_32.lib")

// Function: PnrpResolve
//
// Purpose:  Resolve the given name within a PNRP cloud
//
// Arguments:
//   pwzName  : name to resolve in PNRP, generally the graph id
//   pwzCloud : name of cloud to resolve in, NULL = global cloud
//   pAddr    : pointer to result buffer
//
// Returns:  HRESULT
//
HRESULT PnrpResolve(PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddr)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    WSAQUERYSET*    pResults = NULL;
    WSAQUERYSET     tempResultSet = {0};
    HANDLE          hLookup = NULL;
    BOOL            fFound = FALSE;
    DWORD           dwError;
    INT             iRet;
    ULONG           i;
    DWORD           dwSize = 0;

    //
    // fill in the WSAQUERYSET
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.nMaxResolve = 1;
    pnrpInfo.dwTimeout = 30;
    pnrpInfo.enResolveCriteria = PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;
    // start resolve
    iRet = WSALookupServiceBegin(
            &querySet,
            LUP_RETURN_NAME | LUP_RETURN_ADDR | LUP_RETURN_COMMENT,
            &hLookup);


    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    if (SUCCEEDED(hr))
    {
        dwSize = sizeof(tempResultSet);

        // retrieve the required size
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, &tempResultSet);
        dwError = WSAGetLastError();

        if (dwError == WSAEFAULT)
        {
            // allocate space for the results
            pResults = (WSAQUERYSET*)malloc(dwSize);
            if (pResults == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }
        else
        {
            hr = HRESULT_FROM_WIN32(dwError);
        }
    }

    if (SUCCEEDED(hr))
    {
        // retrieve the addresses
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, pResults);
        if (iRet != 0)
        {
            hr = HRESULT_FROM_WIN32(WSAGetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // return the first IPv6 address found
        for (i = 0; i < pResults->dwNumberOfCsAddrs; i++)
        {
            if (pResults->lpcsaBuffer[i].iProtocol == IPPROTO_TCP &&
                pResults->lpcsaBuffer[i].RemoteAddr.iSockaddrLength == sizeof(SOCKADDR_IN6))
            {
                CopyMemory(pAddr, pResults->lpcsaBuffer[i].RemoteAddr.lpSockaddr, sizeof(SOCKADDR_IN6));
                fFound = TRUE;
                break;
            }
        }

        if (!fFound)
        {
            // unable to find an IPv6 address
            hr = HRESULT_FROM_WIN32(WSA_E_NO_MORE);
        }
    }

    if (hLookup != NULL)
    {
        WSALookupServiceEnd(hLookup);
    }

    if (pResults != NULL)
    {
        free(pResults);
    }

    return hr;
}
```



 

 




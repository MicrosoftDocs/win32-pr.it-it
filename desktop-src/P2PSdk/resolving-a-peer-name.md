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
# <a name="resolving-a-peer-name"></a><span data-ttu-id="e69a3-103">Risoluzione di un nome di peer</span><span class="sxs-lookup"><span data-stu-id="e69a3-103">Resolving a Peer Name</span></span>

<span data-ttu-id="e69a3-104">Questo argomento illustra i metodi per la risoluzione di un nome peer usando le API del provider dello spazio dei nomi PNRP.</span><span class="sxs-lookup"><span data-stu-id="e69a3-104">This topic discusses methods for resolving a peer name using the PNRP Namespace Provider APIs.</span></span>

<span data-ttu-id="e69a3-105">Quando si risolve un nome peer, è necessario fornire le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="e69a3-105">When you resolve a peer name, you must provide the following information:</span></span>

-   [<span data-ttu-id="e69a3-106">Nome peer</span><span class="sxs-lookup"><span data-stu-id="e69a3-106">Peer name</span></span>](peer-names.md)
-   [<span data-ttu-id="e69a3-107">Criteri di risoluzione</span><span class="sxs-lookup"><span data-stu-id="e69a3-107">Resolve criteria</span></span>](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)
-   <span data-ttu-id="e69a3-108">Nome del cloud in cui risolvere il nome peer</span><span class="sxs-lookup"><span data-stu-id="e69a3-108">Cloud name in which to resolve the peer name</span></span>
-   <span data-ttu-id="e69a3-109">Indirizzo IP, facoltativo e utilizzato come hint</span><span class="sxs-lookup"><span data-stu-id="e69a3-109">IP address, which is optional and is used as a hint</span></span>

## <a name="resolving-a-peer-name"></a><span data-ttu-id="e69a3-110">Risoluzione di un nome di peer</span><span class="sxs-lookup"><span data-stu-id="e69a3-110">Resolving a Peer Name</span></span>

<span data-ttu-id="e69a3-111">Dopo aver fornito un nome peer, i criteri di risoluzione, il nome del cloud e l'indirizzo IP facoltativo, è necessario eseguire i passaggi seguenti per completare la risoluzione di un nome peer:</span><span class="sxs-lookup"><span data-stu-id="e69a3-111">After you provide a peer name, resolve criteria, cloud name, and the optional IP address, the following steps must be taken to complete the resolution of a peer name:</span></span>

-   <span data-ttu-id="e69a3-112">Chiamare [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) per avviare il processo e restituire un handle.</span><span class="sxs-lookup"><span data-stu-id="e69a3-112">Call [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) to begin the process and return a handle.</span></span>
-   <span data-ttu-id="e69a3-113">Chiamare [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) per risolvere il nome peer.</span><span class="sxs-lookup"><span data-stu-id="e69a3-113">Call [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) to resolve the peer name.</span></span>
-   <span data-ttu-id="e69a3-114">Chiamare [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) per completare il processo.</span><span class="sxs-lookup"><span data-stu-id="e69a3-114">Call [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) to complete the process.</span></span>

## <a name="an-example-of-resolving-a-peer-name"></a><span data-ttu-id="e69a3-115">Esempio di risoluzione di un nome peer</span><span class="sxs-lookup"><span data-stu-id="e69a3-115">An Example of Resolving a Peer Name</span></span>

<span data-ttu-id="e69a3-116">Il frammento di codice seguente illustra come risolvere un nome peer.</span><span class="sxs-lookup"><span data-stu-id="e69a3-116">The following code snippet shows you how to resolve a peer name.</span></span> <span data-ttu-id="e69a3-117">Nell'esempio si presuppone che venga restituito un indirizzo TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e69a3-117">There is an assumption in the sample that a TCP/IP address will be returned.</span></span>


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



 

 




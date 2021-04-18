---
description: Quando si enumerano i cloud, un'applicazione deve fornire l'ambito della ricerca di cloud. Una volta identificato l'ambito, l'applicazione può avviare il processo di enumerazione.
ms.assetid: efd16cca-ac63-4bfa-bc6c-d7465cc374ee
title: Enumerazione dei cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f958a2cc958c10bd85e674b43a3b41354fc344c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312283"
---
# <a name="enumerating-clouds"></a>Enumerazione dei cloud

Quando si enumerano i cloud, un'applicazione deve fornire l'ambito della ricerca di cloud. Una volta identificato l'ambito, l'applicazione può avviare il processo di enumerazione.

Nella procedura riportata di seguito vengono identificate le chiamate che devono essere effettuate per enumerare i cloud.

**Per enumerare i cloud**

1.  Chiamare [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) per avviare il processo e restituire un handle.
2.  Chiamare [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) per recuperare un set di cloud, quindi chiamare questa funzione fino a quando l'applicazione non recupera tutti i cloud.
3.  Chiamare [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) per completare l'enumerazione.

## <a name="example-enumerating-and-printing-the-names-of-available-link-local-clouds"></a>Esempio: enumerazione e stampa dei nomi dei cloud locali per i collegamenti disponibili


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "ws2_32.lib")

DWORD PrintLinkLocalClouds()
{

    WSAQUERYSETW    qset;
    BLOB            Blob;
    PNRPCLOUDINFO   CloudInfo;
    HANDLE          hLookup = NULL;
    int             err;
    DWORD           dwErr = NO_ERROR;
    DWORD           dwSize;
    WSAQUERYSETW    *pResults = NULL;

    ZeroMemory(&qset, sizeof(qset));
    ZeroMemory(&CloudInfo, sizeof(CloudInfo));

    CloudInfo.dwSize = sizeof(PNRPCLOUDINFO);
    CloudInfo.Cloud.Scope = PNRP_LINK_LOCAL_SCOPE;

    Blob.cbSize = sizeof(PNRPCLOUDINFO);
    Blob.pBlobData = (LPBYTE)&CloudInfo;

    qset.dwSize = sizeof(WSAQUERYSET);
    qset.dwNameSpace = NS_PNRPCLOUD;
    qset.lpServiceClassId = (LPGUID)&SVCID_PNRPCLOUD;
    qset.lpBlob = &Blob;

    //
    // Start enumeration
    //
    err = WSALookupServiceBegin(
            &qset,
            LUP_RETURN_NAME,
            &hLookup);
                
    if(err !=0)
    {
        return WSAGetLastError();
    }

    // getting results
    while(TRUE)
    {

        //
        // Get size
        //
        ZeroMemory(&qset, sizeof(qset));
        dwSize = sizeof(qset);

        pResults = &qset;

        err = WSALookupServiceNext(
                hLookup,
                0,
                &dwSize,
                pResults
                );
        if(err != 0)
        {
            dwErr = WSAGetLastError();
        }

        if(dwErr != NO_ERROR)
        {
            if(dwErr == WSA_E_NO_MORE)
            {
                //
                // No more entries
                //
                dwErr = ERROR_SUCCESS;
                break;
            }
            else if (dwErr == WSAEFAULT)
            {
                //
                // This usually means result buffer too small. Allocate space
                //
                pResults = (WSAQUERYSET *)malloc(dwSize);
                if(pResults == NULL)
                {
                    dwErr = ERROR_OUTOFMEMORY;
                    break;
                }

                //
                // Get cloud name
                //
                err = WSALookupServiceNext(
                        hLookup,
                        0,
                        &dwSize,
                        pResults
                        );
                if(err == 0)
                {
                    wprintf(L"%s\n", pResults->lpszServiceInstanceName);

                    dwErr = NO_ERROR;
                }
                else
                {
                    dwErr = WSAGetLastError();
                }

                free(pResults);

                if(dwErr != NO_ERROR)
                {
                    break;
                }
            }
            else
            {
                //
                // Some other unexpected error
                //
                break;
            }
        }
        else
        {
            //
            // Should never happen
            //
            dwErr = ERROR_GEN_FAILURE;
            break;
        }
    }

    //
    // Close the enumeration
    //
    WSALookupServiceEnd(hLookup);
                
    return dwErr;
}
```



 

 




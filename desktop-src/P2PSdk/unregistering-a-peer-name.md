---
description: Quando si annulla la registrazione di un nome peer, viene rimosso un nome registrato da un Cloud PNRP (Peer Name Resolution Protocol).
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Annullamento della registrazione di un nome peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd482cc9cfd8c32d7bc95edd00e866e2d87b7a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967530"
---
# <a name="unregistering-a-peer-name"></a>Annullamento della registrazione di un nome peer

Quando si annulla la registrazione di un nome peer, viene rimosso un nome registrato da un Cloud PNRP (Peer Name Resolution Protocol).

## <a name="unregistering-a-peer-name"></a>Annullamento della registrazione di un nome peer

Per annullare la registrazione di un nome peer, chiamare [**WSASetService**](pnrp-and-wsasetservice.md). Il valore del parametro *essOperation* deve essere **RNRSERVICE \_ Delete**. Usare le linee guida riportate nelle sezioni seguenti di questo argomento per apportare le configurazioni necessarie ai parametri **WSASetService** e alla struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .

## <a name="configuring-wsasetservice"></a>Configurazione di WSASetService

Quando un'applicazione chiama [**WSASetService**](pnrp-and-wsasetservice.md), i parametri devono essere configurati in base alle specifiche seguenti:

-   il valore di *essOperation* deve essere **RNRSERVICE \_ Delete**.
-   *dwFlags* deve essere zero (0).
-   *lpqsRegInfo* deve puntare a una struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , che deve essere configurata utilizzando le linee guida riportate nella sezione seguente di questo argomento.

## <a name="configuring-wsaqueryset"></a>Configurazione di WSAQUERYSET

La struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve essere configurata in base alle specifiche seguenti:

-   **dwSize** deve specificare la dimensione della struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .
-   **lpszServiceInstanceName** deve puntare al nome peer di cui viene annullata la registrazione.
-   **lpBlob** deve puntare a una struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **lpcsaBuffer** deve puntare all'elenco indirizzi.

> [!Note]  
> I membri rimanenti sono descritti in [**PNRP e WSASetService**](pnrp-and-wsasetservice.md).

 

## <a name="an-example-of-unregistering-a-peer-name"></a>Esempio di annullamento della registrazione di un nome peer

Il frammento di codice seguente illustra come annullare la registrazione di un nome peer fornendo le informazioni corrette quando si chiama [**WSASetService**](pnrp-and-wsasetservice.md) usando la struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 




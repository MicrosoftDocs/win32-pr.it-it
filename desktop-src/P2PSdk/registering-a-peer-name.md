---
description: "Per registrare un nome peer, un'applicazione deve fornire le informazioni seguenti: indirizzo IP listPeer identityPeer nameIf un nome peer non è protetto, un'identità è facoltativa."
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Registrazione di un nome peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0944c4a41c02ff221aa1cc6a0b84ed881a9453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315444"
---
# <a name="registering-a-peer-name"></a>Registrazione di un nome peer

Per registrare un nome peer, un'applicazione deve fornire le seguenti informazioni:

-   Elenco indirizzi IP
-   [Identità peer](creating-a-peer-identity.md)
-   [Nome peer](peer-names.md)

Se un nome peer non è protetto, un'identità è facoltativa. Se un'identità peer viene specificata come **null**, il protocollo PNRP (Peer Name Resolution Protocol) usa un'identità peer predefinita interna.

## <a name="registering-a-peer-name"></a>Registrazione di un nome peer

Dopo aver identificato l'elenco di indirizzi IP, l'identità peer e il nome peer, l'applicazione può registrare un nome peer chiamando [**WSASetService**](pnrp-and-wsasetservice.md). Usare le linee guida riportate nelle sezioni seguenti di questo argomento per apportare le configurazioni necessarie ai parametri **WSASetService** e alla struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .

### <a name="configuring-wsasetservice"></a>Configurazione di WSASetService

Quando un'applicazione chiama [**WSASetService**](pnrp-and-wsasetservice.md), i parametri devono essere configurati in base alle specifiche seguenti:

-   il valore di *essOperation* deve essere **RNRSERVICE \_ Register**.
-   *dwFlags* deve essere zero (0).
-   *lpqsRegInfo* deve puntare a una struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , che deve essere configurata usando le linee guida riportate nella sezione **configurazione di WSAQUERYSET** seguente di questo argomento.

### <a name="configuring-wsaqueryset"></a>Configurazione di WSAQUERYSET

La struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve essere configurata in base alle specifiche seguenti:

-   **dwSize** deve specificare la dimensione della struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .
-   **lpszServiceInstanceName** deve puntare al nome peer registrato.
-   **lpBlob** deve puntare a una struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **lpcsaBuffer** deve puntare all'elenco indirizzi.

> [!Note]  
> I membri rimanenti sono descritti in [**PNRP e WSASetService**](pnrp-and-wsasetservice.md).

 

Dopo la registrazione di un nome peer, le informazioni sono disponibili per l'infrastruttura peer. Tuttavia, si verifica un ritardo tra l'ora di registrazione e la propagazione delle informazioni di registrazione ad altri nodi. Durante questo periodo, gli altri nodi potrebbero non essere in grado di risolvere il peer appena registrato.

## <a name="example-of-registering-a-peer-name"></a>Esempio di registrazione di un nome peer

Il frammento di codice seguente illustra come registrare un nome peer fornendo le informazioni corrette quando si chiama [**WSASetService**](pnrp-and-wsasetservice.md) usando la struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 




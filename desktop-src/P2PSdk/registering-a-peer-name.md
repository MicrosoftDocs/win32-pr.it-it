---
description: Per registrare un nome peer, un'applicazione deve fornire le informazioni seguenti:elenco di indirizzi IPIdentitè del peerNomio peerSe un nome peer non è protetto, un'identità è facoltativa.
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Registrazione di un nome peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcedbe3e405e21ec9709289e8a9237179703b1b8e81f40b449479373524beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011489"
---
# <a name="registering-a-peer-name"></a>Registrazione di un nome peer

Per registrare un nome peer, un'applicazione deve fornire le informazioni seguenti:

-   Elenco di indirizzi IP
-   [Identità peer](creating-a-peer-identity.md)
-   [Nome peer](peer-names.md)

Se un nome peer non è protetto, un'identità è facoltativa. Se un'identità peer viene specificata **come NULL,** il Peer Name Resolution Protocol (PNRP) usa un'identità peer predefinita interna.

## <a name="registering-a-peer-name"></a>Registrazione di un nome peer

Dopo aver identificato l'elenco di indirizzi IP, l'identità peer e il nome peer, l'applicazione può registrare un nome peer chiamando [**WSASetService.**](pnrp-and-wsasetservice.md) Utilizzare le linee guida nelle sezioni seguenti di questo argomento per impostare le configurazioni necessarie per i parametri **WSASetService** e la [**struttura WSAQUERYSET.**](pnrp-and-wsaqueryset.md)

### <a name="configuring-wsasetservice"></a>Configurazione di WSASetService

Quando un'applicazione [**chiama WSASetService,**](pnrp-and-wsasetservice.md)i parametri devono essere configurati in base alle specifiche seguenti:

-   *essOperation* deve avere un valore **di RNRSERVICE \_ REGISTER**.
-   *dwFlags* deve essere zero (0).
-   *lpqsRegInfo* deve puntare a una struttura [**WSAQUERYSET,**](pnrp-and-wsaqueryset.md) che deve essere configurata usando le linee guida riportate nella sezione Configurazione **di WSAQUERYSET** di questo argomento.

### <a name="configuring-wsaqueryset"></a>Configurazione di WSAQUERYSET

La [**struttura WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve essere configurata in base alle specifiche seguenti:

-   **dwSize** deve specificare le dimensioni della [**struttura WSAQUERYSET.**](pnrp-and-wsaqueryset.md)
-   **lpszServiceInstanceName** deve puntare al nome peer registrato.
-   **lpBlob** deve puntare a una [**struttura PNRPINFO.**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
-   **lpcsaBuffer** deve puntare all'elenco di indirizzi.

> [!Note]  
> I membri rimanenti sono descritti in [**PNRP e WSASetService.**](pnrp-and-wsasetservice.md)

 

Dopo la registrazione di un nome peer, le informazioni sono disponibili per l'infrastruttura peer. Tuttavia, si verifica un ritardo tra l'ora di registrazione e la propagazione delle informazioni di registrazione ad altri nodi. Durante questo periodo, altri nodi potrebbero non essere in grado di risolvere il peer appena registrato.

## <a name="example-of-registering-a-peer-name"></a>Esempio di registrazione di un nome peer

Il frammento di codice seguente illustra come registrare un nome peer fornendo le informazioni corrette quando si chiama [**WSASetService**](pnrp-and-wsasetservice.md) usando la [**struttura WSAQUERYSET.**](pnrp-and-wsaqueryset.md)


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



 

 




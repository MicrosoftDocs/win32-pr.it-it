---
description: "L'API del provider dello spazio dei nomi PNRP usa le strutture seguenti:"
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Strutture PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e275dff1b0c0986cfa998ed64cfb1ffad5b19af400f8719715d2106af353d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011529"
---
# <a name="pnrp-structures"></a>Strutture PNRP

L'API del provider dello spazio dei nomi PNRP usa le strutture seguenti:



| Struttura                                                             | Descrizione                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PEER \_ PNRP \_ ENDPOINT \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | Contiene gli indirizzi IP e i dati associati a un endpoint peer.                                                                                                 |
| [**PEER \_ PNRP \_ CLOUD \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | Contiene informazioni su un cloud Peer Name Resolution Protocol (PNRP).                                                                                            |
| [**INFORMAZIONI \_ DI REGISTRAZIONE PNRP \_ \_ PEER**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | Contiene le informazioni fornite da un'identità peer durante la registrazione in un cloud PNRP.                                                                           |
| [PNRP e BLOB](pnrp-and-blob.md)                                    | Passa i dati alla [**struttura WSAQUERYSET**](winsock-nsp-reference-links.md) durante le chiamate a diverse funzioni.                                                  |
| [PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)                      | Facilita la risoluzione dei nomi e l'enumerazione di nomi e cloud.                                                                                         |
| [**PNRP \_ CLOUD \_ ID**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | Contiene i valori che definiscono un cloud di rete.                                                                                                                    |
| [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | A cui punta il **membro lpBlob** della [**struttura WSAQUERYSET.**](winsock-nsp-reference-links.md)                                                            |
| [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | A cui punta il **membro lpBlob** della [**struttura WSAQUERYSET**](winsock-nsp-reference-links.md)                                                             |
| [**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | A cui punta il **membro lpBlob** della [**struttura WSAQUERYSET**](winsock-nsp-reference-links.md) e fornisce supporto per dati opachi specifici dell'applicazione. |



 

 

 

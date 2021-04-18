---
description: "L'API del provider dello spazio dei nomi PNRP usa le strutture seguenti:"
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Strutture PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312227"
---
# <a name="pnrp-structures"></a>Strutture PNRP

L'API del provider dello spazio dei nomi PNRP usa le strutture seguenti:



| Struttura                                                             | Descrizione                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ informazioni endpoint PNRP \_ peer**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | Contiene gli indirizzi IP e i dati associati a un endpoint peer.                                                                                                 |
| [**\_informazioni sul \_ cloud \_ PNRP peer**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | Contiene informazioni su un Cloud PNRP (Peer Name Resolution Protocol).                                                                                            |
| [**\_informazioni di \_ registrazione \_ PNRP peer**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | Contiene le informazioni fornite da un'identità peer quando viene registrato con un Cloud PNRP.                                                                           |
| [PNRP e BLOB](pnrp-and-blob.md)                                    | Passa i dati alla struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) durante le chiamate a diverse funzioni.                                                  |
| [PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)                      | Semplifica la risoluzione dei nomi e l'enumerazione di nomi e cloud.                                                                                         |
| [**\_ID Cloud \_ PNRP**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | Contiene i valori che definiscono un cloud di rete.                                                                                                                    |
| [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | A cui fa riferimento il membro **lpBlob** della struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) .                                                            |
| [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | A cui fa riferimento il membro **lpBlob** della struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md)                                                             |
| [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | A cui fa riferimento il membro **lpBlob** della struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) e fornisce il supporto per i dati opachi specifici dell'applicazione. |



 

 

 

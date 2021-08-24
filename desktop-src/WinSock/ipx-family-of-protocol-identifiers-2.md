---
description: Il parametro del protocollo in socket e WSASocket è un identificatore che stabilisce un tipo di rete e un metodo per identificare i vari protocolli di trasporto eseguiti sulla rete.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Famiglia IPX di identificatori di protocollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549e1dbdb9d379e87ed8e22871188b0b7762e924a695721f1c860fce14f2a2e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733651"
---
# <a name="ipx-family-of-protocol-identifiers"></a>Famiglia IPX di identificatori di protocollo

Il *parametro* del protocollo in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) è un identificatore che stabilisce un tipo di rete e un metodo per identificare i vari protocolli di trasporto eseguiti sulla rete. A differenza di IP, IPX non usa un singolo valore di protocollo per la selezione di uno stack di trasporto. Poiché non è necessario che la rete usi un valore specifico per ogni protocollo di trasporto, è possibile assegnarli in modo pratico per le applicazioni Winsock. Si evitano valori da 0 a 255 per evitare conflitti con i valori del protocollo INET PF \_ corrispondenti.



| Nome         | Valore       | Tipi di socket              | Descrizione                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| Riservato     | 0-255       |                           | Riservato per i valori del \_ protocollo INET PF.              |
| NSPROTO \_ IPX | 1000 - 1255 | SOCK \_ DGRAM SOCK \_ RAW     | Servizio datagrammi per IPX.                           |
| NSPROTO \_ SPX | 1256        | SOCK \_ STREAM SOCK \_ SEQPKT | Scambio di pacchetti affidabile tramite pacchetti di dimensioni fisse. |



 

> [!Note]  
> Quando si specifica NSPROTO SPX, il protocollo SPX II viene utilizzato automaticamente se entrambi gli endpoint sono in grado \_ di eseguire questa operazione.

 

 

 




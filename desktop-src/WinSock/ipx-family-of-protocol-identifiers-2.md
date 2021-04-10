---
description: Il parametro del protocollo in socket e WSASocket è un identificatore che stabilisce un tipo di rete e un metodo per identificare i vari protocolli di trasporto eseguiti sulla rete.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Famiglia di identificatori di protocollo IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129166"
---
# <a name="ipx-family-of-protocol-identifiers"></a>Famiglia di identificatori di protocollo IPX

Il parametro del *protocollo* in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) è un identificatore che stabilisce un tipo di rete e un metodo per identificare i vari protocolli di trasporto eseguiti sulla rete. A differenza di IP, IPX non usa un singolo valore di protocollo per la selezione di uno stack di trasporto. Poiché non esiste alcun requisito di rete per usare un valore specifico per ogni protocollo di trasporto, è possibile assegnarli in modo appropriato per le applicazioni Winsock. Si evitano i valori da 0 a 255 per evitare conflitti con i valori del \_ protocollo di PF inet corrispondenti.



| Nome         | Valore       | Tipi di socket              | Descrizione                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| Riservato     | 0-255       |                           | Riservato per \_ i valori del protocollo di PF inet.              |
| NSPROTO \_ IPX | 1000-1255 | SOCK \_ DGRAM Sock \_ RAW     | Servizio datagramma per IPX.                           |
| \_SPX NSPROTO | 1256        | Sock \_ Stream Sock \_ SEQPKT | Scambio di pacchetti affidabili con pacchetti a dimensione fissa. |



 

> [!Note]  
> Quando \_ si specifica NSPROTO SPX, il protocollo SPX II viene usato automaticamente se entrambi gli endpoint sono in grado di eseguire questa operazione.

 

 

 




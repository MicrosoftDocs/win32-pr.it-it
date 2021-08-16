---
description: In questa sezione viene descritta l'implementazione del protocollo multicast Pragma General Multicast (PGM) in Windows, spesso definita reliable multicast. Reliable Multicast viene implementato tramite Windows Socket in Windows Server 2003 e versioni successive.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programmazione multicast affidabile (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c34365bdc8db553d24182fcb193dc03177627ccf9b00a03f309ab4cf7bbe01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559953"
---
# <a name="reliable-multicast-programming-pgm"></a>Programmazione multicast affidabile (PGM)

In questa sezione viene descritta l'implementazione del protocollo multicast Pragma General Multicast (PGM) in Windows, spesso definita reliable multicast. Reliable Multicast viene implementato tramite Windows Socket in Windows Server 2003 e versioni successive.

**Windows XP:** PGM è supportato solo quando Microsoft Message Queuing (MSMQ) 3.0 è installato.

PGM è un protocollo multicast affidabile e scalabile che consente ai ricevitori di rilevare la perdita, richiedere la ritrasmissione dei dati persi o notificare a un'applicazione la perdita irreversibile. PGM è un protocollo affidabile dal ricevitore, il che significa che il ricevitore è responsabile della ricezione di tutti i dati, assolvendo il mittente della responsabilità della ricezione.

PGM è appropriato per le applicazioni che richiedono il recapito di dati multicast senza duplicati da più origini a più ricevitori. La PGM non supporta il recapito riconosciuto né garantisce l'ordinamento dei pacchetti da più mittenti.

Per altre informazioni sulla PGM, vedere RFC 3208 disponibile [all'indirizzo www.ietf.org](https://www.ietf.org/).

Questa sezione descrive come usare reliable multicast in Windows. Negli argomenti seguenti vengono illustrati i vari aspetti della creazione di un'applicazione multicast affidabile Windows Socket:

-   [Mittenti e ricevitori PGM](pgm-senders-and-receivers.md)
-   [Opzioni del mittente PGM](pgm-sender-options.md)
-   [Invio e ricezione di dati PGM](sending-and-receiving-pgm-data.md)
-   [Multihoming e PGM](multihoming-and-pgm.md)
-   [Opzioni socket PGM](pgm-socket-options.md)

 

 




---
description: In questa sezione viene descritta l'implementazione del protocollo multicast PGM (Pragmatic General Multicast) in Windows, spesso definita multicast affidabile. Il multicast affidabile viene implementato tramite Windows Sockets in Windows Server 2003 e versioni successive.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programmazione multicast affidabile (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310452"
---
# <a name="reliable-multicast-programming-pgm"></a>Programmazione multicast affidabile (PGM)

In questa sezione viene descritta l'implementazione del protocollo multicast PGM (Pragmatic General Multicast) in Windows, spesso definita multicast affidabile. Il multicast affidabile viene implementato tramite Windows Sockets in Windows Server 2003 e versioni successive.

**Windows XP:** Il protocollo PGM è supportato solo quando è installato Microsoft Message Queuing (MSMQ) 3,0.

PGM è un protocollo multicast affidabile e scalabile che consente ai destinatari di rilevare la perdita, richiedere la ritrasmissione di dati persi o notificare a un'applicazione una perdita irreversibile. PGM è un protocollo ricevitore-affidabile, che indica che il ricevitore è responsabile di garantire la ricezione di tutti i dati, assolvere il mittente della responsabilità della ricezione.

PGM è adatto per le applicazioni che richiedono il recapito di dati multicast senza duplicazione da più origini a più ricevitori. Il protocollo PGM non supporta il recapito riconosciuto né garantisce l'ordine dei pacchetti da più mittenti.

Per ulteriori informazioni su PGM, vedere la specifica RFC 3208 disponibile all'indirizzo [www.ietf.org](https://www.ietf.org/).

Questa sezione descrive come usare Reliable Multicast in Windows. Negli argomenti seguenti vengono illustrati i vari aspetti della creazione di un'applicazione multicast affidabile mediante Windows Sockets:

-   [Mittenti e ricevitori PGM](pgm-senders-and-receivers.md)
-   [Opzioni mittente PGM](pgm-sender-options.md)
-   [Invio e ricezione di dati PGM](sending-and-receiving-pgm-data.md)
-   [Multihoming e PGM](multihoming-and-pgm.md)
-   [Opzioni socket PGM](pgm-socket-options.md)

 

 




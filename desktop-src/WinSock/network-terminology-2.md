---
description: Le metriche vengono usate per misurare gli aspetti delle prestazioni di rete e protocollo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminologia di rete (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751418"
---
# <a name="network-terminology-windows-sockets-2"></a>Terminologia di rete (Windows Sockets 2)

Le metriche vengono usate per misurare gli aspetti delle prestazioni di rete e protocollo. I valori di tali metriche in diversi scenari indicano il livello di prestazioni di un'applicazione di rete. Questa sezione definisce i termini e le metriche usati a livello di settore per misurare le prestazioni delle applicazioni di rete. Questi termini vengono usati nel resto di questa guida.

-   Tempo di round trip (RTT)

    Tempo, in millisecondi, per cui una richiesta di eseguire un viaggio da un computer di origine a un computer di destinazione e viceversa. I valori più bassi indicano prestazioni migliori. I tempi di avanzamento e di ritorno del percorso non sono necessariamente uguali.

    I valori RTT sono interessati dall'infrastruttura di rete, dalla distanza tra i nodi, dalle condizioni della rete e dalle dimensioni del pacchetto. Dimensioni del pacchetto, congestione e compressione del payload che incidono su RTT se misurato su collegamenti lenti, ad esempio connessioni remote. Altri fattori influiscono sull'RTT, inclusa la correzione degli errori in diretta e la compressione dei dati, che introducono buffer e code che aumentano RTT e pertanto diminuiscono le prestazioni.

-   Goodput

    Misura dei dati di applicazione utili elaborati correttamente dal ricevitore, in bit al secondo. Goodput consente di misurare la velocità effettiva effettiva o utile e include solo i dati dell'applicazione. il pacchetto, il protocollo e le intestazioni multimediali sono considerati sovraccarico e non fanno parte di goodput.

-   Overhead del protocollo

    Byte non applicazione, inclusi il protocollo e il frame multimediale, divisi per il numero totale di byte trasmessi. Il valore è espresso come percentuale. Valori più elevati indicano prestazioni più ridotte.

    Il sovraccarico viene calcolato per entrambe le direzioni in questa guida, ma può essere calcolato separatamente per ogni direzione.

-   Prodotto Bandwidth-Delay

    Prodotto della larghezza di banda di bit al secondo della rete e RTT (in secondi). Questo valore equivale al numero di bit necessari per riempire la larghezza di banda di rete disponibile. Quando il valore per il ritardo della larghezza di banda è elevato, lo stack TCP/IP deve gestire grandi quantità di dati non riconosciuti per garantire la completa pipeline. Il prodotto con ritardo della larghezza di banda è una metrica end-to-end chiave per le applicazioni di streaming.

 

 




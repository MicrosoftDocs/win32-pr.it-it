---
description: Le metriche vengono usate per misurare gli aspetti delle prestazioni di rete e protocollo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminologia della rete (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d0c5fc67932b5c756ae52b9a7ffefef0f18c2728f2b2773de3741d0e5b7d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794771"
---
# <a name="network-terminology-windows-sockets-2"></a>Terminologia della rete (Windows Sockets 2)

Le metriche vengono usate per misurare gli aspetti delle prestazioni di rete e protocollo. I valori per tali metriche in diversi scenari indicano il livello di prestazioni di un'applicazione di rete. Questa sezione definisce i termini e le metriche usati a livello di settore per misurare le prestazioni delle applicazioni di rete. Questi termini vengono usati nella parte restante di questa guida.

-   Tempo di round trip (RTT)

    Tempo, in millisecondi, per una richiesta di esecuzione di un viaggio da un computer di origine a un computer di destinazione e di nuovo. Valori inferiori indicano prestazioni migliori. Gli orari dei percorsi in avanti e restituiti non sono necessariamente uguali.

    I valori RTT sono interessati dall'infrastruttura di rete, dalla distanza tra i nodi, dalle condizioni di rete e dalle dimensioni dei pacchetti. Dimensioni dei pacchetti, congestione e comprimibilità del payload influiscono su RTT se misurate su collegamenti lenti, ad esempio connessioni remote. Altri fattori influiscono su RTT, tra cui la correzione degli errori in avanti e la compressione dei dati, che introducono buffer e code che aumentano RTT e quindi riducono le prestazioni.

-   Goodput

    Misura dei dati utili dell'applicazione elaborati correttamente dal ricevitore, in bit al secondo. Goodput consente la misurazione della velocità effettiva efficace o utile e include solo i dati dell'applicazione. il pacchetto, il protocollo e le intestazioni multimediali sono considerati sovraccarico e non fanno parte di goodput.

-   Sovraccarico del protocollo

    Byte non applicazione, inclusi il protocollo e il frame multimediale, divisi per il numero totale di byte trasmessi. Il valore è espresso come percentuale. Valori più elevati indicano prestazioni più scarse.

    L'overhead viene calcolato per entrambe le direzioni in questa guida, ma può essere calcolato separatamente per ogni direzione.

-   Bandwidth-Delay prodotto

    Prodotto della larghezza di banda in bit al secondo della rete e del valore RTT (in secondi). Questo valore equivale al numero di bit necessari per riempire la larghezza di banda di rete disponibile. Quando il valore per il prodotto con ritardo della larghezza di banda è elevato, lo stack TCP/IP deve gestire grandi quantità di dati non contrassegnati per mantenere piena la pipeline. Il prodotto con ritardo della larghezza di banda è una metrica end-to-end chiave per le applicazioni di streaming.

 

 




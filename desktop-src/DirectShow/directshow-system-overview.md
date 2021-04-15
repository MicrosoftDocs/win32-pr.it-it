---
description: Panoramica del sistema DirectShow
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Panoramica del sistema DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520586"
---
# <a name="directshow-system-overview"></a>Panoramica del sistema DirectShow

**Sfida dei contenuti multimediali**

L'uso dei contenuti multimediali presenta diverse principali problemi:

-   I flussi multimediali contengono grandi quantità di dati, che devono essere elaborati molto rapidamente.
-   Audio e video devono essere sincronizzati in modo che vengano avviati e arrestati allo stesso tempo e riproducano alla stessa velocità.
-   I dati possono provenire da molte origini, tra cui file locali, reti di computer, trasmissioni televisive e videocamere.
-   I dati sono disponibili in diversi formati, ad esempio Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG) e Digital video (DV).
-   Il programmatore non sa in anticipo quali dispositivi hardware saranno presenti nel sistema dell'utente finale.

**Soluzione DirectShow**

DirectShow è progettato per risolvere ognuno di questi problemi. Il principale obiettivo di progettazione consiste nel semplificare l'attività di creazione di applicazioni multimediali digitali sulla piattaforma Windows, isolando le applicazioni dalle complessità dei trasporti di dati, le differenze hardware e la sincronizzazione.

Per ottenere la velocità effettiva necessaria per lo streaming di video e audio, DirectShow utilizza Direct3D e DirectSound laddove possibile. Queste tecnologie eseguono il rendering dei dati in modo efficiente sulle schede audio e grafiche dell'utente. DirectShow sincronizza la riproduzione incapsulando i dati multimediali in campioni con timestamp. Per gestire la varietà di origini, formati e dispositivi hardware possibili, DirectShow usa un'architettura modulare, in cui l'applicazione combina e trova la corrispondenza con componenti software diversi, detti *filtri*.

DirectShow fornisce filtri che supportano l'acquisizione e l'ottimizzazione di dispositivi basati sul Windows Driver Model (WDM), oltre a filtri che supportano le schede di acquisizione video for Windows (VfW) precedenti e i codec scritti per le interfacce di Gestione compressione audio (ACM) e video Compression Manager (VCM).

Il diagramma seguente illustra la relazione tra un'applicazione, i componenti DirectShow e alcuni componenti hardware e software supportati da DirectShow.

![architettura di alto livello](images/arch-oview2.png)

Come illustrato qui, i filtri DirectShow comunicano con e controllano un'ampia gamma di dispositivi, tra cui il file system locale, il sintonizzatore TV e le schede di acquisizione video, i codec VfW, la visualizzazione video (tramite DirectDraw o GDI) e la scheda audio (tramite DirectSound). Quindi, DirectShow isola l'applicazione da molte delle complessità di questi dispositivi. DirectShow fornisce inoltre filtri nativi per la compressione e la decompressione per determinati formati di file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su DirectShow](about-directshow.md)
</dt> </dl>

 

 




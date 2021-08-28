---
description: DirectShow Panoramica del sistema
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: DirectShow Panoramica del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb7855277029adc563cc032740d3a59b3691fcf12ed2b2595d37a1abd0d923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966351"
---
# <a name="directshow-system-overview"></a>DirectShow Panoramica del sistema

**La sfida della multimedialità**

L'uso di contenuti multimediali presenta diverse sfide principali:

-   I flussi multimediali contengono grandi quantità di dati, che devono essere elaborati molto rapidamente.
-   L'audio e il video devono essere sincronizzati in modo che si avviano e si arrestino contemporaneamente e vengono riprodotti con la stessa velocità.
-   I dati possono provengono da molte origini, tra cui file locali, reti di computer, trasmissioni televisive e videocamere.
-   I dati sono disponibili in diversi formati, ad esempio Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG) e Digital Video (DV).
-   Il programmatore non sa in anticipo quali dispositivi hardware saranno presenti nel sistema dell'utente finale.

**Soluzione DirectShow**

DirectShow è progettato per risolvere ognuna di queste sfide. L'obiettivo principale della progettazione è semplificare l'attività di creazione di applicazioni multimediali digitali nella piattaforma Windows isolando le applicazioni dalle complessità dei trasporti dati, dalle differenze hardware e dalla sincronizzazione.

Per ottenere la velocità effettiva necessaria per lo streaming di video e audio, DirectShow usa Direct3D e DirectSound quando possibile. Queste tecnologie eseguono il rendering dei dati in modo efficiente nelle schede audio e grafiche dell'utente. DirectShow sincronizza la riproduzione incapsulando i dati multimediali in esempi con timestamp. Per gestire l'ampia gamma di origini, formati e dispositivi hardware possibili, DirectShow usa un'architettura modulare, in cui l'applicazione combina e corrisponde a diversi componenti software denominati *filtri*.

DirectShow fornisce filtri che supportano i dispositivi di acquisizione e ottimizzazione basati sul modello di driver Windows (WDM), oltre ai filtri che supportano le schede di acquisizione Video for Windows (VfW) meno recenti e i codec scritti per le interfacce di Gestione compressione audio (ACM) e Video Compression Manager (VCM).

Il diagramma seguente illustra la relazione tra un'applicazione, i componenti DirectShow e alcuni componenti hardware e software supportati DirectShow.

![architettura di alto livello](images/arch-oview2.png)

Come illustrato di seguito, i filtri DirectShow comunicano con e controllano un'ampia gamma di dispositivi, tra cui il file system locale, il siner TV e le schede di acquisizione video, i codec VfW, lo schermo video (tramite DirectDraw o GDI) e la scheda audio (tramite DirectSound). Di conseguenza, DirectShow'applicazione viene isolata da molte delle complessità di questi dispositivi. DirectShow fornisce anche filtri di compressione e decompressione nativi per determinati formati di file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni DirectShow](about-directshow.md)
</dt> </dl>

 

 




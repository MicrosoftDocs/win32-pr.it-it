---
description: Funzionalità del vmr
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Funzionalità del vmr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c78fc34be3097beedb73ac3989bc468cff0851143355902e3236f672797a83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819553"
---
# <a name="features-of-the-vmr"></a>Funzionalità del vmr

Video Mixing Renderer 7 (VMR-7) supporta le nuove funzionalità seguenti:

-   Combinazione reale di più flussi video, usando le funzionalità di alpha blending dei dispositivi hardware Direct3D.
-   Possibilità di collegare il proprio componente di composizione per implementare effetti e transizioni tra più flussi video che entrano nel VMR.
-   Rendering senza finestra vero. Non è più necessario rendere la finestra di riproduzione video un elemento figlio della finestra dell'applicazione per contenere la riproduzione video. La nuova modalità di rendering senza finestra della macchina virtuale consente alle applicazioni di ospitare facilmente la riproduzione video all'interno di qualsiasi finestra senza dover inoltrare messaggi di finestra al renderer per l'elaborazione specifica del renderer.
-   Nuova modalità di riproduzione senza rendering in cui le applicazioni possono fornire il proprio componente allocatore per ottenere l'accesso all'immagine video decodificata prima che venga visualizzata sullo schermo.
-   Supporto migliorato per i PC dotati di più monitor.
-   Supporto per la nuova architettura DirectX Video Acceleration di Microsoft.
-   Supporto per la riproduzione video di alta qualità simultaneamente in più finestre.
-   Supporto per la modalità esclusiva DirectDraw
-   Compatibilità al 100% con le applicazioni esistenti.
-   Supporto per l'esecuzione di istruzioni dei fotogrammi e un modo affidabile per acquisire l'immagine corrente visualizzata.
-   La possibilità per le applicazioni di unire facilmente i propri dati di immagine statici (ad esempio logo del canale o componenti dell'interfaccia utente) con il video in modo uniforme senza sfarfallio.

VmR-9 supporta tutte le funzionalità elencate in precedenza, oltre a:

-   Possibilità di elaborare i dati video direttamente con le API Direct3D, ad esempio i pixel shader.
-   Supporto migliorato per il contenuto video interlacciato.
-   Supporto in qualsiasi piattaforma supportata da DirectX.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul rendering di combinazione video](about-the-video-mixing-render.md)
</dt> </dl>

 

 




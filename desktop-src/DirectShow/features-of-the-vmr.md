---
description: Funzionalità di VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Funzionalità di VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304390"
---
# <a name="features-of-the-vmr"></a>Funzionalità di VMR

Il video che combina il renderer 7 (VMR-7) supporta le seguenti nuove funzionalità:

-   Combinazione reale di più flussi video, usando le funzionalità di fusione alfa dei dispositivi hardware Direct3D.
-   La possibilità di collegare il proprio componente di composizione per implementare gli effetti e le transizioni tra più flussi video che entrano in VMR.
-   Vero rendering senza finestra. Non è più necessario rendere la finestra di riproduzione del video un figlio della finestra dell'applicazione per poter contenere la riproduzione video. La nuova modalità di rendering senza finestra di VMR consente alle applicazioni di ospitare facilmente la riproduzione video in qualsiasi finestra senza dover inviare i messaggi della finestra al renderer per l'elaborazione specifica del renderer.
-   Nuova modalità di riproduzione con rendering in cui le applicazioni possono fornire il proprio componente allocatore per ottenere l'accesso all'immagine video decodificata prima che venga visualizzata sullo schermo.
-   Supporto migliorato per i PC dotati di più monitor.
-   Supporto per la nuova architettura di accelerazione video DirectX Microsoft.
-   Supporto per la riproduzione video di alta qualità simultaneamente su più finestre.
-   Supporto per la modalità esclusiva di DirectDraw
-   100% di compatibilità con le versioni precedenti delle applicazioni esistenti.
-   Supporto per l'esecuzione dei frame e un modo affidabile per acquisire l'immagine corrente da visualizzare.
-   La possibilità per le applicazioni di incorporare facilmente i dati di immagini statiche, ad esempio i loghi dei canali o i componenti dell'interfaccia utente, con il video in modo senza sfarfallio.

VMR-9 supporta tutte le funzionalità sopra elencate, oltre a:

-   Possibilità di elaborare i dati video direttamente con le API Direct3D, ad esempio i pixel shader.
-   Supporto migliorato per contenuto video interlacciato.
-   Supporto per qualsiasi piattaforma supportata da DirectX.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul rendering del mixaggio video](about-the-video-mixing-render.md)
</dt> </dl>

 

 




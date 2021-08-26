---
description: Componenti del filtro VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Componenti del filtro VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dda6e8d37e1b5ac8c00da024fe78d4e18e38eed1e1735e787284d389769cff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903337"
---
# <a name="vmr-filter-components"></a>Componenti del filtro VMR

La macchina virtuale usa una progettazione modulare che consente alle applicazioni di configurarla per molti scenari di rendering diversi. A seconda della configurazione, la macchina virtuale contiene da due a cinque sottocomponenti (oltre ai pin di input).

![vmr in modalità finestra con più flussi](images/vmr-multiple-streams.png)

**Mixer:** Il mixer è un oggetto COM responsabile della combinazione di più flussi. Il dinterlacing si verifica anche all'interno del mixer. Il mixer viene caricato dal vmr quando vengono rilevati più flussi di input o quando il video di input è interlacciato. Il mixer raccoglie informazioni su ogni flusso di input e ordina i flussi nell'ordine Z corretto. È responsabile di determinare quando ogni pin di input riceve un campione e di istruire il compositore dell'immagine al momento appropriato per eseguire la fusione effettiva. Il mixer calcola anche il timestamp da applicare a ogni immagine di output. Quando l'applicazione fornisce una bitmap da visualizzare sopra l'immagine composita, il mixer è responsabile di garantire che la bitmap sia visualizzata sopra anche se viene modificato l'ordine Z dei flussi di input.

**Image Compositor ( Compositore immagine):** Image Compositor è un oggetto COM che esegue la fusione effettiva dei flussi di input su una singola superficie DirectDraw o Direct3D fornita dall'allocator-presenter. La macchina virtuale fornisce un compositore di immagini predefinito che consente alle applicazioni di eseguire effetti di fusione alfa 2D. Le applicazioni possono fornire un compositore di immagini personalizzato per abilitare altri effetti 2D e 3D, ad esempio l'applicazione di trame a parti dell'immagine, la fusione alfa per pixel, il mapping dell'immagine a oggetti 3D stazionari o in movimento e così via.

**Allocator-Presenter:** Allocator-presenter è un oggetto COM che alloca l'oggetto DirectDraw o Direct3D e gestisce la comunicazione con la scheda grafica. Il disegno può essere eseguito come capovolgimento o beatitudine. È possibile collegare il proprio allocatore-presentatore per creare e controllare l'oggetto DirectDraw o Direct3D e/o per ottenere l'accesso ai bit video in fase di presentazione.

**Gestione finestre:** Gestione finestre viene usato solo in modalità finestra. Gestione finestre supporta le interfacce [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) legacy per la compatibilità con le versioni precedenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul rendering di combinazione di video](about-the-video-mixing-render.md)
</dt> </dl>

 

 




---
description: Componenti del filtro VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Componenti del filtro VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529509"
---
# <a name="vmr-filter-components"></a>Componenti del filtro VMR

VMR usa una progettazione modulare che consente alle applicazioni di configurarla per molti scenari di rendering diversi. A seconda della configurazione, il VMR contiene da due a cinque sottocomponenti (oltre ai pin di input).

![VMR in modalità finestra con più flussi](images/vmr-multiple-streams.png)

**Mixer:** Il mixer è un oggetto COM responsabile della combinazione di più flussi. Il deinterlacciamento si verifica anche all'interno del mixer. Il mixer viene caricato da VMR quando vengono rilevati più flussi di input o quando il video di input è interlacciato. Il mixer raccoglie informazioni su ogni flusso di input e ordina i flussi nell'ordine Z corretto. È responsabile di determinare quando ogni pin di input riceve un campione e per istruire il compositore dell'immagine al momento giusto per eseguire la fusione effettiva. Il mixer calcola anche il timestamp da applicare a ogni immagine di output. Quando l'applicazione fornisce una bitmap da visualizzare sopra l'immagine composita, il mixer è responsabile di garantire che la bitmap venga visualizzata in cima anche se viene modificato l'ordine Z dei flussi di input.

**Compositor immagine:** Il compositor dell'immagine è un oggetto COM che esegue la fusione effettiva dei flussi di input su una singola superficie DirectDraw o Direct3D fornita da Allocator-Presenter. VMR fornisce un compositor di immagini predefinito che consente alle applicazioni di eseguire effetti di fusione alfa 2D. Le applicazioni possono fornire un compositor di immagini personalizzato per abilitare altri effetti 2D e 3D, ad esempio l'applicazione di trame a parti dell'immagine, la fusione alfa per pixel, il mapping dell'immagine a oggetti fissi o mobili e così via.

**Allocatore-Presenter:** Allocator-Presenter è un oggetto COM che alloca l'oggetto DirectDraw o Direct3D e gestisce la comunicazione con la scheda grafica. Il disegno può essere eseguito come un flip o come blit. È possibile collegare il proprio allocatore-Presenter per creare e controllare l'oggetto DirectDraw o Direct3D e/o per ottenere l'accesso ai bit video in fase di presentazione.

**Gestione finestre:** Gestione finestre viene utilizzato solo in modalità finestra. Gestione finestre supporta le interfacce legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) per la compatibilità con le versioni precedenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul rendering del mixaggio video](about-the-video-mixing-render.md)
</dt> </dl>

 

 




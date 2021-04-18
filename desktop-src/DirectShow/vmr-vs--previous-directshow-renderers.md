---
description: Confronto tra VMR e
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: VMR rispetto ai renderer DirectShow precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db40f9789a73446cb2dac4ed7033bdb163141bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308950"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>VMR rispetto ai renderer DirectShow precedenti

Con i filtri precedenti, i renderer diversi sarebbero necessari nel grafico a seconda della configurazione hardware.

Il filtro [renderer video](video-renderer-filter.md) è stato usato per eseguire il rendering di un singolo flusso video in scenari di porta non video. Si basava su una tecnologia hardware grafica che ora risale a cinque anni fa e su una versione precedente di DirectDraw. In alcuni scenari USA GDI per il rendering. Questa operazione viene eseguita per conservare le risorse video, che sono state molto più limitate di cinque anni fa, oppure per superare le limitazioni di DirectDraw correlate al supporto di più monitor. Né VMR-7 né VMR-9 utilizzano mai GDI per il rendering; VMR-7 si basa completamente su DirectDraw 7 e VMR-9 è basato su Direct3D 9.

Negli scenari che coinvolgono una porta video o più flussi di input video, prima di VMR è stato usato il filtro [Overlay Mixer](overlay-mixer-filter.md) per il rendering. Questo filtro usa solo la sovrimpressione hardware nella scheda grafica, quindi è generalmente limitata alla superficie sovrapposta fornita dalla maggior parte delle schede. Il mixer di sovrimpressione esegue la chiave del colore di destinazione, ma non è in grado di eseguire la fusione alfa. Poiché non dispone di una gestione finestre, deve usare un secondo filtro, il renderer video, per la gestione della finestra. Il VMR è in grado di eseguire una reale fusione alfa e può creare più sovrapposizioni nel software oltre alle sovrapposizioni hardware.

Negli scenari di porta video in cui le applicazioni stavano sovraponendo la didascalia chiusa o altri dati VBI nel video, era necessario un filtro aggiuntivo, ovvero [VBI Surface allocator](vbi-surface-allocator.md), per allocare la memoria video aggiuntiva per il testo VBI. Per gli ISV, VMR-7 semplifica lo sviluppo di applicazioni combinando la funzionalità di allocazione e rendering in un unico filtro usato in tutti gli scenari. Con VMR, l'allocatore di superficie VBI non è più necessario. Questo filtro viene sostituito in Windows XP dal nuovo filtro di [gestione porta video](video-port-manager.md) che esegue tutte le attività della porta video eseguite in precedenza dal mixer sovrapposto.

> [!Note]  
> VMR-9 non supporta le porte video.

 

VMR è più affidabile dei renderer precedenti, in parte perché usa solo DirectDraw 7 (o Direct3D 9 Se si usano le interfacce VMR-9), anziché i renderer precedenti che usavano una combinazione di interfacce da versioni precedenti e più recenti di DirectDraw. Il VMR usa anche un nuovo meccanismo di presentazione delle immagini, progettato per le generazioni attuali e future degli adapter, che hanno il supporto per Direct3D, una maggiore larghezza di banda di memoria e di memoria video e funzionalità di accelerazione hardware. Con VMR, l'attenzione è rivolta all'elaborazione front-end e a una minore dipendenza dalle porte video e dalle sovrapposizioni. Tuttavia, anche con tutte le nuove funzionalità, VMR è progettato per la massima compatibilità con le applicazioni esistenti.

Il VMR è anche estendibile. Le applicazioni possono fornire i propri sottocomponenti per eseguire effetti video personalizzati e/o assumere il controllo del processo di allocazione e rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul rendering del mixaggio video](about-the-video-mixing-render.md)
</dt> </dl>

 

 




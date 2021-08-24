---
description: VmR e
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: Renderer di macchine virtuali e DirectShow precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9401361c5b258fdff09bf25351a79bf8315dabfb0c82636d7d8c3c9ffcdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903271"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>Renderer di macchine virtuali e DirectShow precedenti

Con i filtri vecchi, nel grafico sarebbero necessari renderer diversi a seconda della configurazione hardware.

Il [filtro Renderer](video-renderer-filter.md) video è stato usato per eseguire il rendering di un singolo flusso video in scenari di porte non video. Si basava sulla tecnologia dell'hardware grafico che ha ora più di cinque anni e su una versione precedente di DirectDraw. In alcuni scenari usa GDI per il rendering. Questa operazione viene eseguita per conservare le risorse video, molto più limitate cinque anni fa, oppure per superare le limitazioni in DirectDraw correlate al supporto di più monitor. Né VMR-7 né VMR-9 utilizzano GDI per il rendering; VMR-7 è completamente basato su DirectDraw 7 e VMR-9 è basato su Direct3D 9.

Negli scenari che coinvolgono una porta video o più flussi di input video, prima del vmr è stato usato il filtro overlay [Mixer](overlay-mixer-filter.md) per il rendering. Questo filtro usa solo la sovrimpressione hardware nella scheda grafica e pertanto è in genere limitato all'unica superficie di sovrapposizione fornita dalla maggior parte delle schede. L'Mixer esegue la combinazione di colori di destinazione, ma non è in grado di eseguire la fusione alfa. Poiché non dispone di un gestore finestre, deve usare un secondo filtro, il renderer video, per la gestione delle finestre. VmR è in grado di ottenere una vera fusione alfa e può creare più sovrimpressione nel software oltre alle sovrimpressione hardware.

Negli scenari di porte video in cui le applicazioni sovrapponevano sottotitoli codificati o altri dati VBI nel video, era necessario un filtro aggiuntivo, [vbi Surface Allocator](vbi-surface-allocator.md), per allocare la memoria video aggiuntiva per il testo VBI. Per gli ISV, VMR-7 semplifica lo sviluppo di applicazioni combinando le funzionalità di allocazione e rendering in un unico filtro usato in tutti gli scenari. Con vmr, l'allocatore di superficie VBI non è più necessario. Questo filtro viene sostituito in Windows [](video-port-manager.md) XP dal nuovo filtro Di Gestione porte video che esegue tutte le attività di porta video eseguite in precedenza dal filtro overlay Mixer.

> [!Note]  
> VmR-9 non supporta le porte video.

 

La macchina virtuale è più affidabile rispetto ai renderer precedenti, in parte perché usa solo le interfacce DirectDraw 7 (o Direct3D 9 se si usa VMR-9), a differenza dei renderer precedenti che usavano una combinazione di interfacce di versioni precedenti e più recenti di DirectDraw. La macchina virtuale usa anche un nuovo meccanismo di presentazione delle immagini progettato per le generazioni correnti e future di schede, con supporto per Direct3D, maggiore larghezza di banda della memoria video e VRAM e funzionalità di accelerazione hardware. Con il vmr, l'attenzione è concentrata sull'elaborazione front-end e sulla riduzione della dipendenza dalle porte video e dalle sovrapposizioni. Anche con tutte le nuove funzionalità, tuttavia, la macchina virtuale è progettata per garantire la massima compatibilità con le applicazioni esistenti.

Anche la macchina virtuale è estendibile. Le applicazioni possono fornire i propri componenti secondari per eseguire effetti video personalizzati e/o assumere il controllo del processo di allocazione e rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul rendering di combinazione di video](about-the-video-mixing-render.md)
</dt> </dl>

 

 




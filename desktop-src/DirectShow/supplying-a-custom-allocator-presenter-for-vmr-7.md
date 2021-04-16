---
description: Specifica di un Allocator-Presenter personalizzato per VMR-7
ms.assetid: 19b43c9b-2578-418f-b03b-af7c7a3a46e4
title: Specifica di un Allocator-Presenter personalizzato per VMR-7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79f191401f990214b2551f9210fab4dfe4d43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556553"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-7"></a>Specifica di un Allocator-Presenter personalizzato per VMR-7

Allocator-Presenter è responsabile dell'allocazione delle superfici di DirectDraw e della presentazione dei fotogrammi video per il rendering. Nella maggior parte degli scenari, la funzionalità di allocatore-Presenter predefinito sarà più che sufficiente per le esigenze di un'applicazione. Tuttavia, inserendo un allocatore-Presenter personalizzato, un'applicazione può ottenere l'accesso diretto ai bit video e controllare completamente il processo di rendering. Il compromesso per questa maggiore potenza è che l'applicazione deve gestire la complessità aggiuntiva della gestione della superficie di DirectDraw.

![uso di un allocatore-Presenter personalizzato](images/custom-ap.png)

La figura precedente illustra le interfacce di comunicazione usate da VMR e da Allocator-Presenter. Un allocatore-Presenter personalizzato che esegue l'override di tutte le funzionalità di allocazione e presentazione predefinite deve implementare le interfacce [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) e [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) e, facoltativamente, [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol).

Per sostituire l'allocatore-Presenter predefinito, un'applicazione chiama il metodo [**IVMRSurfaceAllocatorNotify:: AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) e passa un puntatore al nuovo allocatore-Presenter. In risposta a questa chiamata, VMR chiamerà il metodo [**IVMRSurfaceAllocator:: AdviseNotify**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocator-advisenotify) di Allocator-Presenter per fornire il puntatore all'interfaccia [**IVMRSurfaceAllocatorNotify**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify) di VMR. Allocator-Presenter utilizzerà questo puntatore di interfaccia quando passa gli eventi a VMR con il metodo [**IVMRSurfaceAllocatorNotify:: NotifyEvent**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent) .

Come soluzione alternativa, un'applicazione può usare sia il proprio allocatore-Presenter che l'allocatore-Presenter predefinito. In questo scenario, l'allocatore-Presenter personalizzato gestisce solo le chiamate in cui è necessaria la funzionalità personalizzata e passa il resto delle chiamate dal VMR al relatore allocatore predefinito. In molti casi, è necessario solo eseguire l'override dell'interfaccia [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) .

![uso di due allocatori-Presenter](images/custom-ap2.png)

Per usare un allocatore-Presenter personalizzato e l'allocatore-Presenter predefinito, un'applicazione chiama prima [**IVMRSurfaceAllocatorNotify:: AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) per fornire un puntatore al nuovo allocatore-Presenter. In questo modo l'oggetto Allocator-Presenter predefinito viene eliminato definitivamente, quindi l'applicazione deve crearne un'altra chiamando **QueryInterface** in VMR e richiedendo l'interfaccia [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) . Come illustrato nella figura precedente, l'allocatore-Presenter personalizzato esegue l'override dei metodi dell'interfaccia [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) e passa semplicemente tutte le chiamate all'interfaccia **IVMRSurfaceAllocator** tramite l'implementazione predefinita. La figura mostra anche l'interfaccia [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) come implementata in Allocator-Presenter.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica di un Allocator-Presenter personalizzato per VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
</dt> <dt>

[Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 




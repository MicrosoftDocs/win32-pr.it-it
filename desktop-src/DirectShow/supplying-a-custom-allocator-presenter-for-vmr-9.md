---
description: Fornitura di un Allocator-Presenter personalizzato per VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Fornitura di un Allocator-Presenter personalizzato per VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e5f87aaecf0b2e8576b60a2d0f6a8c74e60fcf0759a123015ded9136c079bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951720"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Fornitura di un Allocator-Presenter personalizzato per VMR-9

Per usare un allocatore-presenter personalizzato con il filtro Video Mixing Renderer 9 (VMR-9), seguire questa procedura:

1.  Implementare una classe che supporti [**le interfacce IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) e [**IVMRImagePresenter9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
2.  Chiamare **QueryInterface** nel filtro VMR-9 per [**l'interfaccia IVMRFilterConfig9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9)
3.  Chiamare il [**metodo IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) e passare il flag **\_ renderless VMR9Mode.**
4.  **QueryInterface** nel filtro VMR-9 per [**l'interfaccia IVMRSurfaceAllocatorNotify9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9)
5.  Chiamare il metodo [**IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) e passare un puntatore al metodo [**IVMRSurfaceAllocator9 dell'allocatore-presentatore.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
6.  Chiamare il metodo [**IVMRSurfaceAllocator9::AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) dell'allocator-presenter e passare un puntatore all'interfaccia [**IVMRSurfaceAllocatorNotify9 del filtro VMR-9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9)
7.  Nell'implementazione di [**IVMRSurfaceAllocator9::AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify)chiamare [**IVMRSurfaceAllocatorNotify9::SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) Passare un puntatore al dispositivo Direct3D e un handle al monitor in cui verrà visualizzato il video.
8.  Nell'implementazione del metodo [**IVMRSurfaceAllocator9::InitializeDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) creare superfici Direct3D che corrispondono ai parametri specificati nel **metodo InitializeDevice.** Facoltativamente, è possibile usare il metodo [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) del filtro VMR-9 per allocare queste superfici. Archiviare i puntatori di superficie in una matrice.
    > [!Note]  
    > Se si vuole che VMR-9 disegni i fotogrammi video su una superficie di trama, aggiungere il flag **VMR9AllocFlag \_ TextureSurface** alla [**struttura VMR9AllocationInfo.**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) Se il dispositivo non supporta trame nel formato video nativo, potrebbe essere necessario creare una superficie di trama separata e quindi copiare i fotogrammi video dalla superficie video alla trama.

     

9.  Durante lo streaming, VMR-9 ottiene le superfici dall'allocatore-presentatore chiamando il [**metodo IVMRSurfaceAllocator9::GetSurface.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) VmR-9 specifica la superficie in base al relativo indice all'interno della matrice di superfici (passaggio 8).
10. Presentare l'immagine quando VMR-9 chiama il metodo [**IVMRImagePresenter9::P resentImage.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) I parametri includono un puntatore alla superficie Direct3D che contiene l'immagine video.
11. Se il dispositivo Direct3D viene perso in qualsiasi momento, l'allocatore-presentatore deve ripristinare il dispositivo e ricreare le superfici. Ad esempio, il dispositivo può andare perso se la modalità di visualizzazione cambia o l'utente sposta la finestra in un altro monitoraggio. Se il dispositivo Direct3D cambia, chiamare il metodo [**IVMRSurfaceAllocatorNotify9::ChangeD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) del filtro VMR-9.
12. Quando lo streaming si arresta, VMR-9 chiama il [**metodo IVMRSurfaceAllocator9::TerminateDevice.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) Allocator-presenter deve rilasciare tutte le risorse Direct3D.

Esistono alcune differenze tra VMR-7 e VMR-9 nel modo in cui vengono gestiti gli allocator-presenter personalizzati:

-   Il metodo [**AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) del filtro VMR-9 è disponibile per l'allocatore-presentatore da usare durante l'allocazione delle superfici. Questo metodo rende superfluo per un allocatore-presenter personalizzato inoltrare tutte le chiamate all'allocatore-presenter predefinito. Per questo motivo, il CLSID dell'allocatore-presenter predefinito del filtro VMR-9 non viene pubblicato.
-   A differenza di VMR-7, VMR-9 non fornisce uno speciale allocatore-presentatore in modalità esclusiva DirectDraw. Il [**metodo IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) rende questo oggetto non necessario.
-   Per i video interlacciati, VMR-9 de-interlaccia sempre il video prima che presenti l'immagine. L'allocatore-presentatore non è più responsabile della de-interlacciamento dell'immagine prima di visualizzarla.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di riproduzione senza rendering vmr (allocatore-presentatori personalizzati)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 




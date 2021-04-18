---
description: Specifica di un Allocator-Presenter personalizzato per VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Specifica di un Allocator-Presenter personalizzato per VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f004e119fc1cbfc167c2130852a4f59700706fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318670"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Specifica di un Allocator-Presenter personalizzato per VMR-9

Per usare un oggetto Allocator-Presenter personalizzato con il filtro video Mixing Renderer 9 (VMR-9), seguire questa procedura:

1.  Implementare una classe che supporta le interfacce [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) e [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9) .
2.  Chiamare **QueryInterface** sul filtro VMR-9 per l'interfaccia [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .
3.  Chiamare il metodo [**IVMRFilterConfig9:: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) e passare il flag **di \_ rendering VMR9Mode** .
4.  **QueryInterface** sul filtro VMR-9 per l'interfaccia [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) .
5.  Chiamare il metodo [**IVMRSurfaceAllocatorNotify9:: AdviseSurfaceAllocator**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) e passare un puntatore al metodo [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) dell'allocatore-Presenter.
6.  Chiamare il metodo [**IVMRSurfaceAllocator9:: AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) del relatore dell'allocatore e passare un puntatore all'interfaccia [**IVMRSURFACEALLOCATORNOTIFY9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) del filtro VMR-9.
7.  Nell'implementazione di [**IVMRSurfaceAllocator9:: AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify), chiamare [**IVMRSurfaceAllocatorNotify9:: SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) passare un puntatore al dispositivo Direct3D e un handle per il monitoraggio in cui verrà visualizzato il video.
8.  Nell'implementazione del metodo [**IVMRSurfaceAllocator9:: InitializeDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) creare le superfici Direct3D che corrispondono ai parametri specificati nel metodo **InitializeDevice** . Facoltativamente, è possibile usare il metodo [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) del filtro VMR-9 per allocare tali superfici. Archiviare i puntatori della superficie in una matrice.
    > [!Note]  
    > Se si desidera che VMR-9 disegni i fotogrammi video su una superficie di trama, aggiungere il flag **VMR9AllocFlag \_ TextureSurface** alla struttura [**VMR9AllocationInfo**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) . Se il dispositivo non supporta le trame nel formato video nativo, potrebbe essere necessario creare una superficie di trama separata, quindi copiare i fotogrammi video dalla superficie video alla trama.

     

9.  Durante lo streaming, VMR-9 ottiene le superfici dall'allocatore-Presenter chiamando il metodo [**IVMRSurfaceAllocator9:: GetSurface**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) . VMR-9 specifica la superficie in base al relativo indice all'interno della matrice di superficie (passaggio 8).
10. Presentare l'immagine quando VMR-9 chiama il metodo [**IVMRImagePresenter9::P resentimage**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) . I parametri includono un puntatore alla superficie Direct3D che contiene l'immagine del video.
11. Se il dispositivo Direct3D viene perso in qualsiasi momento, l'allocatore-Presenter deve ripristinare il dispositivo e ricreare le superfici. Ad esempio, il dispositivo può andare perduto se la modalità di visualizzazione cambia o se l'utente sposta la finestra su un altro monitor. Se il dispositivo Direct3D viene modificato, chiamare il metodo [**IVMRSurfaceAllocatorNotify9:: ChangeD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) del filtro VMR-9.
12. Quando il flusso viene interrotto, VMR-9 chiama il metodo [**IVMRSurfaceAllocator9:: TerminateDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) . Allocator-Presenter deve rilasciare tutte le risorse Direct3D.

Esistono alcune differenze tra VMR-7 e VMR-9 nel modo in cui vengono gestiti gli allocatori personalizzati:

-   Il metodo [**AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) del filtro VMR-9 è disponibile per l'allocatore-Presenter da usare durante l'allocazione di superfici. Questo metodo rende non necessario che un allocatore-Presenter personalizzato inoltri qualsiasi chiamata a allocatore-Presenter predefinito. Per questo motivo, il CLSID dell'allocatore-Presenter predefinito del filtro VMR-9 non viene pubblicato.
-   A differenza di VMR-7, VMR-9 non fornisce una speciale modalità esclusiva DirectDraw Allocator-Presenter. Il metodo [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) rende non necessario questo oggetto.
-   Per il video interlacciato, VMR-9 Annulla sempre l'interlacciatura del video prima di presentare l'immagine. Allocator-Presenter non è più responsabile del deinterlacciamento dell'immagine prima di visualizzarla.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 




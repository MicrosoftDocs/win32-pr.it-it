---
description: Modalità esclusiva DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Modalità esclusiva DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09199e04a221299676c21fbc2876af4b8149943a743101d34893d5563ed42482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016180"
---
# <a name="directdraw-exclusive-mode"></a>Modalità esclusiva DirectDraw

> [!Note]  
> Questo argomento si applica solo a VMR-7. In VMR-9 è possibile abilitare la modalità esclusiva fornendo il proprio allocatore-presentatore in modalità esclusiva. Questa operazione è relativamente semplice se si usa il [**metodo IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) L'esempio VMR9Allocator illustra come implementare un allocatore-presenter personalizzato.

 

In modalità esclusiva DirectDraw un'applicazione assume il controllo esclusivo dell'hardware grafico. Ciò è utile per applicazioni come giochi o applicazioni video a schermo intero. In genere, la macchina virtuale crea gli oggetti DirectDraw e imposta il livello cooperativo su normale. Tuttavia, per eseguire la macchina virtuale in modalità esclusiva DirectDraw, l'applicazione stessa deve creare l'oggetto DirectDraw e la superficie primaria e chiamare **SetCooperativeLevel** per specificare la modalità esclusiva.

La macchina virtuale ha uno speciale allocatore-presenter che ne consente l'esecuzione in modalità esclusiva DirectDraw. Per configurare la macchina virtuale per l'uso di questo allocatore-presenter:

1.  Creare il filtro Graph e aggiungerne il vmr usando il [**metodo IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) Per un esempio di codice, vedere [Modalità senza finestra VMR.](vmr-windowless-mode.md)
2.  Creare l'allocatore-presenter in modalità esclusiva:
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  Configurare il nuovo allocator-presenter:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Collegare il nuovo allocatore-presenter al vmr.
5.  Compilare il resto del grafico dei filtri nei modi consueti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di funzionamento di VMR](vmr-modes-of-operation.md)
</dt> </dl>

 

 




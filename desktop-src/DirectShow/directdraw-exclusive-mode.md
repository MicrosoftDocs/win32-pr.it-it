---
description: Modalità esclusiva di DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Modalità esclusiva di DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304399"
---
# <a name="directdraw-exclusive-mode"></a>Modalità esclusiva di DirectDraw

> [!Note]  
> Questo argomento si applica solo a VMR-7. In VMR-9 è possibile abilitare la modalità esclusiva fornendo il proprio allocatore-Presenter in modalità esclusiva. Questo è relativamente semplice se si usa il metodo [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) . L'esempio VMR9Allocator illustra come implementare un allocatore-Presenter personalizzato.

 

In modalità esclusiva DirectDraw, un'applicazione acquisisce il controllo esclusivo dell'hardware grafico. Questa operazione è utile per applicazioni quali giochi o applicazioni video a schermo intero. In genere, VMR crea gli oggetti DirectDraw e imposta il livello cooperativo su Normal. Tuttavia, per eseguire VMR in modalità esclusiva DirectDraw, l'applicazione deve creare l'oggetto DirectDraw e la superficie primaria e chiamare **SetCooperativeLevel** per specificare la modalità esclusiva.

VMR dispone di uno speciale allocatore-Presenter che consente l'esecuzione in modalità esclusiva DirectDraw. Per configurare VMR per l'uso di questo allocatore-Presenter:

1.  Creare il grafico di filtro e aggiungervi il VMR usando il metodo [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Per un esempio di codice, vedere [modalità senza finestra VMR](vmr-windowless-mode.md).
2.  Creare la modalità esclusiva Allocator-Presenter:
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

    

3.  Configurare il nuovo allocatore-Presenter:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Collegare il nuovo allocatore-Presenter a VMR.
5.  Compilare il resto del grafico di filtro nei modi usuali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di funzionamento VMR](vmr-modes-of-operation.md)
</dt> </dl>

 

 




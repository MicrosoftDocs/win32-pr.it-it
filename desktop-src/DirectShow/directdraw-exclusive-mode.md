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
# <a name="directdraw-exclusive-mode"></a><span data-ttu-id="2483d-103">Modalità esclusiva di DirectDraw</span><span class="sxs-lookup"><span data-stu-id="2483d-103">DirectDraw Exclusive Mode</span></span>

> [!Note]  
> <span data-ttu-id="2483d-104">Questo argomento si applica solo a VMR-7.</span><span class="sxs-lookup"><span data-stu-id="2483d-104">This topic applies to the VMR-7 only.</span></span> <span data-ttu-id="2483d-105">In VMR-9 è possibile abilitare la modalità esclusiva fornendo il proprio allocatore-Presenter in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="2483d-105">In the VMR-9, you enable exclusive mode by supplying your own exclusive mode allocator-presenter.</span></span> <span data-ttu-id="2483d-106">Questo è relativamente semplice se si usa il metodo [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) .</span><span class="sxs-lookup"><span data-stu-id="2483d-106">This is relatively straightforward if you use the [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) method.</span></span> <span data-ttu-id="2483d-107">L'esempio VMR9Allocator illustra come implementare un allocatore-Presenter personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2483d-107">The VMR9Allocator sample shows how to implement a custom allocator-presenter.</span></span>

 

<span data-ttu-id="2483d-108">In modalità esclusiva DirectDraw, un'applicazione acquisisce il controllo esclusivo dell'hardware grafico.</span><span class="sxs-lookup"><span data-stu-id="2483d-108">In DirectDraw Exclusive Mode, an application takes exclusive control of the graphics hardware.</span></span> <span data-ttu-id="2483d-109">Questa operazione è utile per applicazioni quali giochi o applicazioni video a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="2483d-109">This is useful for applications such as games, or perhaps full-screen video applications.</span></span> <span data-ttu-id="2483d-110">In genere, VMR crea gli oggetti DirectDraw e imposta il livello cooperativo su Normal.</span><span class="sxs-lookup"><span data-stu-id="2483d-110">Normally, the VMR creates the DirectDraw objects and sets the cooperative level to normal.</span></span> <span data-ttu-id="2483d-111">Tuttavia, per eseguire VMR in modalità esclusiva DirectDraw, l'applicazione deve creare l'oggetto DirectDraw e la superficie primaria e chiamare **SetCooperativeLevel** per specificare la modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="2483d-111">However, to run the VMR in DirectDraw Exclusive Mode, the application itself must create the DirectDraw object and the primary surface, and call **SetCooperativeLevel** to specify exclusive mode.</span></span>

<span data-ttu-id="2483d-112">VMR dispone di uno speciale allocatore-Presenter che consente l'esecuzione in modalità esclusiva DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="2483d-112">The VMR has a special allocator-presenter that enables it to run in DirectDraw Exclusive Mode.</span></span> <span data-ttu-id="2483d-113">Per configurare VMR per l'uso di questo allocatore-Presenter:</span><span class="sxs-lookup"><span data-stu-id="2483d-113">To configure the VMR to use this allocator-presenter:</span></span>

1.  <span data-ttu-id="2483d-114">Creare il grafico di filtro e aggiungervi il VMR usando il metodo [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) .</span><span class="sxs-lookup"><span data-stu-id="2483d-114">Create the Filter Graph and add the VMR to it using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="2483d-115">Per un esempio di codice, vedere [modalità senza finestra VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="2483d-115">For a code example, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span>
2.  <span data-ttu-id="2483d-116">Creare la modalità esclusiva Allocator-Presenter:</span><span class="sxs-lookup"><span data-stu-id="2483d-116">Create the Exclusive Mode allocator-presenter:</span></span>
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

    

3.  <span data-ttu-id="2483d-117">Configurare il nuovo allocatore-Presenter:</span><span class="sxs-lookup"><span data-stu-id="2483d-117">Configure the new allocator-presenter:</span></span>
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  <span data-ttu-id="2483d-118">Collegare il nuovo allocatore-Presenter a VMR.</span><span class="sxs-lookup"><span data-stu-id="2483d-118">Plug the new allocator-presenter into the VMR.</span></span>
5.  <span data-ttu-id="2483d-119">Compilare il resto del grafico di filtro nei modi usuali.</span><span class="sxs-lookup"><span data-stu-id="2483d-119">Build the rest of the filter graph in the usual ways.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2483d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2483d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2483d-121">Modalità di funzionamento VMR</span><span class="sxs-lookup"><span data-stu-id="2483d-121">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
</dt> </dl>

 

 




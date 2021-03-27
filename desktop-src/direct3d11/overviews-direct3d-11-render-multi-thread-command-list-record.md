---
title: Come registrare un elenco di comandi
description: In questo argomento viene illustrato come creare e registrare un elenco di comandi.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711545"
---
# <a name="how-to-record-a-command-list"></a><span data-ttu-id="4ebd9-103">Procedura: registrare un elenco di comandi</span><span class="sxs-lookup"><span data-stu-id="4ebd9-103">How to: Record a Command List</span></span>

<span data-ttu-id="4ebd9-104">Un [elenco](overviews-direct3d-11-render-multi-thread-command-list.md) di comandi è un elenco registrato di comandi per il rendering.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="4ebd9-105">In questo argomento viene illustrato come creare e registrare un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="4ebd9-105">This topic shows how to create and record a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="4ebd9-106">Usare un elenco di comandi per registrare i comandi di rendering e riprodurli in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-106">Use a command list to record render commands and play them back later.</span></span> <span data-ttu-id="4ebd9-107">Un elenco di comandi è utile per suddividere le attività di rendering tra thread.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-107">A command list is convenient for splitting rendering tasks between threads.</span></span>

<span data-ttu-id="4ebd9-108">**Per registrare un elenco di comandi**</span><span class="sxs-lookup"><span data-stu-id="4ebd9-108">**To record a command list**</span></span>

1.  <span data-ttu-id="4ebd9-109">È necessario creare un elenco di comandi da un contesto posticipato, che contiene lo stato del dispositivo e le azioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-109">A command list must be created from a deferred context, which contains device state and rendering actions.</span></span> <span data-ttu-id="4ebd9-110">Dato un dispositivo, creare un contesto posticipato chiamando [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="4ebd9-110">Given a device, create a deferred context by calling [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  <span data-ttu-id="4ebd9-111">Usare il contesto posticipato per eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-111">Use the deferred context to render.</span></span>

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    <span data-ttu-id="4ebd9-112">Questo semplice esempio cancella una destinazione di rendering, ma è possibile aggiungere altri comandi di rendering.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-112">This simple example clears a render target, but you could add additional render commands.</span></span>

3.  <span data-ttu-id="4ebd9-113">Creare o registrare un elenco di comandi chiamando [**sul ID3D11DeviceContext:: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) e passando un puntatore a un'interfaccia [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) non inizializzata.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-113">Create/record a command list by calling [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) and passing a pointer to an uninitialized [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) interface.</span></span>

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    <span data-ttu-id="4ebd9-114">Quando il metodo restituisce un risultato, viene creato un elenco di comandi contenente tutti i comandi di rendering e un'interfaccia viene restituita all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-114">When the method returns, a command list is created containing all the render commands and an interface is returned to the application.</span></span>

    <span data-ttu-id="4ebd9-115">Il parametro booleano indica al runtime cosa fare con lo stato della pipeline nel contesto posticipato.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-115">The boolean parameter tells the runtime what to do with the pipeline state in the deferred context.</span></span> <span data-ttu-id="4ebd9-116">**True** significa ripristinare lo stato del contesto di dispositivo alla condizione dell'elenco di pre-comandi al termine della registrazione, **false** significa che non modifica lo stato dopo la registrazione.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-116">**TRUE** means restore the state of the device context to its pre-command list condition when recording is completed, **FALSE** means do not change the state after recording.</span></span> <span data-ttu-id="4ebd9-117">Ciò significa che il contesto di dispositivo rifletterà le modifiche di stato contenute nell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="4ebd9-117">This means that the device context will reflect the state changes contained in the command list.</span></span>

<span data-ttu-id="4ebd9-118">Per vedere un esempio per la riproduzione di un elenco di comandi, vedere [procedura: riprodurre un elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span><span class="sxs-lookup"><span data-stu-id="4ebd9-118">To see an example for playing back a command list, see [How to: Play Back a Command List](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ebd9-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ebd9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ebd9-120">Elenco comandi</span><span class="sxs-lookup"><span data-stu-id="4ebd9-120">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="4ebd9-121">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4ebd9-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





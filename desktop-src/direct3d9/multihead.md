---
description: Le schede Multihead sono quelle con un acceleratore e un acceleratore di frame, indipendenti da Digital a analogico (DAC), e monitorano gli output.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481300"
---
# <a name="multihead-direct3d-9"></a><span data-ttu-id="ffd52-103">Multihead (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ffd52-103">Multihead (Direct3D 9)</span></span>

<span data-ttu-id="ffd52-104">Le schede Multihead sono quelle con un acceleratore e un acceleratore di frame, indipendenti da Digital a analogico (DAC), e monitorano gli output.</span><span class="sxs-lookup"><span data-stu-id="ffd52-104">Multihead cards are those that have a common frame buffer and accelerator, independent digital-to-analog converters (DACs), and monitor outputs.</span></span> <span data-ttu-id="ffd52-105">Tali dispositivi possono offrire un supporto più usabile per più monitor rispetto a un numero simile di schede di visualizzazione eterogenee.</span><span class="sxs-lookup"><span data-stu-id="ffd52-105">Such devices can offer much more usable multiple monitor support than a similar number of heterogeneous display adapters.</span></span>

<span data-ttu-id="ffd52-106">Le schede Multihead sono esposte nell'API come un singolo dispositivo a livello di API che può guidare diverse catene di scambio a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ffd52-106">Multihead cards are exposed in the API as a single API-level device that can drive several full-screen swap chains.</span></span> <span data-ttu-id="ffd52-107">Di conseguenza, tutte le risorse vengono condivise con tutte le intestazioni e ogni Head ha esattamente le stesse funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ffd52-107">Consequently, all resources are shared with all the heads, and each head has exactly the same capabilities.</span></span> <span data-ttu-id="ffd52-108">Ogni intestazione può essere impostata su modalità di visualizzazione indipendente.</span><span class="sxs-lookup"><span data-stu-id="ffd52-108">Each head can be set to independent display modes.</span></span> <span data-ttu-id="ffd52-109">È possibile usare chiamate separate a [**IDirect3DSwapChain9::P inviato nuovamente**](/windows/desktop/api) per aggiornare ogni Head.</span><span class="sxs-lookup"><span data-stu-id="ffd52-109">You can use separate calls to [**IDirect3DSwapChain9::Present**](/windows/desktop/api) to refresh each head.</span></span> <span data-ttu-id="ffd52-110">È anche possibile usare una sola chiamata a [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) per aggiornare ogni Head in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="ffd52-110">You can also use one call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) to refresh each head sequentially.</span></span>

> [!Note]  
> <span data-ttu-id="ffd52-111">L'aggiornamento di ogni Head non si verifica contemporaneamente con una singola chiamata a [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="ffd52-111">The refresh of each head does not occur simultaneously with a single call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="ffd52-112">Le statistiche presenti in Direct3D 9Ex possono utilizzare la struttura [**D3DPRESENTSTATS**](d3dpresentstats.md) per limitare gli aggiornamenti a ogni capo vicino per limitare gli effetti di strappo tra più intestazioni degli adapter.</span><span class="sxs-lookup"><span data-stu-id="ffd52-112">Present statistics in Direct3D 9Ex can use the [**D3DPRESENTSTATS**](d3dpresentstats.md) structure to keep the refreshes to each head close to each other to limit tearing effects across multiple heads of adapters.</span></span> <span data-ttu-id="ffd52-113">Per informazioni sulla sincronizzazione dei frame delle applicazioni Direct3D 9Ex flip model, vedere la pagina relativa ai [miglioramenti di Direct3D 9Ex](../direct3darticles/direct3d-9ex-improvements.md).</span><span class="sxs-lookup"><span data-stu-id="ffd52-113">For information about synchronizing frames of Direct3D 9Ex flip model applications, see [Direct3D 9Ex Improvements](../direct3darticles/direct3d-9ex-improvements.md).</span></span>

 

<span data-ttu-id="ffd52-114">Ogni catena di scambio per un dispositivo Multihead deve essere a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ffd52-114">Each swap chain for a multihead device must be full screen.</span></span> <span data-ttu-id="ffd52-115">Quando un dispositivo è entrato in modalità multihead, deve rimanere a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ffd52-115">When a device has entered multihead mode, it must remain full screen.</span></span> <span data-ttu-id="ffd52-116">La transizione alla modalità finestra richiede l'eliminazione del dispositivo (ad eccezione della normale operazione ALT + TAB-to-minimizza).</span><span class="sxs-lookup"><span data-stu-id="ffd52-116">The transition back to windowed mode requires the destruction of the device (except for the normal ALT+TAB-to-minimize operation).</span></span>

<span data-ttu-id="ffd52-117">Il metodo precedente per suddividere la memoria video tra le teste e considerare ogni capo come un acceleratore completamente indipendente sarà comunque uno scenario di utilizzo comune.</span><span class="sxs-lookup"><span data-stu-id="ffd52-117">The old method of dividing video memory between the heads and treating each head as a fully independent accelerator will still be a common usage scenario.</span></span> <span data-ttu-id="ffd52-118">Questa proposta non sostituisce questo meccanismo, a meno che l'applicazione non sia stata codificata in modo specifico per funzionare in modalità Multihead Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ffd52-118">This proposal does not replace that mechanism unless the application has been specifically coded to function in the Direct3D 9 multihead mode.</span></span>

<span data-ttu-id="ffd52-119">Ai driver viene assegnata una conoscenza adeguata per passare tra le due modalità operative.</span><span class="sxs-lookup"><span data-stu-id="ffd52-119">Drivers are given adequate knowledge to switch between the two modes of operation.</span></span>

<span data-ttu-id="ffd52-120">Una testa verrà chiamata intestazione master e tutte le altre teste sulla stessa scheda verranno denominate intestazioni subordinate.</span><span class="sxs-lookup"><span data-stu-id="ffd52-120">One head will be called the master head, and all other heads on the same card be called subordinate heads.</span></span> <span data-ttu-id="ffd52-121">Se in un sistema è presente più di un adattatore multihead, il database master e i relativi subordinati di un adattatore Multihead vengono chiamati gruppi.</span><span class="sxs-lookup"><span data-stu-id="ffd52-121">If more than one multihead adapter is present in a system, the master and its subordinates from one multihead adapter are called a group.</span></span> <span data-ttu-id="ffd52-122">I gruppi sono identificati dall'ordinale dell'adapter della testa master.</span><span class="sxs-lookup"><span data-stu-id="ffd52-122">Groups are denoted by the adapter ordinal of their master head.</span></span>

<span data-ttu-id="ffd52-123">La struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) è stata aggiornata per esporre i nuovi tappi hardware seguenti.</span><span class="sxs-lookup"><span data-stu-id="ffd52-123">The [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure has been updated to expose the following new hardware caps.</span></span>


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   <span data-ttu-id="ffd52-124">NumberOfAdaptersInGroup è 1 per gli adapter convenzionali e maggiore di 1 per l'adattatore Master di una scheda Multihead.</span><span class="sxs-lookup"><span data-stu-id="ffd52-124">NumberOfAdaptersInGroup is 1 for conventional adapters, and greater than 1 for the master adapter of a multihead card.</span></span> <span data-ttu-id="ffd52-125">Il valore sarà 0 per un adapter subordinato di una scheda Multihead.</span><span class="sxs-lookup"><span data-stu-id="ffd52-125">The value will be 0 for a subordinate adapter of a multihead card.</span></span> <span data-ttu-id="ffd52-126">Ogni scheda può avere al massimo un master, ma potrebbe avere molti subordinati.</span><span class="sxs-lookup"><span data-stu-id="ffd52-126">Each card can have at most one master, but might have many subordinates.</span></span>
-   <span data-ttu-id="ffd52-127">MasterAdapterOrdinal indica quale dispositivo è il master per questo subordinato.</span><span class="sxs-lookup"><span data-stu-id="ffd52-127">MasterAdapterOrdinal indicates which device is the master for this subordinate.</span></span>
-   <span data-ttu-id="ffd52-128">AdapterOrdinalInGroup indica l'ordine in cui le intestazioni fanno riferimento all'API.</span><span class="sxs-lookup"><span data-stu-id="ffd52-128">AdapterOrdinalInGroup indicates the order in which heads are referenced by the API.</span></span> <span data-ttu-id="ffd52-129">L'adapter Master ha sempre AdapterOrdinalInGroup 0.</span><span class="sxs-lookup"><span data-stu-id="ffd52-129">The master adapter always has AdapterOrdinalInGroup 0.</span></span> <span data-ttu-id="ffd52-130">Questi valori non corrispondono ai numeri ordinali degli adapter passati ai metodi IDirect3D9, ma si applicano solo alle intestazioni all'interno di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="ffd52-130">These values do not correspond to the adapter ordinals passed to the IDirect3D9 methods, but apply only to heads within a group.</span></span>

<span data-ttu-id="ffd52-131">Questa definizione consente alle schede Multihead di continuare a presentare più schede come se fossero schede indipendenti, proprio come in DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="ffd52-131">This definition allows multihead cards to continue to present multiple adapters as if they were independent cards, just as they did in DirectX 8.</span></span>

<span data-ttu-id="ffd52-132">Per creare un dispositivo multihead, specificare il flag di comportamento D3DCREATE \_ ADAPTERGROUP \_ Device in [**IDirect3D9:: CreateDevice**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ffd52-132">To create a multihead device, specify the behavior flag D3DCREATE\_ADAPTERGROUP\_DEVICE in [**IDirect3D9::CreateDevice**](/windows/desktop/api).</span></span> <span data-ttu-id="ffd52-133">I parametri di presentazione, ovvero una matrice di [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md), devono contenere elementi NumberOfAdaptersInGroup.</span><span class="sxs-lookup"><span data-stu-id="ffd52-133">The presentation parameters (an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md)) should contain NumberOfAdaptersInGroup elements.</span></span> <span data-ttu-id="ffd52-134">Il runtime assegnerà ogni elemento a ogni Head in ordine numerico AdapterOrdinalInGroup.</span><span class="sxs-lookup"><span data-stu-id="ffd52-134">The runtime will assign each element to each head in AdapterOrdinalInGroup numerical order.</span></span> <span data-ttu-id="ffd52-135">Quando \_ \_ viene impostato il dispositivo D3DCREATE ADAPTERGROUP, ogni parametro Presentation deve avere:</span><span class="sxs-lookup"><span data-stu-id="ffd52-135">When D3DCREATE\_ADAPTERGROUP\_DEVICE is set, each presentation parameter must have:</span></span>

-   <span data-ttu-id="ffd52-136">Il membro a finestra è impostato su **false** (in altre parole, deve essere a schermo intero).</span><span class="sxs-lookup"><span data-stu-id="ffd52-136">The Windowed member set to **FALSE** (in other words, be full screen).</span></span>
-   <span data-ttu-id="ffd52-137">Lo stesso valore per il membro EnableAutoDepthStencil dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ffd52-137">The same value for the EnableAutoDepthStencil member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="ffd52-138">Inoltre, se EnableAutoDepthStencil è **true**, ognuno dei campi seguenti deve avere lo stesso valore per ogni [**\_ parametro D3DPRESENT**](d3dpresent-parameters.md):</span><span class="sxs-lookup"><span data-stu-id="ffd52-138">In addition, if EnableAutoDepthStencil is **TRUE**, then each of the following fields must have the same value for each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md):</span></span>

-   <span data-ttu-id="ffd52-139">AutoDepthStencilFormat</span><span class="sxs-lookup"><span data-stu-id="ffd52-139">AutoDepthStencilFormat</span></span>
-   <span data-ttu-id="ffd52-140">BackBufferWidth</span><span class="sxs-lookup"><span data-stu-id="ffd52-140">BackBufferWidth</span></span>
-   <span data-ttu-id="ffd52-141">BackBufferHeight</span><span class="sxs-lookup"><span data-stu-id="ffd52-141">BackBufferHeight</span></span>
-   <span data-ttu-id="ffd52-142">BackBufferFormat</span><span class="sxs-lookup"><span data-stu-id="ffd52-142">BackBufferFormat</span></span>

<span data-ttu-id="ffd52-143">Se è impostata l'applicazione livello dati, le chiamate aggiuntive a [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) non sono valide.</span><span class="sxs-lookup"><span data-stu-id="ffd52-143">If DAC is set, additional calls to [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) are illegal.</span></span>

<span data-ttu-id="ffd52-144">Se il dispositivo è stato creato con l'applicazione livello dati, [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) prevede una matrice di [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ffd52-144">If the device was created with the DAC, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) will expect an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="ffd52-145">Ogni struttura di [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) passata a [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) deve essere a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ffd52-145">Each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure passed to [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) must be full screen.</span></span> <span data-ttu-id="ffd52-146">Per tornare alla modalità finestra, l'applicazione deve eliminare definitivamente il dispositivo e ricreare un dispositivo non multiparte in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="ffd52-146">To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.</span></span>

<span data-ttu-id="ffd52-147">Di seguito è riportato uno scenario di utilizzo di base:</span><span class="sxs-lookup"><span data-stu-id="ffd52-147">Here is a basic usage scenario:</span></span>


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



<span data-ttu-id="ffd52-148">Per ulteriori informazioni, vedere [**IDirect3D9:: CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9:: GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span><span class="sxs-lookup"><span data-stu-id="ffd52-148">For more information, see [**IDirect3D9::CreateDevice**](/windows/desktop/api) and [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffd52-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ffd52-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffd52-150">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="ffd52-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 

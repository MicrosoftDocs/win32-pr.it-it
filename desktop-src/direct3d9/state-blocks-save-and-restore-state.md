---
description: Un blocco di stato è un gruppo di Stati del dispositivo.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Stato di salvataggio e ripristino di blocchi di stato (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965462"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a><span data-ttu-id="051e6-103">Stato di salvataggio e ripristino di blocchi di stato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="051e6-103">State Blocks Save and Restore State (Direct3D 9)</span></span>

<span data-ttu-id="051e6-104">Un blocco di stato è un gruppo di Stati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="051e6-104">A state block is a group of device states.</span></span> <span data-ttu-id="051e6-105">Lo stato del dispositivo è costituito dallo stato di rendering, dallo stato del vertice, dallo stato dei pixel o da tutti i precedenti.</span><span class="sxs-lookup"><span data-stu-id="051e6-105">Device state is made up of render state, vertex state, pixel state, or all of the above.</span></span> <span data-ttu-id="051e6-106">Un blocco di stato contiene uno snapshot dello stato corrente di un dispositivo oppure è possibile creare un blocco di stato che registra ogni modifica dello stato apportata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="051e6-106">A state block contains a snapshot of a device's current state, or you can create a state block that records each state change that your application makes.</span></span>

## <a name="capture-a-block-of-state"></a><span data-ttu-id="051e6-107">Acquisisci un blocco di stato</span><span class="sxs-lookup"><span data-stu-id="051e6-107">Capture a Block of State</span></span>

<span data-ttu-id="051e6-108">Scegliere il tipo di stato che si desidera acquisire e creare un blocco di stato simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="051e6-108">Choose the type of state that you want to capture, and create a state block like this:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



<span data-ttu-id="051e6-109">[**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) crea un blocco di stato e acquisisce automaticamente lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="051e6-109">[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) creates a state block, and automatically captures the device state.</span></span> <span data-ttu-id="051e6-110">Lo stato del dispositivo viene specificato dal tipo di blocco di stato nel primo argomento.</span><span class="sxs-lookup"><span data-stu-id="051e6-110">The device state is specified by the state block type in the first argument.</span></span> <span data-ttu-id="051e6-111">Questo stato può essere uno dei seguenti: tutti gli Stati del dispositivo (vedere [salvare tutti gli Stati dei dispositivi con StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), tutti i pixel (vedere [salvataggio dello stato dei pixel con StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) o tutto lo stato del vertice (vedere [salvataggio degli Stati dei vertici con un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="051e6-111">This state can be one of the following: all device state (see [Saving All Device States with a StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), all pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)), or all vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>

<span data-ttu-id="051e6-112">Il sistema degli effetti usa un blocco di stato per salvare lo stato.</span><span class="sxs-lookup"><span data-stu-id="051e6-112">The effect system uses a state block to save state.</span></span> <span data-ttu-id="051e6-113">Dopo la chiamata di [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) , viene creato un blocco di stato e viene acquisito lo stato.</span><span class="sxs-lookup"><span data-stu-id="051e6-113">After [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called, a state block is created and state is captured.</span></span> <span data-ttu-id="051e6-114">Quando viene chiamato [**ID3DXEffect:: end**](id3dxeffect--end.md) , lo stato del blocco di stato viene riapplicato al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="051e6-114">When [**ID3DXEffect::End**](id3dxeffect--end.md) is called, the state block state is reapplied to the device.</span></span>

## <a name="capture-individual-states"></a><span data-ttu-id="051e6-115">Acquisisci singoli Stati</span><span class="sxs-lookup"><span data-stu-id="051e6-115">Capture Individual States</span></span>

<span data-ttu-id="051e6-116">Per salvare una sequenza di stato personalizzata, eseguire il wrapping dello stato che si desidera salvare in una coppia [**IDirect3DDevice9:: BeginStateBlock**](/windows/desktop/api) e [**IDirect3DDevice9:: EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) .</span><span class="sxs-lookup"><span data-stu-id="051e6-116">To save a custom state sequence, wrap the state that you want to save in a [**IDirect3DDevice9::BeginStateBlock**](/windows/desktop/api) and [**IDirect3DDevice9::EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) pair.</span></span> <span data-ttu-id="051e6-117">BeginStateBlock indica al dispositivo corrente di impostare un blocco di stato e aggiungervi tutte le modifiche di stato che si verificano fino a quando non viene chiamato EndStateBlock.</span><span class="sxs-lookup"><span data-stu-id="051e6-117">BeginStateBlock tells the current device to set up a state block and add to it every state change that occurs until EndStateBlock is called.</span></span> <span data-ttu-id="051e6-118">Ecco un esempio:</span><span class="sxs-lookup"><span data-stu-id="051e6-118">Here's an example:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



<span data-ttu-id="051e6-119">In questo modo si salva un numero qualsiasi di modifiche di stato in qualsiasi sequenza in un stateblock personalizzato.</span><span class="sxs-lookup"><span data-stu-id="051e6-119">This will save any number of state changes in any sequence to a custom stateblock.</span></span> <span data-ttu-id="051e6-120">In seguito, quando si vuole usare stateblock per reimpostare lo stato del dispositivo, chiamare [**IDirect3DStateBlock9:: Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span><span class="sxs-lookup"><span data-stu-id="051e6-120">Later, when you want to use the stateblock to reset the device state, call [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span></span> <span data-ttu-id="051e6-121">Questa operazione sovrascriverà solo lo stato del dispositivo acquisito nel blocco di stato.</span><span class="sxs-lookup"><span data-stu-id="051e6-121">This will overwrite only the device state that has been captured in the state block.</span></span> <span data-ttu-id="051e6-122">Qualsiasi altro stato del dispositivo che non è stato acquisito con il stateblock personalizzato non verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="051e6-122">Any other device state that was not captured with the custom stateblock will not be changed.</span></span> <span data-ttu-id="051e6-123">Ancora una volta, poiché l'oggetto stateblock è un'interfaccia, sarà necessario rilasciarlo al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="051e6-123">Once again, since the stateblock object is an interface, you will need to release it when you are done with it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="051e6-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="051e6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="051e6-125">Stati (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="051e6-125">States (Direct3D 9)</span></span>](states.md)
</dt> </dl>

 

 

---
description: Un blocco di stato può essere usato per acquisire tutti gli Stati dei dispositivi. vedere lo stato di salvataggio e ripristino dei blocchi di stato (Direct3D 9).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Salvataggio di tutti gli Stati dei dispositivi con StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304194"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="d0a39-103">Salvataggio di tutti gli Stati dei dispositivi con StateBlock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d0a39-103">Saving All Device States with a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="d0a39-104">Un blocco di stato può essere usato per acquisire tutti gli Stati dei dispositivi. vedere lo [stato di salvataggio e ripristino dei blocchi di stato (Direct3D 9)](state-blocks-save-and-restore-state.md).</span><span class="sxs-lookup"><span data-stu-id="d0a39-104">A state block can be used to capture all device states (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="d0a39-105">Gli elementi di stato seguenti sono inclusi nello stato del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="d0a39-105">The following state elements are included in the device state:</span></span>

-   <span data-ttu-id="d0a39-106">Stato vertice (vedere [salvataggio degli Stati dei vertici con StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="d0a39-106">Vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="d0a39-107">Stato dei pixel (vedere [salvataggio dello stato dei pixel con StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="d0a39-107">Pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="d0a39-108">Ogni trama assegnata a un campionatore.</span><span class="sxs-lookup"><span data-stu-id="d0a39-108">Each texture assigned to a sampler.</span></span>
-   <span data-ttu-id="d0a39-109">Ogni trama del vertice.</span><span class="sxs-lookup"><span data-stu-id="d0a39-109">Each vertex texture.</span></span>
-   <span data-ttu-id="d0a39-110">Trama della mappa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="d0a39-110">Each displacement map texture.</span></span>
-   <span data-ttu-id="d0a39-111">Tavolozza di trama corrente.</span><span class="sxs-lookup"><span data-stu-id="d0a39-111">The current texture palette.</span></span>
-   <span data-ttu-id="d0a39-112">Per ogni flusso di vertici: un puntatore al buffer dei vertici, ogni argomento di [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api)e il divisore, se presente, da [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="d0a39-112">For each vertex stream: a pointer to the vertex buffer, each argument from [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api), and the divider (if any) from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="d0a39-113">Puntatore al buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="d0a39-113">A pointer to the index buffer.</span></span>
-   <span data-ttu-id="d0a39-114">Viewport.</span><span class="sxs-lookup"><span data-stu-id="d0a39-114">The viewport.</span></span>
-   <span data-ttu-id="d0a39-115">Rettangolo a forbice.</span><span class="sxs-lookup"><span data-stu-id="d0a39-115">The scissors rectangle.</span></span>
-   <span data-ttu-id="d0a39-116">Matrici internazionali, di visualizzazione e di proiezione.</span><span class="sxs-lookup"><span data-stu-id="d0a39-116">The world, view, and projection matrices.</span></span>
-   <span data-ttu-id="d0a39-117">Trasformazioni della trama.</span><span class="sxs-lookup"><span data-stu-id="d0a39-117">The texture transforms.</span></span>
-   <span data-ttu-id="d0a39-118">Eventuali piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="d0a39-118">The clipping planes (if any).</span></span>
-   <span data-ttu-id="d0a39-119">Materiale corrente.</span><span class="sxs-lookup"><span data-stu-id="d0a39-119">The current material.</span></span>

<span data-ttu-id="d0a39-120">Per acquisire tutti gli Stati del dispositivo con un blocco di stato, specificare D3DSBT \_ all durante la chiamata a [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="d0a39-120">To capture all device states with a state block, specify D3DSBT\_ALL when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0a39-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0a39-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0a39-122">Stato di salvataggio e ripristino del blocco di stato</span><span class="sxs-lookup"><span data-stu-id="d0a39-122">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 

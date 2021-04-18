---
description: Il buffering di profondità è un metodo per rimuovere le linee e le superfici nascoste. Per impostazione predefinita, Direct3D non usa la memorizzazione nel buffer di profondità.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Stato buffering profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481556"
---
# <a name="depth-buffering-state-direct3d-9"></a><span data-ttu-id="83ca4-104">Stato buffering profondità (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83ca4-104">Depth Buffering State (Direct3D 9)</span></span>

<span data-ttu-id="83ca4-105">Il buffering di profondità è un metodo per rimuovere le linee e le superfici nascoste.</span><span class="sxs-lookup"><span data-stu-id="83ca4-105">Depth buffering is a method of removing hidden lines and surfaces.</span></span> <span data-ttu-id="83ca4-106">Per impostazione predefinita, Direct3D non usa la memorizzazione nel buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="83ca4-106">By default, Direct3D does not use depth buffering.</span></span>

<span data-ttu-id="83ca4-107">Per una panoramica concettuale dei buffer di profondità, vedere [buffer di profondità (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="83ca4-107">For a conceptual overview of depth buffers, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="83ca4-108">Le applicazioni C++ aggiornano lo stato di buffering di profondità con lo \_ stato di rendering ZENABLE di D3DRS, usando un membro dell'enumerazione [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) per specificare il nuovo valore di stato.</span><span class="sxs-lookup"><span data-stu-id="83ca4-108">C++ applications update the depth-buffering state with the D3DRS\_ZENABLE render state, using a member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumeration to specify the new state value.</span></span>

<span data-ttu-id="83ca4-109">Se l'applicazione deve impedire a Direct3D di scrivere nel buffer di profondità, può usare il \_ valore enumerato D3DRS ZWRITEENABLE, specificando D3DZB \_ false come secondo parametro per la chiamata a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="83ca4-109">If your application needs to prevent Direct3D from writing to the depth buffer, it can use the D3DRS\_ZWRITEENABLE enumerated value, specifying D3DZB\_FALSE as the second parameter for the call to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="83ca4-110">Nell'esempio di codice seguente viene illustrato come impostare lo stato del buffer di profondità per abilitare il buffer z.</span><span class="sxs-lookup"><span data-stu-id="83ca4-110">The following code example shows how the depth-buffer state is set to enable z-buffering.</span></span>


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



<span data-ttu-id="83ca4-111">L'applicazione può anche usare lo \_ stato di rendering ZFUNC di D3DRS per controllare la funzione di confronto utilizzata da Direct3D durante l'esecuzione del buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="83ca4-111">Your application can also use the D3DRS\_ZFUNC render state to control the comparison function that Direct3D uses when performing depth buffering.</span></span>

<span data-ttu-id="83ca4-112">La distorsione Z è un metodo di visualizzazione di una superficie davanti a un'altra, anche se i valori di profondità sono uguali.</span><span class="sxs-lookup"><span data-stu-id="83ca4-112">Z-biasing is a method of displaying one surface in front of another, even if their depth values are the same.</span></span> <span data-ttu-id="83ca4-113">È possibile utilizzare questa tecnica per diversi effetti.</span><span class="sxs-lookup"><span data-stu-id="83ca4-113">You can use this technique for a variety of effects.</span></span> <span data-ttu-id="83ca4-114">Un esempio comune è il rendering di ombre sulle pareti.</span><span class="sxs-lookup"><span data-stu-id="83ca4-114">A common example is rendering shadows on walls.</span></span> <span data-ttu-id="83ca4-115">Sia l'ombreggiatura che la parete hanno lo stesso valore di profondità.</span><span class="sxs-lookup"><span data-stu-id="83ca4-115">Both the shadow and the wall have the same depth value.</span></span> <span data-ttu-id="83ca4-116">Tuttavia, si desidera che l'applicazione mostri l'ombreggiatura sulla parete.</span><span class="sxs-lookup"><span data-stu-id="83ca4-116">However, you want your application to show the shadow on the wall.</span></span> <span data-ttu-id="83ca4-117">Se si assegna una polarizzazione z all'ombreggiatura, Direct3D li visualizza correttamente (vedere D3DRS \_ DEPTHBIAS).</span><span class="sxs-lookup"><span data-stu-id="83ca4-117">Giving a z-bias to the shadow makes Direct3D display them properly (see D3DRS\_DEPTHBIAS).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83ca4-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83ca4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83ca4-119">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="83ca4-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 

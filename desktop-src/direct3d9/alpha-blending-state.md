---
description: Il valore alfa di un colore ne controlla la trasparenza. L'abilitazione della fusione alfa consente la fusione di colori, materiali e trame in una superficie con trasparenza su un'altra superficie.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Stato di fusione alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401460"
---
# <a name="alpha-blending-state-direct3d-9"></a><span data-ttu-id="dc9f6-104">Stato di fusione alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc9f6-104">Alpha Blending State (Direct3D 9)</span></span>

<span data-ttu-id="dc9f6-105">Il valore alfa di un colore ne controlla la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-105">The alpha value of a color controls its transparency.</span></span> <span data-ttu-id="dc9f6-106">L'abilitazione della fusione alfa consente la fusione di colori, materiali e trame in una superficie con trasparenza su un'altra superficie.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-106">Enabling alpha blending allows colors, materials, and textures on a surface to be blended with transparency onto another surface.</span></span>

<span data-ttu-id="dc9f6-107">Per altre informazioni, vedere [Alpha texture blending (Direct3D 9)](alpha-texture-blending.md) e [blending di trame (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="dc9f6-107">For more information, see [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) and [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

<span data-ttu-id="dc9f6-108">Le applicazioni scritte in C++ usano lo stato di rendering [**\_ ALPHABLENDENABLE di D3DRS**](./d3drenderstatetype.md) per abilitare la sfumatura di trasparenza alfa.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-108">Applications written in C++ use the [**D3DRS\_ALPHABLENDENABLE**](./d3drenderstatetype.md) render state to enable alpha transparency blending.</span></span> <span data-ttu-id="dc9f6-109">L'API Direct3D consente molti tipi di fusione alfa.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-109">The Direct3D API allows many types of alpha blending.</span></span> <span data-ttu-id="dc9f6-110">Tuttavia, è importante notare che l'hardware 3D dell'utente potrebbe non supportare tutti gli Stati di fusione consentiti da Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-110">However, it is important to note the user's 3D hardware might not support all the blending states allowed by Direct3D.</span></span>

<span data-ttu-id="dc9f6-111">Il tipo di fusione alfa eseguita dipende dagli Stati di rendering [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) e **D3DRS \_ DESTBLEND** .</span><span class="sxs-lookup"><span data-stu-id="dc9f6-111">The type of alpha blending that is done depends on the [**D3DRS\_SRCBLEND**](./d3drenderstatetype.md) And **D3DRS\_DESTBLEND** render states.</span></span> <span data-ttu-id="dc9f6-112">Gli Stati di Blend di origine e di destinazione vengono utilizzati nelle coppie.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-112">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="dc9f6-113">Nell'esempio di codice riportato di seguito viene illustrato il modo in cui lo stato di Blend di origine è impostato su D3DBLEND \_ SRCCOLOR e lo stato di Blend di destinazione è impostato su D3DBLEND \_ INVSRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-113">The following code example demonstrates how the source blend state is set to D3DBLEND\_SRCCOLOR and the destination blend state is set to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="dc9f6-114">La modifica degli Stati di Blend di origine e di destinazione può fornire l'aspetto degli oggetti emissivo in un'atmosfera nebbiosa o polverosa.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-114">Altering the source and destination blend states can give the appearance of emissive objects in a foggy or dusty atmosphere.</span></span> <span data-ttu-id="dc9f6-115">Ad esempio, se l'applicazione modella le fiamme, forza i campi, i Beam plasmatici o gli oggetti radianti allo stesso modo in un ambiente nebbioso, impostare gli Stati di Blend di origine e di destinazione su D3DBLEND \_ One.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-115">For instance, if your application models flames, force fields, plasma beams, or similarly radiant objects in a foggy environment, set the source and destination blend states to D3DBLEND\_ONE.</span></span>

<span data-ttu-id="dc9f6-116">Un'altra applicazione di fusione alfa consiste nel controllare l'illuminazione in una scena 3D, denominata anche Light Mapping.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-116">Another application of alpha blending is to control the lighting in a 3D scene, also called light mapping.</span></span> <span data-ttu-id="dc9f6-117">Impostando lo stato di Blend di origine su D3DBLEND \_ zero e lo stato di Blend di destinazione su D3DBLEND \_ SRCALPHA, una scena viene offuscata in base alle informazioni alfa di origine.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-117">Setting the source blend state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCALPHA darkens a scene according to the source alpha information.</span></span> <span data-ttu-id="dc9f6-118">La primitiva di origine viene usata come mappa chiara che ridimensiona il contenuto del buffer del frame per scurirlo quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-118">The source primitive is used as a light map that scales the contents of the frame buffer to darken it when appropriate.</span></span> <span data-ttu-id="dc9f6-119">Questo produce un mapping chiaro monocromatico.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-119">This produces monochrome light mapping.</span></span>

<span data-ttu-id="dc9f6-120">È possibile ottenere il mapping della luce dei colori impostando lo stato di fusione alfa di origine su D3DBLEND \_ zero e lo stato di Blend di destinazione su D3DBLEND \_ SRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="dc9f6-120">You can achieve color light mapping by setting the source alpha blending state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCCOLOR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc9f6-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc9f6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc9f6-122">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="dc9f6-122">Render States</span></span>](render-states.md)
</dt> </dl>

 

 

---
description: Viene eseguito il rendering delle primitive senza trame con il colore specificato dal materiale o con i colori specificati per i vertici, se presenti.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Stato di riempimento e contorno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303800"
---
# <a name="outline-and-fill-state-direct3d-9"></a><span data-ttu-id="0ff59-103">Stato di riempimento e contorno (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0ff59-103">Outline and Fill State (Direct3D 9)</span></span>

<span data-ttu-id="0ff59-104">Viene eseguito il rendering delle primitive senza trame con il colore specificato dal materiale o con i colori specificati per i vertici, se presenti.</span><span class="sxs-lookup"><span data-stu-id="0ff59-104">Primitives that have no textures are rendered with the color specified by their material, or with the colors specified for the vertices, if any.</span></span> <span data-ttu-id="0ff59-105">È possibile selezionare il metodo per riempirli specificando un valore definito dal tipo enumerato [**D3DFILLMODE**](./d3dfillmode.md) per lo stato di \_ rendering D3DRS FillMode.</span><span class="sxs-lookup"><span data-stu-id="0ff59-105">You can select the method to fill them by specifying a value defined by the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type for the D3DRS\_FILLMODE render state.</span></span>

<span data-ttu-id="0ff59-106">Per abilitare la rethering, l'applicazione deve passare il \_ valore enumerato D3DRS DITHERENABLE come primo parametro a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="0ff59-106">To enable dithering, your application must pass the D3DRS\_DITHERENABLE enumerated value as the first parameter to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span> <span data-ttu-id="0ff59-107">Deve impostare il secondo parametro su **true** per abilitare la dithering e **false** per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="0ff59-107">It must set the second parameter to **TRUE** to enable dithering, and **FALSE** to disable it.</span></span>

<span data-ttu-id="0ff59-108">In alcuni casi, il disegno dell'ultimo pixel in una riga può causare una sovrapposizione approfondita con le primitive circostanti.</span><span class="sxs-lookup"><span data-stu-id="0ff59-108">At times, drawing the last pixel in a line can cause unsightly overlap with surrounding primitives.</span></span> <span data-ttu-id="0ff59-109">È possibile controllare questa operazione usando il \_ valore enumerato di D3DRS LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="0ff59-109">You can control this using the D3DRS\_LASTPIXEL enumerated value.</span></span> <span data-ttu-id="0ff59-110">Tuttavia, non modificare questa impostazione senza alcuna premeditazione.</span><span class="sxs-lookup"><span data-stu-id="0ff59-110">However, do not alter this setting without some forethought.</span></span> <span data-ttu-id="0ff59-111">In alcune condizioni, la disattivazione del rendering dell'ultimo pixel può causare Gap non visivi tra primitive.</span><span class="sxs-lookup"><span data-stu-id="0ff59-111">Under some conditions, suppressing the rendering of the last pixel can cause unsightly gaps between primitives.</span></span>

<span data-ttu-id="0ff59-112">È possibile disegnare le strutture degli oggetti impostando il modello di disegno a linee appropriato.</span><span class="sxs-lookup"><span data-stu-id="0ff59-112">Object outlines can be drawn by setting the appropriate line drawing pattern.</span></span> <span data-ttu-id="0ff59-113">Lo stato predefinito di disegno della linea consiste nel disegnare linee continue.</span><span class="sxs-lookup"><span data-stu-id="0ff59-113">The default line drawing state is to draw solid lines.</span></span> <span data-ttu-id="0ff59-114">Per altre informazioni, vedere [supporto per la creazione di linee nello stato di rendering D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff59-114">For more information, see [Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) render state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ff59-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ff59-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ff59-116">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="0ff59-116">Render States</span></span>](render-states.md)
</dt> </dl>

 

 

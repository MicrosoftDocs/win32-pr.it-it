---
description: La fusione alfa del buffer dei frame è leggermente diversa da quella del vertice Alpha, dal materiale Alfa e dalla trama alfa.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Buffer frame alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123858"
---
# <a name="frame-buffer-alpha-direct3d-9"></a><span data-ttu-id="fb078-103">Buffer frame alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fb078-103">Frame Buffer Alpha (Direct3D 9)</span></span>

<span data-ttu-id="fb078-104">La fusione alfa del buffer dei frame è leggermente diversa da quella del vertice Alpha, dal materiale Alfa e dalla trama alfa.</span><span class="sxs-lookup"><span data-stu-id="fb078-104">Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha.</span></span> <span data-ttu-id="fb078-105">Il vertice, il materiale e l'alfa di trama impostano i valori di trasparenza usati solo per la primitiva corrente e non hanno alcun effetto su altre primitive.</span><span class="sxs-lookup"><span data-stu-id="fb078-105">Vertex, material, and texture alpha set transparency values that are used only for the current primitive, and by themselves have no effect on other primitives.</span></span> <span data-ttu-id="fb078-106">La fusione alfa del buffer dei frame controlla il modo in cui la primitiva corrente viene combinata con i pixel esistenti nel buffer del frame per produrre un colore finale del pixel.</span><span class="sxs-lookup"><span data-stu-id="fb078-106">Frame buffer alpha-blending controls how the current primitive is combined with existing pixels in the frame buffer to yield a final pixel color.</span></span>

<span data-ttu-id="fb078-107">Quando si esegue la fusione alfa, vengono combinati due colori: un colore di origine e un colore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fb078-107">When performing alpha blending, two colors are being combined: a source color and a destination color.</span></span> <span data-ttu-id="fb078-108">Il colore di origine è dall'oggetto trasparente, il colore di destinazione è il colore già presente nella posizione dei pixel.</span><span class="sxs-lookup"><span data-stu-id="fb078-108">The source color is from the transparent object, the destination color is the color already at the pixel location.</span></span> <span data-ttu-id="fb078-109">Il colore di destinazione è il risultato del rendering di un altro oggetto dietro l'oggetto trasparente, ovvero l'oggetto che sarà visibile tramite l'oggetto trasparente.</span><span class="sxs-lookup"><span data-stu-id="fb078-109">The destination color is the result of rendering some other object that is behind the transparent object, that is, the object that will be visible through the transparent object.</span></span> <span data-ttu-id="fb078-110">La fusione alfa usa una formula per controllare il rapporto tra gli oggetti di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fb078-110">Alpha blending uses a formula to control the ratio between the source and destination objects.</span></span>


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



<span data-ttu-id="fb078-111">ObjectColor è il contributo della primitiva di cui viene eseguito il rendering nella posizione del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="fb078-111">ObjectColor is the contribution from the primitive being rendered at the current pixel location.</span></span> <span data-ttu-id="fb078-112">PixelColor è il contributo del buffer dei frame nella posizione del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="fb078-112">PixelColor is the contribution from the frame buffer at the current pixel location.</span></span>

<span data-ttu-id="fb078-113">Il set di fattori di blend alfa che è possibile usare è riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="fb078-113">The set of alpha blend factors that can be used are listed below.</span></span>



| <span data-ttu-id="fb078-114">Fattore modalità Blend</span><span class="sxs-lookup"><span data-stu-id="fb078-114">Blend mode factor</span></span>         | <span data-ttu-id="fb078-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb078-115">Description</span></span>                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb078-116">D3DBLEND \_ zero</span><span class="sxs-lookup"><span data-stu-id="fb078-116">D3DBLEND\_ZERO</span></span>            | <span data-ttu-id="fb078-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="fb078-117">(0, 0, 0, 0)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="fb078-118">D3DBLEND \_ One</span><span class="sxs-lookup"><span data-stu-id="fb078-118">D3DBLEND\_ONE</span></span>             | <span data-ttu-id="fb078-119">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="fb078-119">(1, 1, 1, 1)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="fb078-120">\_SRCCOLOR D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-120">D3DBLEND\_SRCCOLOR</span></span>        | <span data-ttu-id="fb078-121">(RS, GS, BS, As)</span><span class="sxs-lookup"><span data-stu-id="fb078-121">(Rs, Gs, Bs, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="fb078-122">\_INVSRCCOLOR D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-122">D3DBLEND\_INVSRCCOLOR</span></span>     | <span data-ttu-id="fb078-123">(1-RS, 1-GS, 1-BS, 1 come)</span><span class="sxs-lookup"><span data-stu-id="fb078-123">(1-Rs, 1-Gs, 1-Bs, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="fb078-124">\_SRCALPHA D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-124">D3DBLEND\_SRCALPHA</span></span>        | <span data-ttu-id="fb078-125">(Come, come, come)</span><span class="sxs-lookup"><span data-stu-id="fb078-125">(As, As, As, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="fb078-126">\_INVSRCALPHA D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-126">D3DBLEND\_INVSRCALPHA</span></span>     | <span data-ttu-id="fb078-127">(1-As, 1-As, 1-As, 1-As)</span><span class="sxs-lookup"><span data-stu-id="fb078-127">(1-As, 1-As, 1-As, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="fb078-128">\_DESTALPHA D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-128">D3DBLEND\_DESTALPHA</span></span>       | <span data-ttu-id="fb078-129">(Ad, ad, ad, ad)</span><span class="sxs-lookup"><span data-stu-id="fb078-129">(Ad, Ad, Ad, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="fb078-130">\_INVDESTALPHA D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-130">D3DBLEND\_INVDESTALPHA</span></span>    | <span data-ttu-id="fb078-131">(1-ad, 1-ad, 1-ad, 1-ad)</span><span class="sxs-lookup"><span data-stu-id="fb078-131">(1-Ad, 1-Ad, 1-Ad, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="fb078-132">\_DESTCOLOR D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-132">D3DBLEND\_DESTCOLOR</span></span>       | <span data-ttu-id="fb078-133">(Rd, GD, BD, ad)</span><span class="sxs-lookup"><span data-stu-id="fb078-133">(Rd, Gd, Bd, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="fb078-134">\_INVDESTCOLOR D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-134">D3DBLEND\_INVDESTCOLOR</span></span>    | <span data-ttu-id="fb078-135">(1-Rd, 1-GD, 1-BD, 1-ad)</span><span class="sxs-lookup"><span data-stu-id="fb078-135">(1-Rd, 1-Gd, 1-Bd, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="fb078-136">\_SRCALPHASAT D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-136">D3DBLEND\_SRCALPHASAT</span></span>     | <span data-ttu-id="fb078-137">(f, f, f, 1); f = min (As, 1-ad)</span><span class="sxs-lookup"><span data-stu-id="fb078-137">(f, f, f, 1); f = min(As, 1-Ad)</span></span>                                                                                                                                                          |
| <span data-ttu-id="fb078-138">\_BOTHSRCALPHA D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-138">D3DBLEND\_BOTHSRCALPHA</span></span>    | <span data-ttu-id="fb078-139">Obsoleto per DirectX 6 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="fb078-139">Obsolete for DirectX 6 and later.</span></span> <span data-ttu-id="fb078-140">È possibile ottenere lo stesso risultato impostando i fattori di Blend di origine e di destinazione su D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA in chiamate separate.</span><span class="sxs-lookup"><span data-stu-id="fb078-140">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span> |
| <span data-ttu-id="fb078-141">\_BOTHINVSRCALPHA D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-141">D3DBLEND\_BOTHINVSRCALPHA</span></span> | <span data-ttu-id="fb078-142">Obsoleto per DirectX 6.</span><span class="sxs-lookup"><span data-stu-id="fb078-142">Obsolete for DirectX 6.</span></span> <span data-ttu-id="fb078-143">È possibile ottenere lo stesso risultato impostando i fattori di Blend di origine e di destinazione su D3DBLEND \_ INVSRCALPHA e D3DBLEND \_ SRCALPHA in chiamate separate.</span><span class="sxs-lookup"><span data-stu-id="fb078-143">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_INVSRCALPHA and D3DBLEND\_SRCALPHA in separate calls.</span></span>           |
| <span data-ttu-id="fb078-144">\_BLENDFACTOR D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-144">D3DBLEND\_BLENDFACTOR</span></span>     | <span data-ttu-id="fb078-145">Usare color. r, color. g, color. b e color. a ottenuto dall' \_ impostazione BLENDFACTOR di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="fb078-145">Use color.r, color.g, color.b, and color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                                 |
| <span data-ttu-id="fb078-146">\_INVBLENDFACTOR D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="fb078-146">D3DBLEND\_INVBLENDFACTOR</span></span>  | <span data-ttu-id="fb078-147">Usare 1-color. r, 1-color. g, 1-color. b e 1-color. a ottenuto dall' \_ impostazione BLENDFACTOR di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="fb078-147">Use 1-color.r, 1-color.g, 1-color.b, and 1-color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                         |



 

<span data-ttu-id="fb078-148">Direct3D usa lo \_ stato di rendering ALPHABLENDENABLE di D3DRS per abilitare la sfumatura di trasparenza alfa.</span><span class="sxs-lookup"><span data-stu-id="fb078-148">Direct3D uses the D3DRS\_ALPHABLENDENABLE render state to enable alpha transparency blending.</span></span> <span data-ttu-id="fb078-149">Il tipo di fusione alfa eseguita dipende \_ dagli Stati di rendering D3DRS SRCBLEND e D3DRS \_ DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="fb078-149">The type of alpha blending that is done depends on the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span> <span data-ttu-id="fb078-150">Gli Stati di Blend di origine e di destinazione vengono utilizzati nelle coppie.</span><span class="sxs-lookup"><span data-stu-id="fb078-150">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="fb078-151">Il seguente frammento di codice imposta lo stato di Blend di origine su D3DBLEND \_ SRCCOLOR e lo stato di Blend di destinazione su D3DBLEND \_ INVSRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="fb078-151">The following code fragment sets the source blend state to D3DBLEND\_SRCCOLOR and the destination blend state to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="fb078-152">Questo codice esegue una Blend lineare tra il colore di origine (il colore della primitiva di cui viene eseguito il rendering nella posizione corrente) e il colore di destinazione (il colore in corrispondenza della posizione corrente nel buffer del frame).</span><span class="sxs-lookup"><span data-stu-id="fb078-152">This code performs a linear blend between the source color (the color of the primitive being rendered at the current location) and the destination color (the color at the current location in the frame buffer).</span></span> <span data-ttu-id="fb078-153">L'aspetto risultante è simile a quello colorato in quanto il colore dell'oggetto di destinazione sembra essere trasmesso tramite l'oggetto di origine. il resto sembra essere assorbito.</span><span class="sxs-lookup"><span data-stu-id="fb078-153">The resulting appearance is similar to tinted glass in that some of the color of the destination object seems to be transmitted through the source object; the rest of it appears to be absorbed.</span></span>

<span data-ttu-id="fb078-154">Molti di questi fattori di Blend richiedono che i valori alfa nella trama funzionino correttamente.</span><span class="sxs-lookup"><span data-stu-id="fb078-154">Many of these blend factors require alpha values in the texture to operate correctly.</span></span> <span data-ttu-id="fb078-155">Quindi, quando si usa il vertice o il materiale Alfa, l'applicazione è limitata al modo in cui le modalità produrranno risultati interessanti.</span><span class="sxs-lookup"><span data-stu-id="fb078-155">Thus, when using vertex or material alpha, the application is restricted as to which modes will produce interesting results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb078-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb078-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb078-157">Fusione alfa</span><span class="sxs-lookup"><span data-stu-id="fb078-157">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 




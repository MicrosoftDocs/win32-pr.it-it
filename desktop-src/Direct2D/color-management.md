---
title: Effetto di gestione colori
description: Usare l'effetto di gestione colori per trasformare un'immagine da un profilo colori ICC (International Color Consortium) a un altro. L'effetto trasforma l'immagine in base alla specifica ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- effetto di gestione colori
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400544"
---
# <a name="color-management-effect"></a><span data-ttu-id="bef3e-105">Effetto di gestione colori</span><span class="sxs-lookup"><span data-stu-id="bef3e-105">Color management effect</span></span>

<span data-ttu-id="bef3e-106">Usare l'effetto di gestione colori per trasformare un'immagine da un profilo colori ICC (International Color Consortium) a un altro.</span><span class="sxs-lookup"><span data-stu-id="bef3e-106">Use the color management effect to transform an image from one ICC (International Color Consortium) color profile to another.</span></span> <span data-ttu-id="bef3e-107">L'effetto trasforma l'immagine in base alla [specifica ICC](https://www.color.org).</span><span class="sxs-lookup"><span data-stu-id="bef3e-107">The effect transforms the image according to the [ICC specification](https://www.color.org).</span></span>

<span data-ttu-id="bef3e-108">Il CLSID per questo effetto è CLSID \_ D2D1ColorManagement.</span><span class="sxs-lookup"><span data-stu-id="bef3e-108">The CLSID for this effect is CLSID\_D2D1ColorManagement.</span></span>

- [<span data-ttu-id="bef3e-109">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="bef3e-109">Effect properties</span></span>](#effect-properties)
- [<span data-ttu-id="bef3e-110">Modalità finalità di rendering</span><span class="sxs-lookup"><span data-stu-id="bef3e-110">Rendering intent modes</span></span>](#rendering-intent-modes)
- [<span data-ttu-id="bef3e-111">Modalità Alpha immagine di input</span><span class="sxs-lookup"><span data-stu-id="bef3e-111">Input image alpha modes</span></span>](#input-image-alpha-modes)
- [<span data-ttu-id="bef3e-112">Conformità con la specifica ICC</span><span class="sxs-lookup"><span data-stu-id="bef3e-112">Compliance with ICC specification</span></span>](#compliance-with-icc-specification)
- [<span data-ttu-id="bef3e-113">Comportamento canale alfa</span><span class="sxs-lookup"><span data-stu-id="bef3e-113">Alpha channel behavior</span></span>](#alpha-channel-behavior)
- [<span data-ttu-id="bef3e-114">Modalità di qualità</span><span class="sxs-lookup"><span data-stu-id="bef3e-114">Quality modes</span></span>](#quality-modes)
- [<span data-ttu-id="bef3e-115">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="bef3e-115">Sample code</span></span>](#sample-code)
- [<span data-ttu-id="bef3e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bef3e-116">Requirements</span></span>](#requirements)
- [<span data-ttu-id="bef3e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bef3e-117">Related topics</span></span>](#related-topics)

## <a name="effect-properties"></a><span data-ttu-id="bef3e-118">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="bef3e-118">Effect properties</span></span>

| <span data-ttu-id="bef3e-119">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="bef3e-119">Display name and index enumeration</span></span> | <span data-ttu-id="bef3e-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bef3e-120">Description</span></span> |
|-|-|
| <span data-ttu-id="bef3e-121">SourceContext</span><span class="sxs-lookup"><span data-stu-id="bef3e-121">SourceContext</span></span><br/> <span data-ttu-id="bef3e-122">D2D1 \_ COLORMANAGEMENT \_ - \_ \_ contesto colore \_ origine</span><span class="sxs-lookup"><span data-stu-id="bef3e-122">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="bef3e-123">Informazioni sullo spazio dei colori di origine.</span><span class="sxs-lookup"><span data-stu-id="bef3e-123">The source color space information.</span></span> <span data-ttu-id="bef3e-124">Il tipo è [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="bef3e-124">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="bef3e-125">Il valore predefinito è NULL.</span><span class="sxs-lookup"><span data-stu-id="bef3e-125">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="bef3e-126">SourceIntent</span><span class="sxs-lookup"><span data-stu-id="bef3e-126">SourceIntent</span></span><br/> <span data-ttu-id="bef3e-127">D2D1 \_ COLORMANAGEMENT \_ - \_ \_ finalità rendering \_ origine</span><span class="sxs-lookup"><span data-stu-id="bef3e-127">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="bef3e-128">Quale finalità del rendering ICC utilizzare.</span><span class="sxs-lookup"><span data-stu-id="bef3e-128">Which ICC rendering intent to use.</span></span> <span data-ttu-id="bef3e-129">Il tipo è D2D1 \_ COLORMANAGEMENT \_ rendering \_ Intent.</span><span class="sxs-lookup"><span data-stu-id="bef3e-129">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="bef3e-130">Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ rendering \_ finalità \_ percettiv.</span><span class="sxs-lookup"><span data-stu-id="bef3e-130">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="bef3e-131">DestinationContext</span><span class="sxs-lookup"><span data-stu-id="bef3e-131">DestinationContext</span></span><br/> <span data-ttu-id="bef3e-132">D2D1 \_ COLORMANAGEMENT \_ - \_ \_ contesto colore \_ destinazione</span><span class="sxs-lookup"><span data-stu-id="bef3e-132">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="bef3e-133">Informazioni sullo spazio dei colori di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bef3e-133">The destination color space information.</span></span> <span data-ttu-id="bef3e-134">Il tipo è [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="bef3e-134">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="bef3e-135">Il valore predefinito è NULL.</span><span class="sxs-lookup"><span data-stu-id="bef3e-135">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="bef3e-136">DestinationIntent</span><span class="sxs-lookup"><span data-stu-id="bef3e-136">DestinationIntent</span></span><br/> <span data-ttu-id="bef3e-137">\_Finalità di \_ \_ rendering della \_ destinazione \_ d2d1 COLORMANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="bef3e-137">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="bef3e-138">Quale finalità del rendering ICC utilizzare.</span><span class="sxs-lookup"><span data-stu-id="bef3e-138">Which ICC rendering intent to use.</span></span> <span data-ttu-id="bef3e-139">Il tipo è D2D1 \_ COLORMANAGEMENT \_ rendering \_ Intent.</span><span class="sxs-lookup"><span data-stu-id="bef3e-139">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="bef3e-140">Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ rendering \_ finalità \_ percettiv.</span><span class="sxs-lookup"><span data-stu-id="bef3e-140">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="bef3e-141">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="bef3e-141">AlphaMode</span></span><br/> <span data-ttu-id="bef3e-142">D2D1 \_ COLORMANAGEMENT \_ prop \_ Alpha \_ mode</span><span class="sxs-lookup"><span data-stu-id="bef3e-142">D2D1\_COLORMANAGEMENT\_PROP\_ALPHA\_MODE</span></span><br/> | <span data-ttu-id="bef3e-143">Come interpretare i dati alfa contenuti nell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="bef3e-143">How to interpret alpha data that is contained in the input image.</span></span> <span data-ttu-id="bef3e-144">Il tipo è D2D1 \_ COLORMANAGEMENT \_ Alpha \_ mode.</span><span class="sxs-lookup"><span data-stu-id="bef3e-144">The type is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="bef3e-145">Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ Alpha \_ mode \_ premoltiplicato.</span><span class="sxs-lookup"><span data-stu-id="bef3e-145">The default value is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/> |
| <span data-ttu-id="bef3e-146">Qualità</span><span class="sxs-lookup"><span data-stu-id="bef3e-146">Quality</span></span><br/> <span data-ttu-id="bef3e-147">\_Qualità della \_ prop \_ COLORMANAGEMENT d2d1</span><span class="sxs-lookup"><span data-stu-id="bef3e-147">D2D1\_COLORMANAGEMENT\_PROP\_QUALITY</span></span><br/> | <span data-ttu-id="bef3e-148">Livello di qualità della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="bef3e-148">The quality level of the transform.</span></span> <span data-ttu-id="bef3e-149">Il tipo è D2D1 \_ COLORMANAGEMENT \_ Quality.</span><span class="sxs-lookup"><span data-stu-id="bef3e-149">The type is D2D1\_COLORMANAGEMENT\_QUALITY.</span></span><br/> <span data-ttu-id="bef3e-150">Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ qualità \_ normale.</span><span class="sxs-lookup"><span data-stu-id="bef3e-150">The default value is D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL.</span></span><br/> |

## <a name="rendering-intent-modes"></a><span data-ttu-id="bef3e-151">Modalità finalità di rendering</span><span class="sxs-lookup"><span data-stu-id="bef3e-151">Rendering intent modes</span></span>

| <span data-ttu-id="bef3e-152">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="bef3e-152">Enumeration</span></span> | <span data-ttu-id="bef3e-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bef3e-153">Description</span></span> |
|-|-|
| <span data-ttu-id="bef3e-154">\_ \_ \_ Percettivo della finalità di rendering COLORMANAGEMENT d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="bef3e-154">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL</span></span> | <span data-ttu-id="bef3e-155">L'effetto comprime o espande la gamma di colori completa dell'immagine per riempire la gamma di colori del dispositivo, in modo che il saldo grigio venga mantenuto, ma l'accuratezza colorimetrico potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="bef3e-155">The effect compresses or expands the full color gamut of the image to fill the color gamut of the device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span> |
| <span data-ttu-id="bef3e-156">\_ \_ \_ \_ Colorimetrico relativo per il rendering COLORMANAGEMENT di d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="bef3e-156">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="bef3e-157">L'effetto conserva il Chroma dei colori nell'immagine al possibile costo di tonalità e luminosità.</span><span class="sxs-lookup"><span data-stu-id="bef3e-157">The effect preserves the chroma of colors in the image at the possible expense of hue and lightness.</span></span> |
| <span data-ttu-id="bef3e-158">\_ \_ \_ Saturazione finalità rendering COLORMANAGEMENT d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="bef3e-158">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_SATURATION</span></span> | <span data-ttu-id="bef3e-159">L'effetto regola i colori che non rientrano nell'intervallo di colori a cui viene eseguito il rendering del dispositivo di output sul colore più vicino disponibile.</span><span class="sxs-lookup"><span data-stu-id="bef3e-159">The effect adjusts colors that fall outside the range of colors the output device renders to the closest color available.</span></span> <span data-ttu-id="bef3e-160">Non mantiene il punto bianco.</span><span class="sxs-lookup"><span data-stu-id="bef3e-160">It does not preserve the white point.</span></span> |
| <span data-ttu-id="bef3e-161">\_ \_ \_ Colorimetrico assoluto della finalità di rendering \_ COLORMANAGEMENT d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="bef3e-161">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> | <span data-ttu-id="bef3e-162">L'effetto regola i colori che non rientrano nell'intervallo in cui il dispositivo di output è in grado di eseguire il rendering sul colore più vicino di cui è possibile eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="bef3e-162">The effect adjusts any colors that fall outside the range that the output device can render to the closest color that can be rendered.</span></span> <span data-ttu-id="bef3e-163">L'effetto non modifica gli altri colori e conserva il punto bianco.</span><span class="sxs-lookup"><span data-stu-id="bef3e-163">The effect does not change the other colors and preserves the white point.</span></span> |

## <a name="input-image-alpha-modes"></a><span data-ttu-id="bef3e-164">Modalità Alpha immagine di input</span><span class="sxs-lookup"><span data-stu-id="bef3e-164">Input image alpha modes</span></span>

| <span data-ttu-id="bef3e-165">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="bef3e-165">Enumeration</span></span> | <span data-ttu-id="bef3e-166">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bef3e-166">Description</span></span> |
|-|-|
| <span data-ttu-id="bef3e-167">D2D1 \_ COLORMANAGEMENT \_ - \_ modalità alfa \_ premoltiplicata</span><span class="sxs-lookup"><span data-stu-id="bef3e-167">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="bef3e-168">L'effetto presuppone che la modalità Alpha sia premoltiplicata.</span><span class="sxs-lookup"><span data-stu-id="bef3e-168">The effect assumes the alpha mode is premultiplied.</span></span> |
| <span data-ttu-id="bef3e-169">D2D1 \_ COLORMANAGEMENT \_ - \_ modalità Alpha \_ diritta</span><span class="sxs-lookup"><span data-stu-id="bef3e-169">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_STRAIGHT</span></span> | <span data-ttu-id="bef3e-170">L'effetto presuppone che la modalità Alpha sia diritta.</span><span class="sxs-lookup"><span data-stu-id="bef3e-170">The effect assumes the alpha mode is straight.</span></span> |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a><span data-ttu-id="bef3e-171">Modifiche del comportamento D2D1_GAMMA1_G2084</span><span class="sxs-lookup"><span data-stu-id="bef3e-171">D2D1_GAMMA1_G2084 behavior changes</span></span>
    
<span data-ttu-id="bef3e-172">Se l'applicazione usa lo spazio [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) o uno dei [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) valori di enumerazione che usano lo spazio di colore SMPTE St. 2084 (percettiv quantizzator), l'applicazione intende usare i dati HDR.</span><span class="sxs-lookup"><span data-stu-id="bef3e-172">If your application uses the [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) space, or one of the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration values that use the SMPTE ST.2084 (Perceptual Quantizer) color space, then the application intends to work with HDR data.</span></span>

<span data-ttu-id="bef3e-173">Le API [**ID2D1DeviceContext5:: CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) e [**ID2D1DeviceContext5:: CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) non ne fanno conto; il contenuto HDR viene invece ridimensionato per adattarsi all'intervallo di 0-1 durante l'operazione di degamma G2084.</span><span class="sxs-lookup"><span data-stu-id="bef3e-173">The [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) and [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) APIs don't account for that; rather, the HDR content is scaled to fit in the 0-1 range during the G2084 DeGamma operation.</span></span>

<span data-ttu-id="bef3e-174">In pratica, il contenuto codificato in questo spazio gamma usa un WhiteLevel di riferimento di 10.000 nit, che in genere viene rappresentato in CCCS come 10.000/80 = 125,0.</span><span class="sxs-lookup"><span data-stu-id="bef3e-174">In practice, content that is encoded in this gamma space uses a reference WhiteLevel of 10,000 Nits, which would normally be represented in CCCS as 10,000 / 80 = 125.0.</span></span> <span data-ttu-id="bef3e-175">Quindi, per semplificare l'app, è più semplice per questa conversione gamma ridimensionare anche la luminanza per un fattore di 125.</span><span class="sxs-lookup"><span data-stu-id="bef3e-175">So, to better facilitate your app, it's simplest for this gamma conversion to also scale the luminance by a factor of 125.</span></span> <span data-ttu-id="bef3e-176">A partire da Windows 10, versione 1809 (10,0; Build 17763), il comportamento dell'effetto di gestione dei colori è tale da applicare questa scalabilità.</span><span class="sxs-lookup"><span data-stu-id="bef3e-176">As of Windows 10, version 1809 (10.0; Build 17763), the behavior of the color management effect is such that it applies this scaling.</span></span> <span data-ttu-id="bef3e-177">Ciò significa che, in qualità di sviluppatore, non è necessario applicare un secondo [effetto di regolazione del livello bianco](white-level-adjustment-effect.md) nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="bef3e-177">That means that you, as the developer, don't have to apply a second [White level adjustment effect](white-level-adjustment-effect.md) into the pipeline.</span></span>

## <a name="compliance-with-icc-specification"></a><span data-ttu-id="bef3e-178">Conformità con la specifica ICC</span><span class="sxs-lookup"><span data-stu-id="bef3e-178">Compliance with ICC specification</span></span>

<span data-ttu-id="bef3e-179">L'effetto di gestione colori è conforme alla specifica ICC v 4.3, con le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bef3e-179">The color management effect is compliant with the ICC v4.3 specification, with these limitations:</span></span>

- <span data-ttu-id="bef3e-180">L'effetto supporta spazi dei colori 1, 3 e 4.</span><span class="sxs-lookup"><span data-stu-id="bef3e-180">The effect supports 1, 3, and 4 channel color spaces.</span></span>
- <span data-ttu-id="bef3e-181">L'effetto non supporta lo spazio dei nomi o i profili colori denominati.</span><span class="sxs-lookup"><span data-stu-id="bef3e-181">The effect doesn't support ColorSpace or Named Color profiles.</span></span>

## <a name="alpha-channel-behavior"></a><span data-ttu-id="bef3e-182">Comportamento canale alfa</span><span class="sxs-lookup"><span data-stu-id="bef3e-182">Alpha channel behavior</span></span>

<span data-ttu-id="bef3e-183">In generale, l'effetto imposta alfa su 1 (opaco) se non sono presenti dati alfa nell'immagine di origine e i dati alfa vengono rimossi se l'immagine di destinazione non contiene spazio.</span><span class="sxs-lookup"><span data-stu-id="bef3e-183">In general, the effect sets alpha to 1 (opaque) if there is no alpha data in the source image and the alpha data is discarded if there is no room in the destination image.</span></span> <span data-ttu-id="bef3e-184">La tabella seguente descrive il comportamento alfa.</span><span class="sxs-lookup"><span data-stu-id="bef3e-184">The table here describes the alpha behavior.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bef3e-185">Spazio di colore di origine, formato pixel</span><span class="sxs-lookup"><span data-stu-id="bef3e-185">Source colorspace, pixel format</span></span></th>
<th><span data-ttu-id="bef3e-186">Spazio colore di destinazione, formato pixel</span><span class="sxs-lookup"><span data-stu-id="bef3e-186">Destination colorspace, pixel format</span></span></th>
<th><span data-ttu-id="bef3e-187">Comportamento Alpha</span><span class="sxs-lookup"><span data-stu-id="bef3e-187">Alpha behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="bef3e-188">1 canale, formato R pixel $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="bef3e-188">1 channel, R pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bef3e-189">1 canale, formato pixel R</span><span class="sxs-lookup"><span data-stu-id="bef3e-189">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="bef3e-190">(Nessun dato alfanumerico)</span><span class="sxs-lookup"><span data-stu-id="bef3e-190">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bef3e-191">1 canale, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-191">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-192">I dati alfa sono impostati su 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="bef3e-192">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bef3e-193">3 canali, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-193">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-194">I dati alfa sono impostati su 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="bef3e-194">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bef3e-195">4 canali, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-195">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-196">(Nessun dato alfanumerico)</span><span class="sxs-lookup"><span data-stu-id="bef3e-196">(No alpha data)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="bef3e-197">1 canale, formato pixel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="bef3e-197">1 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bef3e-198">1 canale, formato pixel R</span><span class="sxs-lookup"><span data-stu-id="bef3e-198">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="bef3e-199">Dati alfa eliminati</span><span class="sxs-lookup"><span data-stu-id="bef3e-199">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bef3e-200">1 canale, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-200">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-201">I dati alfa vengono passati</span><span class="sxs-lookup"><span data-stu-id="bef3e-201">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bef3e-202">3 canali, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-202">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-203">I dati alfa vengono passati</span><span class="sxs-lookup"><span data-stu-id="bef3e-203">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bef3e-204">4 canali, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-204">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-205">Dati alfa eliminati</span><span class="sxs-lookup"><span data-stu-id="bef3e-205">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="bef3e-206">3 canali, formato pixel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="bef3e-206">3 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bef3e-207">1 canale, formato pixel R</span><span class="sxs-lookup"><span data-stu-id="bef3e-207">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="bef3e-208">Dati alfa eliminati</span><span class="sxs-lookup"><span data-stu-id="bef3e-208">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bef3e-209">1 canale, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-209">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-210">I dati alfa vengono passati</span><span class="sxs-lookup"><span data-stu-id="bef3e-210">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bef3e-211">3 canali, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-211">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-212">I dati alfa vengono passati</span><span class="sxs-lookup"><span data-stu-id="bef3e-212">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bef3e-213">4 canali, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-213">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-214">Dati alfa eliminati</span><span class="sxs-lookup"><span data-stu-id="bef3e-214">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="bef3e-215">4 canali, formato pixel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="bef3e-215">4 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bef3e-216">1 canale, formato pixel R</span><span class="sxs-lookup"><span data-stu-id="bef3e-216">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="bef3e-217">(Nessun dato alfanumerico)</span><span class="sxs-lookup"><span data-stu-id="bef3e-217">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bef3e-218">1 canale, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-218">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-219">I dati alfa sono impostati su 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="bef3e-219">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bef3e-220">3 canali, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-220">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-221">I dati alfa sono impostati su 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="bef3e-221">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="bef3e-222">4 canali, formato pixel RGBA</span><span class="sxs-lookup"><span data-stu-id="bef3e-222">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="bef3e-223">(Nessun dato alfanumerico)</span><span class="sxs-lookup"><span data-stu-id="bef3e-223">(No alpha data)</span></span></td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a><span data-ttu-id="bef3e-224">Modalità di qualità</span><span class="sxs-lookup"><span data-stu-id="bef3e-224">Quality modes</span></span>

| <span data-ttu-id="bef3e-225">Mode</span><span class="sxs-lookup"><span data-stu-id="bef3e-225">Mode</span></span> | <span data-ttu-id="bef3e-226">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bef3e-226">Description</span></span> |
|-|-|
| <span data-ttu-id="bef3e-227">\_Prova di \_ qualità d2d1 COLORMANAGEMENT \_</span><span class="sxs-lookup"><span data-stu-id="bef3e-227">D2D1\_COLORMANAGEMENT\_QUALITY\_PROOF</span></span> | <span data-ttu-id="bef3e-228">Modalità di qualità più bassa.</span><span class="sxs-lookup"><span data-stu-id="bef3e-228">The lowest quality mode.</span></span> <span data-ttu-id="bef3e-229">Questa modalità richiede il livello di funzionalità 9 \_ 1 o superiore.</span><span class="sxs-lookup"><span data-stu-id="bef3e-229">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="bef3e-230">D2D1 \_ COLORMANAGEMENT \_ qualità \_ normale</span><span class="sxs-lookup"><span data-stu-id="bef3e-230">D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL</span></span> | <span data-ttu-id="bef3e-231">Modalità di qualità normale.</span><span class="sxs-lookup"><span data-stu-id="bef3e-231">Normal quality mode.</span></span> <span data-ttu-id="bef3e-232">Questa modalità richiede il livello di funzionalità 9 \_ 1 o superiore.</span><span class="sxs-lookup"><span data-stu-id="bef3e-232">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="bef3e-233">D2D1 \_ COLORMANAGEMENT \_ qualità \_ migliore</span><span class="sxs-lookup"><span data-stu-id="bef3e-233">D2D1\_COLORMANAGEMENT\_QUALITY\_BEST</span></span> | <span data-ttu-id="bef3e-234">Modalità di qualità migliore.</span><span class="sxs-lookup"><span data-stu-id="bef3e-234">The best quality mode.</span></span> <span data-ttu-id="bef3e-235">Questa modalità richiede il livello di funzionalità 10 \_ 0 o superiore, nonché i buffer di precisione a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="bef3e-235">This mode requires feature level 10\_0 or above, as well as floating point precision buffers.</span></span> <span data-ttu-id="bef3e-236">Questa modalità supporta la precisione a virgola mobile e l'intervallo esteso come definito nella specifica ICC v 4.3.</span><span class="sxs-lookup"><span data-stu-id="bef3e-236">This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification.</span></span> |

<span data-ttu-id="bef3e-237">L'effetto di gestione colori ha esito negativo durante il disegno se l'applicazione richiede una modalità di qualità non supportata dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="bef3e-237">The color management effect fails when drawing if the application requests a quality mode that is not supported by the hardware.</span></span> <span data-ttu-id="bef3e-238">È possibile determinare il livello di funzionalità quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span><span class="sxs-lookup"><span data-stu-id="bef3e-238">You can determine the feature level when you call [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span></span> <span data-ttu-id="bef3e-239">È possibile verificare il supporto del buffer a virgola mobile chiamando [**ID2D1EffectContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) con il valore [**d2d1 \_ buffer \_ Precision \_ 32 bpc \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span><span class="sxs-lookup"><span data-stu-id="bef3e-239">You can check for floating point buffer support by calling [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) with the value [**D2D1\_BUFFER\_PRECISION\_32BPC\_FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span></span>

## <a name="sample-code"></a><span data-ttu-id="bef3e-240">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="bef3e-240">Sample code</span></span>

<span data-ttu-id="bef3e-241">Per un esempio di questo effetto, scaricare l' [esempio di regolazione foto effetti Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)e vedere la lezione 4 dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="bef3e-241">For an example of this effect, download the [Direct2D effects photo adjustment sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment), and see Lesson 4 of the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="bef3e-242">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bef3e-242">Requirements</span></span>

| <span data-ttu-id="bef3e-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef3e-243">Requirement</span></span> | <span data-ttu-id="bef3e-244">Valore</span><span class="sxs-lookup"><span data-stu-id="bef3e-244">Value</span></span> |
|-|-|
| <span data-ttu-id="bef3e-245">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bef3e-245">Minimum supported client</span></span> | <span data-ttu-id="bef3e-246">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="bef3e-246">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bef3e-247">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bef3e-247">Minimum supported server</span></span> | <span data-ttu-id="bef3e-248">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="bef3e-248">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bef3e-249">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bef3e-249">Header</span></span> | <span data-ttu-id="bef3e-250">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="bef3e-250">d2d1effects.h</span></span> |
| <span data-ttu-id="bef3e-251">Libreria</span><span class="sxs-lookup"><span data-stu-id="bef3e-251">Library</span></span> | <span data-ttu-id="bef3e-252">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="bef3e-252">d2d1.lib, dxguid.lib</span></span> |

## <a name="related-topics"></a><span data-ttu-id="bef3e-253">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bef3e-253">Related topics</span></span>

* [<span data-ttu-id="bef3e-254">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="bef3e-254">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

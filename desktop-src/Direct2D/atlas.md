---
title: Effetto Atlas
description: È possibile usare questo effetto per restituire una parte di un'immagine ma mantenere l'area esterna alla parte da usare nelle operazioni successive.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478233"
---
# <a name="atlas-effect"></a><span data-ttu-id="b95f3-103">Effetto Atlas</span><span class="sxs-lookup"><span data-stu-id="b95f3-103">Atlas effect</span></span>

<span data-ttu-id="b95f3-104">È possibile usare questo effetto per restituire una parte di un'immagine ma mantenere l'area esterna alla parte da usare nelle operazioni successive.</span><span class="sxs-lookup"><span data-stu-id="b95f3-104">You can use this effect to output a portion of an image but retain the region outside of the portion for use in subsequent operations.</span></span>

<span data-ttu-id="b95f3-105">Il CLSID per questo effetto è CLSID \_ D2D1Atlas.</span><span class="sxs-lookup"><span data-stu-id="b95f3-105">The CLSID for this effect is CLSID\_D2D1Atlas.</span></span>

<span data-ttu-id="b95f3-106">L'effetto Atlas è utile se si desidera caricare un'immagine di grandi dimensioni costituita da molte immagini più piccole, ad esempio vari frame di uno sprite.</span><span class="sxs-lookup"><span data-stu-id="b95f3-106">The atlas effect is useful if you want to load a large image made up of many smaller images, such as various frames of a sprite.</span></span>

<span data-ttu-id="b95f3-107">Per creare l'output, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b95f3-107">To create the output the effect:</span></span>

1.  <span data-ttu-id="b95f3-108">Ritaglia l'input nella proprietà *InputRect* specificata.</span><span class="sxs-lookup"><span data-stu-id="b95f3-108">Crops the input to the given *InputRect* property.</span></span>
2.  <span data-ttu-id="b95f3-109">Converte l'origine del risultato in (0,0).</span><span class="sxs-lookup"><span data-stu-id="b95f3-109">Translates the origin of the result to (0,0).</span></span>

> [!Note]  
> <span data-ttu-id="b95f3-110">La proprietà *InputPaddingRect* deve essere maggiore solo se e solo se i pixel tra i due rettangoli sono di colore nero trasparente nell'input.</span><span class="sxs-lookup"><span data-stu-id="b95f3-110">The *InputPaddingRect* property should only be larger if and only if the pixels between the two rectangles are transparent black on the input.</span></span> <span data-ttu-id="b95f3-111">Questo può comportare l'esecuzione di Direct2D del grafo in modo più ottimale.</span><span class="sxs-lookup"><span data-stu-id="b95f3-111">This may result in Direct2D executing the graph more optimally.</span></span>

 

<span data-ttu-id="b95f3-112">Di seguito è riportato un esempio dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b95f3-112">Here is an example of the effect.</span></span> <span data-ttu-id="b95f3-113">Questa immagine è piccola e semplice a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="b95f3-113">This image is small and simple for illustration purposes.</span></span>

![immagine di input.](images/atlas.png)

<span data-ttu-id="b95f3-115">L'immagine precedente è l'input dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b95f3-115">The preceding image is the input to the effect.</span></span> <span data-ttu-id="b95f3-116">Il codice qui crea un effetto Atlas, imposta l'input, imposta il rettangolo di input, quindi disegna l'output.</span><span class="sxs-lookup"><span data-stu-id="b95f3-116">The code here creates an atlas effect, sets the input, sets the input rectangle, and then draws the output.</span></span>


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



<span data-ttu-id="b95f3-117">Il codice precedente seleziona un rettangolo intorno al secondo triangolo.</span><span class="sxs-lookup"><span data-stu-id="b95f3-117">The preceding code selects a rectangle that is around the second triangle.</span></span> <span data-ttu-id="b95f3-118">La spaziatura interna viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="b95f3-118">The padding around it is ignored.</span></span> <span data-ttu-id="b95f3-119">Di seguito è illustrata l'immagine risultante.</span><span class="sxs-lookup"><span data-stu-id="b95f3-119">Here is the resulting image.</span></span>

![immagine di output.](images/atlas2.png)

> [!Note]  
> <span data-ttu-id="b95f3-121">Si tratta di una situazione in cui è possibile scegliere di specificare un *InputPaddingRect* perché il riempimento è nero trasparente.</span><span class="sxs-lookup"><span data-stu-id="b95f3-121">This is a situation where you may choose to specify a *InputPaddingRect* because the padding is transparent black.</span></span> <span data-ttu-id="b95f3-122">Il rettangolo sarà `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .</span><span class="sxs-lookup"><span data-stu-id="b95f3-122">The rectangle would be `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);`.</span></span>

 

## <a name="effect-properties"></a><span data-ttu-id="b95f3-123">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="b95f3-123">Effect properties</span></span>



| <span data-ttu-id="b95f3-124">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="b95f3-124">Display name and index enumeration</span></span>                                             | <span data-ttu-id="b95f3-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b95f3-125">Description</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b95f3-126">InputRect</span><span class="sxs-lookup"><span data-stu-id="b95f3-126">InputRect</span></span><br/> <span data-ttu-id="b95f3-127">D2D1 \_ Atlas \_ prop \_ input \_ Rect</span><span class="sxs-lookup"><span data-stu-id="b95f3-127">D2D1\_ATLAS\_PROP\_INPUT\_RECT</span></span><br/>                 | <span data-ttu-id="b95f3-128">Parte dell'immagine passata all'effetto successivo.</span><span class="sxs-lookup"><span data-stu-id="b95f3-128">The portion of the image passed to the next effect.</span></span><br/> <span data-ttu-id="b95f3-129">Il tipo è D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="b95f3-129">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="b95f3-130">Il valore predefinito è (-FLT \_ Max,-flt \_ Max, flt \_ Max, flt \_ max).</span><span class="sxs-lookup"><span data-stu-id="b95f3-130">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span> <br/> |
| <span data-ttu-id="b95f3-131">InputPaddingRect</span><span class="sxs-lookup"><span data-stu-id="b95f3-131">InputPaddingRect</span></span><br/> <span data-ttu-id="b95f3-132">\_Rettangolo di \_ \_ riempimento input \_ d2d1 Atlas Prop \_</span><span class="sxs-lookup"><span data-stu-id="b95f3-132">D2D1\_ATLAS\_PROP\_INPUT\_PADDING\_RECT</span></span><br/> | <span data-ttu-id="b95f3-133">Dimensioni massime campionate per il rettangolo di output.</span><span class="sxs-lookup"><span data-stu-id="b95f3-133">The maximum size sampled for the output rectangle.</span></span><br/> <span data-ttu-id="b95f3-134">Il tipo è D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="b95f3-134">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="b95f3-135">Il valore predefinito è (-FLT \_ Max,-flt \_ Max, flt \_ Max, flt \_ max).</span><span class="sxs-lookup"><span data-stu-id="b95f3-135">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="b95f3-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b95f3-136">Requirements</span></span>



| <span data-ttu-id="b95f3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b95f3-137">Requirement</span></span> | <span data-ttu-id="b95f3-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b95f3-138">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b95f3-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b95f3-139">Minimum supported client</span></span> | <span data-ttu-id="b95f3-140">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b95f3-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b95f3-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b95f3-141">Minimum supported server</span></span> | <span data-ttu-id="b95f3-142">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b95f3-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b95f3-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b95f3-143">Header</span></span>                   | <span data-ttu-id="b95f3-144">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b95f3-144">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b95f3-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="b95f3-145">Library</span></span>                  | <span data-ttu-id="b95f3-146">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b95f3-146">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b95f3-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b95f3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b95f3-148">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b95f3-148">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


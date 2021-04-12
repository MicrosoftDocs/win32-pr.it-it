---
description: Definisce i valori che specificano le proprietà di un'alternativa di riconoscimento. Il Application Programming Interface di Tablet PC (API) USA identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in automazione sono stringhe costanti.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Costanti RecognitionProperty (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348636"
---
# <a name="recognitionproperty-constants"></a><span data-ttu-id="935cb-104">Costanti RecognitionProperty</span><span class="sxs-lookup"><span data-stu-id="935cb-104">RecognitionProperty Constants</span></span>

<span data-ttu-id="935cb-105">Definisce i valori che specificano le proprietà di un'alternativa di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="935cb-105">Defines values that specify the properties of a recognition alternate.</span></span> <span data-ttu-id="935cb-106">Il Application Programming Interface di Tablet PC (API) USA identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in automazione sono stringhe costanti.</span><span class="sxs-lookup"><span data-stu-id="935cb-106">The Tablet PC application programming interface (API) uses globally unique identifiers (GUIDs) to identify packet properties, which in Automation are constant strings.</span></span>

<span data-ttu-id="935cb-107">La tabella seguente elenca i campi GUID (Globally Unique Identifier) delle proprietà alternative di riconoscimento disponibili.</span><span class="sxs-lookup"><span data-stu-id="935cb-107">The following table lists the available recognition alternate property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="935cb-108">Usare questi GUID per accedere alle proprietà di un oggetto [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) chiamando il metodo [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .</span><span class="sxs-lookup"><span data-stu-id="935cb-108">Use these GUIDs to access properties of an [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object by calling the [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) method.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="935cb-109">Nome costante</span><span class="sxs-lookup"><span data-stu-id="935cb-109">Constant Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="935cb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="935cb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <span data-ttu-id="935cb-111"><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="935cb-111"><dt> <strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="935cb-112">GUID che identifica la proprietà per il numero di riga dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="935cb-112">The GUID that identifies the property for the line number of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="935cb-113">LineNumber specifica le alternative con un numero di riga specifico.</span><span class="sxs-lookup"><span data-stu-id="935cb-113">LineNumber specifies the alternates with a particular line number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="935cb-114">Questo campo non è supportato per i riconoscitori dei caratteri asiatici orientali.</span><span class="sxs-lookup"><span data-stu-id="935cb-114">This field is not supported for recognizers of East Asian characters.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <span data-ttu-id="935cb-115"><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="935cb-115"><dt> <strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="935cb-116">GUID che identifica la proprietà per la segmentazione dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="935cb-116">The GUID that identifies the property for the segmentation of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="935cb-117">Segmentazione specifica il frammento di input o l'unità di base che il riconoscimento USA per produrre un risultato del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="935cb-117">Segmentation specifies the basic ink fragment or unit that the recognizer uses to produce a recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="935cb-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="935cb-118">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <span data-ttu-id="935cb-119"><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="935cb-119"><dt> <strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="935cb-120">GUID che identifica la proprietà per il punto critico di riconoscimento dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="935cb-120">The GUID that identifies the property for the recognition hot point of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <span data-ttu-id="935cb-121"><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="935cb-121"><dt> <strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="935cb-122">GUID che identifica la proprietà per il numero massimo di tratti del risultato del riconoscimento per l'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="935cb-122">The GUID that identifies the property for the maximum stroke count of the recognition result for the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="935cb-123">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="935cb-123">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <span data-ttu-id="935cb-124"><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="935cb-124"><dt> <strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="935cb-125">GUID che identifica la proprietà per la metrica dei punti per pollice dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="935cb-125">The GUID that identifies the property for the points-per-inch metric of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="935cb-126">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="935cb-126">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <span data-ttu-id="935cb-127"><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="935cb-127"><dt> <strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="935cb-128">GUID che identifica la proprietà relativa al livello di confidenza del riconoscimento nel risultato del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="935cb-128">The GUID that identifies the property for the level of confidence that the recognizer has in the recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="935cb-129">La valutazione della confidenza è disponibile solo per Stati Uniti lingua inglese e per tutti i riconoscitori di movimento in Microsoft Windows XP Tablet PC Edition e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="935cb-129">Confidence evaluation is available only for United States English and all gesture recognizers in Microsoft Windows XP Tablet PC Edition and Windows Vista.</span></span> <span data-ttu-id="935cb-130">Metodi che forniscono la proprietà confidenza per qualsiasi altro riconoscitore restituito E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="935cb-130">Methods that provide the confidence property for any other recognizer return E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <span data-ttu-id="935cb-131"><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="935cb-131"><dt> <strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="935cb-132">GUID che identifica la proprietà per le metriche della riga dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> , ovvero la riga per la quale recuperare le metriche.</span><span class="sxs-lookup"><span data-stu-id="935cb-132">The GUID that identifies the property for the line metrics of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object, which is the line for which to retrieve metrics.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="935cb-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="935cb-133">Remarks</span></span>

<span data-ttu-id="935cb-134">In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut. h, che si trova nella <systemdrive> \\ Directory: programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include directory se è stato installato l'SDK nel percorso predefinito.</span><span class="sxs-lookup"><span data-stu-id="935cb-134">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="935cb-135">In C++, queste costanti sono WCHAR, non BSTR.</span><span class="sxs-lookup"><span data-stu-id="935cb-135">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="935cb-136">Convertirli in BSTR prima di usarli.</span><span class="sxs-lookup"><span data-stu-id="935cb-136">Convert them into BSTRs before use.</span></span> <span data-ttu-id="935cb-137">Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="935cb-137">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="935cb-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="935cb-138">Requirements</span></span>



| <span data-ttu-id="935cb-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="935cb-139">Requirement</span></span> | <span data-ttu-id="935cb-140">Valore</span><span class="sxs-lookup"><span data-stu-id="935cb-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935cb-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="935cb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="935cb-142">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="935cb-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="935cb-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="935cb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="935cb-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="935cb-144">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="935cb-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="935cb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="935cb-146"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="935cb-146"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935cb-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="935cb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935cb-148">**Metodo AlternatesWithConstantPropertyValues**</span><span class="sxs-lookup"><span data-stu-id="935cb-148">**AlternatesWithConstantPropertyValues Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[<span data-ttu-id="935cb-149">**Proprietà ConfidenceAlternates**</span><span class="sxs-lookup"><span data-stu-id="935cb-149">**ConfidenceAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[<span data-ttu-id="935cb-150">**Proprietà LineAlternates**</span><span class="sxs-lookup"><span data-stu-id="935cb-150">**LineAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[<span data-ttu-id="935cb-151">**Interfaccia IInkRecognitionAlternates**</span><span class="sxs-lookup"><span data-stu-id="935cb-151">**IInkRecognitionAlternates Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 





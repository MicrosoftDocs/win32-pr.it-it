---
description: Recupera i dati specifici dell'applicazione o altri dati della proprietà per l'identificatore specificato.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'Metodo IContextNode:: GetPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751847"
---
# <a name="icontextnodegetpropertydata-method"></a><span data-ttu-id="39474-103">Metodo IContextNode:: GetPropertyData</span><span class="sxs-lookup"><span data-stu-id="39474-103">IContextNode::GetPropertyData method</span></span>

<span data-ttu-id="39474-104">Recupera i dati specifici dell'applicazione o altri dati della proprietà per l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="39474-104">Retrieves application-specific data or other property data for the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="39474-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39474-105">Syntax</span></span>


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a><span data-ttu-id="39474-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39474-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39474-107">*pPropertyDataId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39474-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39474-108">Identificatore per i dati.</span><span class="sxs-lookup"><span data-stu-id="39474-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="39474-109">*pulPropertyDataSize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="39474-109">*pulPropertyDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39474-110">Dimensioni dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="39474-110">The size of the data in bytes.</span></span> <span data-ttu-id="39474-111">Il valore passato non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="39474-111">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="39474-112">*ppbPropertyData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="39474-112">*ppbPropertyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39474-113">Puntatore a una matrice di Unsigned Integer a 8 bit che contiene i dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="39474-113">A pointer to an 8-bit unsigned integer array that contains the property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39474-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39474-114">Return value</span></span>

<span data-ttu-id="39474-115">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="39474-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="39474-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="39474-116">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="39474-117">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppbPropertyData* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="39474-117">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertyData* when you no longer need the information.</span></span>

 

<span data-ttu-id="39474-118">Oltre a recuperare i dati specifici dell'applicazione aggiunti con [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md), questo metodo viene usato per recuperare le proprietà comuni descritte dalle costanti delle [proprietà del nodo di contesto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="39474-118">In addition to retrieving application-specific data that was added with [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md), this method is used to retrieve common properties that are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

<span data-ttu-id="39474-119">Le proprietà di tipo stringa includono:</span><span class="sxs-lookup"><span data-stu-id="39474-119">The string-type properties include:</span></span>

-   <span data-ttu-id="39474-120">GUID \_ CNP \_ RECOGNIZEDSTRING</span><span class="sxs-lookup"><span data-stu-id="39474-120">GUID\_CNP\_RECOGNIZEDSTRING</span></span>
-   <span data-ttu-id="39474-121">GUID \_ CNP \_ ShapeName</span><span class="sxs-lookup"><span data-stu-id="39474-121">GUID\_CNP\_SHAPENAME</span></span>
-   <span data-ttu-id="39474-122">GUID \_ AHP \_ ANALYSISHINTNAME</span><span class="sxs-lookup"><span data-stu-id="39474-122">GUID\_AHP\_ANALYSISHINTNAME</span></span>
-   <span data-ttu-id="39474-123">GUID \_ AHP \_ PREFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="39474-123">GUID\_AHP\_PREFIXTEXT</span></span>
-   <span data-ttu-id="39474-124">GUID \_ AHP \_ SUFFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="39474-124">GUID\_AHP\_SUFFIXTEXT</span></span>
-   <span data-ttu-id="39474-125">controllo controllo \_ AHP GUID \_</span><span class="sxs-lookup"><span data-stu-id="39474-125">GUID\_AHP\_FACTOID</span></span>

<span data-ttu-id="39474-126">Il valore restituito è \**WCHAR \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a \**\* WCHAR*_ la lunghezza restituita è `(length of the string + 1) _ sizeof(WCHAR)` .</span><span class="sxs-lookup"><span data-stu-id="39474-126">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `(length of the string + 1) _ sizeof(WCHAR)`.</span></span>

<span data-ttu-id="39474-127">Le proprietà di tipo booleano includono:</span><span class="sxs-lookup"><span data-stu-id="39474-127">The Boolean-type properties include:</span></span>

-   <span data-ttu-id="39474-128">GUID \_ AHP \_ OVERRIDELANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="39474-128">GUID\_AHP\_OVERRIDELANGUAGEID</span></span>
-   <span data-ttu-id="39474-129">GUID \_ AHP \_ COERCETOFACTOID</span><span class="sxs-lookup"><span data-stu-id="39474-129">GUID\_AHP\_COERCETOFACTOID</span></span>
-   <span data-ttu-id="39474-130">GUID \_ AHP \_ WORDMODE</span><span class="sxs-lookup"><span data-stu-id="39474-130">GUID\_AHP\_WORDMODE</span></span>

<span data-ttu-id="39474-131">Il valore restituito è la **variante \_ bool**.</span><span class="sxs-lookup"><span data-stu-id="39474-131">The return value is **VARIANT\_BOOL**.</span></span> <span data-ttu-id="39474-132">Se si esegue il cast del \* parametro *ppbPropertyData* a \**Variant \_ bool \** _ la lunghezza restituita è `sizeof(VARIANT_BOOL)` .</span><span class="sxs-lookup"><span data-stu-id="39474-132">If you cast the \**ppbPropertyData* parameter to \**VARIANT\_BOOL\** _ its returned length is `sizeof(VARIANT_BOOL)`.</span></span>

<span data-ttu-id="39474-133">GUID \_ AHP \_ guide è una proprietà di tipo guida.</span><span class="sxs-lookup"><span data-stu-id="39474-133">GUID\_AHP\_GUIDE is a guide-type property.</span></span> <span data-ttu-id="39474-134">Il valore restituito è _*InkAnalysisRecognitionGuide \**_.</span><span class="sxs-lookup"><span data-stu-id="39474-134">The return value is _*InkAnalysisRecognitionGuide\**_.</span></span> <span data-ttu-id="39474-135">Se si esegue il cast del \_ parametro *ppbPropertyData* a \**InkAnalysisRecognitionGuide \** _ la lunghezza restituita è `sizeof(InkAnalysisRecognitionGuide)` .</span><span class="sxs-lookup"><span data-stu-id="39474-135">If you cast the \_*ppbPropertyData* parameter to \**InkAnalysisRecognitionGuide\** _ its returned length is `sizeof(InkAnalysisRecognitionGuide)`.</span></span>

<span data-ttu-id="39474-136">Le proprietà di tipo integer includono:</span><span class="sxs-lookup"><span data-stu-id="39474-136">Integer-type properties include:</span></span>

-   <span data-ttu-id="39474-137">GUID \_ CNP \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="39474-137">GUID\_CNP\_LINENUMBER</span></span>
-   <span data-ttu-id="39474-138">GUID \_ CNP \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="39474-138">GUID\_CNP\_POINTSPERINCH</span></span>
-   <span data-ttu-id="39474-139">GUID \_ CNP \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="39474-139">GUID\_CNP\_CONFIDENCELEVEL</span></span>
-   <span data-ttu-id="39474-140">\_conferma CNP \_ GUID</span><span class="sxs-lookup"><span data-stu-id="39474-140">GUID\_CNP\_CONFIRMATION</span></span>
-   <span data-ttu-id="39474-141">GUID \_ CNP \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="39474-141">GUID\_CNP\_MAXIMUMSTROKECOUNT</span></span>
-   <span data-ttu-id="39474-142">\_ \_ segmentazione GUID CNP</span><span class="sxs-lookup"><span data-stu-id="39474-142">GUID\_CNP\_SEGMENTATION</span></span>
-   <span data-ttu-id="39474-143">GUID \_ CNP \_ ALIGNMENTLEVEL</span><span class="sxs-lookup"><span data-stu-id="39474-143">GUID\_CNP\_ALIGNMENTLEVEL</span></span>

<span data-ttu-id="39474-144">Il valore restituito è _*Long \**_.</span><span class="sxs-lookup"><span data-stu-id="39474-144">The return value is _*LONG\**_.</span></span> <span data-ttu-id="39474-145">Se si esegue il cast del \_ parametro *ppbPropertyData* a \**Long \** _ la lunghezza restituita è `sizeof(LONG)` .</span><span class="sxs-lookup"><span data-stu-id="39474-145">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)`.</span></span>

<span data-ttu-id="39474-146">Metrica riga: le proprietà del tipo includono:</span><span class="sxs-lookup"><span data-stu-id="39474-146">Line metrics-type properties include:</span></span>

-   <span data-ttu-id="39474-147">GUID \_ CNP \_ ascenders</span><span class="sxs-lookup"><span data-stu-id="39474-147">GUID\_CNP\_ASCENDERS</span></span>
-   <span data-ttu-id="39474-148">\_CNP \_ DISCENDEnti GUID</span><span class="sxs-lookup"><span data-stu-id="39474-148">GUID\_CNP\_DESCENDERS</span></span>
-   <span data-ttu-id="39474-149">\_linea di \_ base CNP GUID</span><span class="sxs-lookup"><span data-stu-id="39474-149">GUID\_CNP\_BASELINE</span></span>
-   <span data-ttu-id="39474-150">linea \_ media CNP GUID \_</span><span class="sxs-lookup"><span data-stu-id="39474-150">GUID\_CNP\_MIDLINE</span></span>

<span data-ttu-id="39474-151">Il valore restituito è _*Long \**_.</span><span class="sxs-lookup"><span data-stu-id="39474-151">The return value is _*LONG\**_.</span></span> <span data-ttu-id="39474-152">Se si esegue il cast del \_ parametro *ppbPropertyData* a \**\* Long* _ la lunghezza restituita è, indicando `sizeof(LONG)_4` i valori (x, y) per i punti iniziali seguiti dai valori (x, y) per i punti finali.</span><span class="sxs-lookup"><span data-stu-id="39474-152">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_4`, signifying the (x, y) values for the starting points followed by the (x, y) values for the ending points.</span></span>

<span data-ttu-id="39474-153">GUID \_ CNP \_ TEXTRECOGNIZERID è una proprietà **GUID** .</span><span class="sxs-lookup"><span data-stu-id="39474-153">GUID\_CNP\_TEXTRECOGNIZERID is a **GUID** property.</span></span> <span data-ttu-id="39474-154">Il valore restituito è \**GUID \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* in \**\* GUID*_ , la lunghezza restituita è `sizeof(GUID)` .</span><span class="sxs-lookup"><span data-stu-id="39474-154">The return value is \**GUID\**_. If you cast the \_*ppbPropertyData* parameter to \**GUID\**_ its returned length is `sizeof(GUID)`.</span></span>

<span data-ttu-id="39474-155">GUID \_ CNP \_ ROTATEDBOUNDINGBOX è una proprietà del rettangolo di delimitazione ruotata.</span><span class="sxs-lookup"><span data-stu-id="39474-155">GUID\_CNP\_ROTATEDBOUNDINGBOX is a rotated bounding box property.</span></span> <span data-ttu-id="39474-156">Il valore restituito è _*Long \**_.</span><span class="sxs-lookup"><span data-stu-id="39474-156">The return value is _*LONG\**_.</span></span> <span data-ttu-id="39474-157">Se si esegue il cast del \_ parametro *ppbPropertyData* a \**\* Long* _ la lunghezza restituita è, indicando `sizeof(LONG)_8` i valori (x, y) per i quattro angoli della casella.</span><span class="sxs-lookup"><span data-stu-id="39474-157">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_8`, signifying the (x, y) values for the four corners of the box.</span></span>

<span data-ttu-id="39474-158">GUID \_ CNP \_ Hotpoint è una proprietà di punti sensibili.</span><span class="sxs-lookup"><span data-stu-id="39474-158">GUID\_CNP\_HOTPOINT is a hot point property.</span></span> <span data-ttu-id="39474-159">Il valore restituito è \**Long \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a \**Long \**_ la lunghezza restituita è, indicando `sizeof(LONG)_2` i valori (x, y) per il punto.</span><span class="sxs-lookup"><span data-stu-id="39474-159">The return value is \**LONG\**_. If you cast the \_*ppbPropertyData* parameter to \**LONG\**_ its returned length is `sizeof(LONG)_2`, signifying the (x, y) values for the point.</span></span>

<span data-ttu-id="39474-160">GUID \_ AHP \_ è una proprietà dell'elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="39474-160">GUID\_AHP\_WORDLIST is a word list property.</span></span> <span data-ttu-id="39474-161">Il valore restituito è \**WCHAR \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a \**\* WCHAR*_ la lunghezza restituita è `n _ sizeof(WCHAR)` , dove `n` è la somma delle lunghezze di stringa del numero di stringhe nell'elenco più 1 per ogni carattere di terminazione **null** per ogni stringa.</span><span class="sxs-lookup"><span data-stu-id="39474-161">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `n _ sizeof(WCHAR)`, where `n` is the sum of the string lengths of the number of strings in the list plus 1 for each **NULL** termination character for each string.</span></span>

## <a name="examples"></a><span data-ttu-id="39474-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="39474-162">Examples</span></span>

<span data-ttu-id="39474-163">Questo esempio mostra un metodo che accede alla proprietà del nodo di contesto AlignmentLevel di un tipo di nodo di contesto di paragrafo.</span><span class="sxs-lookup"><span data-stu-id="39474-163">This example shows a method that accesses the AlignmentLevel context node property of a Paragraph context node type.</span></span>


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="39474-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39474-164">Requirements</span></span>



| <span data-ttu-id="39474-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="39474-165">Requirement</span></span> | <span data-ttu-id="39474-166">Valore</span><span class="sxs-lookup"><span data-stu-id="39474-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39474-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39474-167">Minimum supported client</span></span><br/> | <span data-ttu-id="39474-168">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="39474-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="39474-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39474-169">Minimum supported server</span></span><br/> | <span data-ttu-id="39474-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="39474-170">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="39474-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39474-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="39474-172"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="39474-172"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="39474-173">DLL</span><span class="sxs-lookup"><span data-stu-id="39474-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39474-174"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39474-174"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="39474-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39474-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39474-176">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="39474-176">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="39474-177">**IContextNode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="39474-177">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="39474-178">**IContextNode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="39474-178">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="39474-179">**IContextNode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="39474-179">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="39474-180">**IContextNode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="39474-180">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="39474-181">**IContextNode:: LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="39474-181">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="39474-182">**IContextNode:: SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="39474-182">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="39474-183">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="39474-183">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Specifica gli attributi di un IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Enumerazione RecognizerCapabilities (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313445"
---
# <a name="recognizercapabilities-enumeration"></a><span data-ttu-id="8499b-103">Enumerazione RecognizerCapabilities</span><span class="sxs-lookup"><span data-stu-id="8499b-103">RecognizerCapabilities enumeration</span></span>

<span data-ttu-id="8499b-104">Specifica gli attributi di un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="8499b-104">Specifies the attributes of an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8499b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8499b-105">Syntax</span></span>


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a><span data-ttu-id="8499b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="8499b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8499b-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ nessuno**</span><span class="sxs-lookup"><span data-stu-id="8499b-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC\_None**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-108">Nessuna funzionalità specificata.</span><span class="sxs-lookup"><span data-stu-id="8499b-108">No capabilities specified.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**\_DONOTCARE RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC\_DoNotCare**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-110">Ignora tutti gli altri flag impostati.</span><span class="sxs-lookup"><span data-stu-id="8499b-110">Ignores all other flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="8499b-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC\_Object**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-112">Supporta il riconoscimento degli oggetti. in caso contrario, riconosce solo il testo.</span><span class="sxs-lookup"><span data-stu-id="8499b-112">Supports object recognition; otherwise, recognizes only text.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**\_FREEINPUT RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC\_FreeInput**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-114">Supporta l'input libero, in cui viene immesso l'input penna senza utilizzare una guida per il riconoscimento, ad esempio una riga o una casella.</span><span class="sxs-lookup"><span data-stu-id="8499b-114">Supports free input, where ink is entered without the use of a recognition guide, such as a line or a box.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**\_LINEDINPUT RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC\_LinedInput**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-116">Supporta l'input rigato, che è simile alla scrittura su un foglio di carta.</span><span class="sxs-lookup"><span data-stu-id="8499b-116">Supports lined input, which is similar to writing on lined paper.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**\_BOXEDINPUT RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC\_BoxedInput**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-118">Supporta l'input boxed, in cui ogni carattere o parola viene immesso in una casella.</span><span class="sxs-lookup"><span data-stu-id="8499b-118">Supports boxed input, where each character or word is entered in a box.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**\_CHARACTERAUTOCOMPLETIONINPUT RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC\_CharacterAutoCompletionInput**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-120">Supporta il completamento automatico del carattere.</span><span class="sxs-lookup"><span data-stu-id="8499b-120">Supports character Autocomplete.</span></span> <span data-ttu-id="8499b-121">I riconoscitori che supportano il completamento automatico del carattere richiedono input boxed.</span><span class="sxs-lookup"><span data-stu-id="8499b-121">Recognizers that support character Autocomplete require boxed input.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**\_RIGHTANDDOWN RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC\_RightAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-123">Supporta l'input della grafia nell'ordine a destra e in basso, ad esempio nelle lingue occidentali e in alcune lingue asiatiche orientali.</span><span class="sxs-lookup"><span data-stu-id="8499b-123">Supports handwriting input in right and down order, such as in western languages and some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**\_LEFTANDDOWN RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC\_LeftAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-125">Supporta l'input della grafia nell'ordine di sinistra e in basso, ad esempio in lingua ebraica e araba.</span><span class="sxs-lookup"><span data-stu-id="8499b-125">Supports handwriting input in left and down order, such as in Hebrew and Arabic languages.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**\_DOWNANDLEFT RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC\_DownAndLeft**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-127">Supporta l'input della grafia nell'ordine inverso e a sinistra, ad esempio in alcune lingue asiatiche orientali.</span><span class="sxs-lookup"><span data-stu-id="8499b-127">Supports handwriting input in down and left order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**\_DOWNANDRIGHT RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC\_DownAndRight**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-129">Supporta l'input della grafia in ordine inverso e corretto, ad esempio in alcune lingue asiatiche orientali.</span><span class="sxs-lookup"><span data-stu-id="8499b-129">Supports handwriting input in down and right order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**\_ARBITRARYANGLE RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC\_ArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-131">Supporta testo scritto a angoli arbitrari.</span><span class="sxs-lookup"><span data-stu-id="8499b-131">Supports text written at arbitrary angles.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**\_Reticolo RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC\_Lattice**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-133">Supporta la restituzione di un reticolo come alternativa a una stringa per i risultati del riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="8499b-133">Supports returning a lattice as an alternative a string for handwriting recognition results.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**\_ADVISEINKCHANGE RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC\_AdviseInkChange**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-135">Supporta l'interruzione del riconoscimento in background, ad esempio quando l'input penna è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="8499b-135">Supports interrupting background recognition, such as when the ink has changed.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**\_STROKEREORDER RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC\_StrokeReorder**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-137">Supporta l'ordine dei tratti, spaziale e temporale, viene gestito come parte dell'operazione di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="8499b-137">Supports that stroke order, spatial and temporal, is handled as part of the recognition operation.</span></span> <span data-ttu-id="8499b-138">Il [**IInkAnalyzer**](iinkanalyzer.md) non riordina i tratti prima di inviare input penna al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="8499b-138">The [**IInkAnalyzer**](iinkanalyzer.md) does not reorder strokes before sending ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="8499b-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**\_Personalizzabile RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC\_Personalizable**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-140">Supporta la grafia personalizzata, in cui il riconoscimento migliora il riconoscimento quando viene esposto alla stessa grafia nel tempo.</span><span class="sxs-lookup"><span data-stu-id="8499b-140">Supports personalized handwriting, where the recognizer improves recognition when exposed to the same handwriting over time.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**\_PREFERSARBITRARYANGLE RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC\_PrefersArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-142">Il [**IInkAnalyzer**](iinkanalyzer.md) non deve ruotare la grafia a un orientamento orizzontale prima di inviare l'input penna al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="8499b-142">The [**IInkAnalyzer**](iinkanalyzer.md) need not rotate the handwriting to a horizontal orientation before sending the ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="8499b-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**\_PREFERSPARAGRAPHBREAKING RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC\_PrefersParagraphBreaking**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-144">Il [**IInkAnalyzer**](iinkanalyzer.md) deve inviare interi paragrafi di input penna al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), consentendo al **IInkAnalysisRecognizer** di eseguire le interruzioni di riga e di parola (o carattere).</span><span class="sxs-lookup"><span data-stu-id="8499b-144">The [**IInkAnalyzer**](iinkanalyzer.md) should send entire paragraphs of ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), allowing the **IInkAnalysisRecognizer** to do the line breaking and word (or character) breaking.</span></span>

</dd> <dt>

<span data-ttu-id="8499b-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**\_PREFERSSEGMENTATIONRECOGNITION RC**</span><span class="sxs-lookup"><span data-stu-id="8499b-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC\_PrefersSegmentationRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="8499b-146">Riconosce solo una parola o un carattere per ogni operazione di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="8499b-146">Recognizes only one word or character per recognition operation.</span></span> <span data-ttu-id="8499b-147">[**IInkAnalyzer**](iinkanalyzer.md) esegue la segmentazione sulla grafia e invia un solo segmento alla volta al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="8499b-147">The [**IInkAnalyzer**](iinkanalyzer.md) performs segmentation on the handwriting and sends only one segment at a time to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8499b-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="8499b-148">Remarks</span></span>

<span data-ttu-id="8499b-149">Questa enumerazione consente una combinazione bit per bit dei relativi valori dei membri.</span><span class="sxs-lookup"><span data-stu-id="8499b-149">This enumeration allows a bitwise combination of its member values.</span></span> <span data-ttu-id="8499b-150">Usare questa enumerazione per trovare un riconoscimento input penna installato che supporta gli attributi necessari.</span><span class="sxs-lookup"><span data-stu-id="8499b-150">Use this enumeration to find an installed ink recognizer that supports the attributes you need.</span></span>

## <a name="requirements"></a><span data-ttu-id="8499b-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8499b-151">Requirements</span></span>



| <span data-ttu-id="8499b-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="8499b-152">Requirement</span></span> | <span data-ttu-id="8499b-153">Valore</span><span class="sxs-lookup"><span data-stu-id="8499b-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8499b-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8499b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8499b-155">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8499b-155">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8499b-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8499b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8499b-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8499b-157">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8499b-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8499b-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="8499b-159"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8499b-159"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8499b-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8499b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8499b-161">**IInkAnalysisRecognizer:: GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8499b-161">**IInkAnalysisRecognizer::GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[<span data-ttu-id="8499b-162">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="8499b-162">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





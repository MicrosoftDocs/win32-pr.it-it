---
title: Messaggio di EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Imposta lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- Controlli di Windows Message EM_SETTYPOGRAPHYOPTIONS
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964385"
---
# <a name="em_settypographyoptions-message"></a><span data-ttu-id="f8ed9-104">\_Messaggio SETTYPOGRAPHYOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="f8ed9-104">EM\_SETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="f8ed9-105">Imposta lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-105">Sets the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8ed9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8ed9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ed9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8ed9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ed9-108">Specifica uno o entrambi i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-108">Specifies one or both of the following values.</span></span>



| <span data-ttu-id="f8ed9-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f8ed9-109">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="f8ed9-110">Significato</span><span class="sxs-lookup"><span data-stu-id="f8ed9-110">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <span data-ttu-id="f8ed9-111"><dt>**A \_ ADVANCEDTYPOGRAPHY**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ed9-111"><dt>**TO\_ADVANCEDTYPOGRAPHY** </dt></span></span> </dl> | <span data-ttu-id="f8ed9-112">L'interruzioni di riga e la formattazione di riga avanzate sono attivate.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-112">Advanced line breaking and line formatting is turned on.</span></span> <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <span data-ttu-id="f8ed9-113"><dt>**a \_ SIMPLELINEBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ed9-113"><dt>**TO\_SIMPLELINEBREAK**</dt></span></span> </dl>             | <span data-ttu-id="f8ed9-114">Interruzioni di riga più veloci per testo semplice (richiede **\_ ADVANCEDTYPOGRAPHY**).</span><span class="sxs-lookup"><span data-stu-id="f8ed9-114">Faster line breaking for simple text (requires **TO\_ADVANCEDTYPOGRAPHY**).</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="f8ed9-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8ed9-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ed9-116">Maschera costituita da uno o più flag in *wParam*.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-116">A mask consisting of one or more of the flags in *wParam*.</span></span> <span data-ttu-id="f8ed9-117">Verranno impostati o cancellati solo i flag impostati in questa maschera.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-117">Only the flags that are set in this mask will be set or cleared.</span></span> <span data-ttu-id="f8ed9-118">In questo modo è possibile impostare o cancellare un flag singolo senza leggere gli Stati del flag corrente.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-118">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ed9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8ed9-119">Return value</span></span>

<span data-ttu-id="f8ed9-120">Restituisce **true** se *wParam* è valido; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-120">Returns **TRUE** if *wParam* is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ed9-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8ed9-121">Remarks</span></span>

<span data-ttu-id="f8ed9-122">L'interruzioni di riga avanzate viene attivata automaticamente dal controllo Rich Edit quando necessario, ad esempio per la gestione di alfabeti non latini, come l'arabo e l'ebraico, e per la matematica.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-122">Advanced line breaking is turned on automatically by the rich edit control when needed, such as for handling complex scripts like Arabic and Hebrew, and for mathematics.</span></span> <span data-ttu-id="f8ed9-123">È necessario anche per i paragrafi giustificati, la sillabazione e altre funzionalità tipografiche.</span><span class="sxs-lookup"><span data-stu-id="f8ed9-123">It s also needed for justified paragraphs, hyphenation, and other typographic features.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ed9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8ed9-124">Requirements</span></span>



| <span data-ttu-id="f8ed9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8ed9-125">Requirement</span></span> | <span data-ttu-id="f8ed9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f8ed9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ed9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8ed9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ed9-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8ed9-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8ed9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8ed9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ed9-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8ed9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8ed9-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f8ed9-131">Redistributable</span></span><br/>          | <span data-ttu-id="f8ed9-132">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="f8ed9-132">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="f8ed9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8ed9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8ed9-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ed9-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ed9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8ed9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ed9-136">**\_GETTYPOGRAPHYOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="f8ed9-136">**EM\_GETTYPOGRAPHYOPTIONS**</span></span>](em-gettypographyoptions.md)
</dt> </dl>

 

 






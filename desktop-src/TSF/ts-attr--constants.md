---
title: Costanti TS_ATTR_ (Textstor. h)
description: '\_ \_ Per ottenere e modificare i valori degli attributi del documento, vengono utilizzate le costanti di Servizi terminal. Queste costanti formano i possibili valori dei flag bit nei metodi ITextStoreACP e ITextStoreAnchor.'
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477998"
---
# <a name="ts_attr_-constants"></a><span data-ttu-id="955a8-104">\_Costanti attr \_ di Servizi terminal \*</span><span class="sxs-lookup"><span data-stu-id="955a8-104">TS\_ATTR\_\* Constants</span></span>

<span data-ttu-id="955a8-105">\_ \_ \* Per ottenere e modificare i valori degli attributi del documento vengono usate le costanti attr di Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="955a8-105">The TS\_ATTR\_\* constants are used to obtain and change the values of document attributes.</span></span> <span data-ttu-id="955a8-106">Queste costanti formano i possibili valori dei flag bit nei metodi [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="955a8-106">These constants form possible values of bitfield flags in [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>



| <span data-ttu-id="955a8-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="955a8-107">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="955a8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="955a8-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <span data-ttu-id="955a8-109"><dt>**Servizi terminal \_ ATTR \_ trova \_ indietro**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="955a8-109"><dt>**TS\_ATTR\_FIND\_BACKWARDS**</dt> <dt>( 0x1 )</dt></span></span> </dl>        | <span data-ttu-id="955a8-110">Eseguire una ricerca all'indietro dal carattere iniziale o dalla posizione di ancoraggio per la posizione in cui si verifica una transizione in un valore di attributo documento.</span><span class="sxs-lookup"><span data-stu-id="955a8-110">Search backward from the start character or anchor position for the position where a transition occurs in a document attribute value.</span></span> <span data-ttu-id="955a8-111">Il valore predefinito è ricerca in futuro.</span><span class="sxs-lookup"><span data-stu-id="955a8-111">The default is search forward.</span></span><br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <span data-ttu-id="955a8-112"><dt>**Servizi terminal \_ \_ \_ \_ Offset ricerca attr**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="955a8-112"><dt>**TS\_ATTR\_FIND\_WANT\_OFFSET**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="955a8-113">Restituisce il numero di caratteri tra il carattere iniziale o la posizione di ancoraggio (**acpStart** in [ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) o **PaStart** in [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) e la posizione in cui si verifica la transizione di un attributo.</span><span class="sxs-lookup"><span data-stu-id="955a8-113">Return the number of characters between the start character or anchor position (**acpStart** in [ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) or **paStart** in [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) and the position at which an attribute transition occurs.</span></span><br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <span data-ttu-id="955a8-114"><dt>**Servizi terminal \_ ATTR \_ Find \_ updatestart**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="955a8-114"><dt>**TS\_ATTR\_FIND\_UPDATESTART**</dt> <dt>( 0x4 )</dt></span></span> </dl>  | <span data-ttu-id="955a8-115">Usato da [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) per posizionare l'ancoraggio di input alla successiva transizione dell'attributo, se ne viene trovata una.</span><span class="sxs-lookup"><span data-stu-id="955a8-115">Used by [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) to position the input anchor at the next attribute transition, if one is found.</span></span> <span data-ttu-id="955a8-116">In caso contrario, l'ancoraggio di input non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="955a8-116">Otherwise the input anchor is not modified.</span></span><br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <span data-ttu-id="955a8-117"><dt>**Servizi terminal \_ \_ \_ \_ Valore di Find want per attr**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="955a8-117"><dt>**TS\_ATTR\_FIND\_WANT\_VALUE**</dt> <dt>( 0x8 )</dt></span></span> </dl>    | <span data-ttu-id="955a8-118">Caricare i valori dell'attributo Document supportati nella struttura [ \_ ATTRVAL di Servizi terminal](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .</span><span class="sxs-lookup"><span data-stu-id="955a8-118">Load supported document attribute values into the [TS\_ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) structure.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <span data-ttu-id="955a8-119"><dt>**Servizi terminal \_ ATTR \_ Find \_ want \_ end**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="955a8-119"><dt>**TS\_ATTR\_FIND\_WANT\_END**</dt> <dt>( 0x10 )</dt></span></span> </dl>         | <span data-ttu-id="955a8-120">Usato da [ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) e [ITextStoreAnchor:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) per ottenere i valori dell'attributo del documento che terminano con il carattere o la posizione di ancoraggio specificata.</span><span class="sxs-lookup"><span data-stu-id="955a8-120">Used by [ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) and [ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) to obtain the document attribute values that end at the specified character or anchor position.</span></span><br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <span data-ttu-id="955a8-121"><dt>**Servizi terminal \_ ATTR \_ Find \_ Hidden**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="955a8-121"><dt>**TS\_ATTR\_FIND\_HIDDEN**</dt> <dt>( 0x20 )</dt></span></span> </dl>                | <span data-ttu-id="955a8-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="955a8-122">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="955a8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="955a8-123">Requirements</span></span>



| <span data-ttu-id="955a8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="955a8-124">Requirement</span></span> | <span data-ttu-id="955a8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="955a8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="955a8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="955a8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="955a8-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="955a8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="955a8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="955a8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="955a8-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="955a8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="955a8-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="955a8-130">Redistributable</span></span><br/>          | <span data-ttu-id="955a8-131">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="955a8-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="955a8-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="955a8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="955a8-133"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="955a8-133"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="955a8-134">IDL</span><span class="sxs-lookup"><span data-stu-id="955a8-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="955a8-135"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="955a8-135"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="955a8-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="955a8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955a8-137">ATTRID di Servizi terminal \_</span><span class="sxs-lookup"><span data-stu-id="955a8-137">TS\_ATTRID</span></span>](ts-attrid.md)
</dt> <dt>

[<span data-ttu-id="955a8-138">ATTRVAL di Servizi terminal \_</span><span class="sxs-lookup"><span data-stu-id="955a8-138">TS\_ATTRVAL</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[<span data-ttu-id="955a8-139">ITextStoreACP:: FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="955a8-139">ITextStoreACP::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="955a8-140">ITextStoreACP:: RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="955a8-140">ITextStoreACP::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="955a8-141">ITextStoreAnchor::FindNextAttrTransition</span><span class="sxs-lookup"><span data-stu-id="955a8-141">ITextStoreAnchor::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="955a8-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span><span class="sxs-lookup"><span data-stu-id="955a8-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 






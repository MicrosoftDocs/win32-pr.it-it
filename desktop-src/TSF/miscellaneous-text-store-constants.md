---
title: Costanti di archivio di testo varie (Textstor. h)
description: Le costanti di archivio di testo varie impostano determinate proprietà per gli archivi di testo.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120918"
---
# <a name="miscellaneous-text-store-constants"></a><span data-ttu-id="826ff-103">Costanti di archivio di testo varie</span><span class="sxs-lookup"><span data-stu-id="826ff-103">Miscellaneous Text Store Constants</span></span>

<span data-ttu-id="826ff-104">Le costanti di archivio di testo varie impostano determinate proprietà per gli archivi di testo.</span><span class="sxs-lookup"><span data-stu-id="826ff-104">The miscellaneous text store constants set certain properties for text stores.</span></span>



| <span data-ttu-id="826ff-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="826ff-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="826ff-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="826ff-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <span data-ttu-id="826ff-107"><dt>**Servizi terminal \_ \_Selezione predefinita**</dt> <dt>((ulong)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="826ff-107"><dt>**TS\_DEFAULT\_SELECTION**</dt> <dt>( ( ULONG )-1 )</dt></span></span> </dl> | <span data-ttu-id="826ff-108">Se il parametro *ulIndex* di [ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) è impostato su questo valore, viene ottenuta la selezione predefinita.</span><span class="sxs-lookup"><span data-stu-id="826ff-108">If the *ulIndex* parameter of [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) is set to this value, the default selection is obtained.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <span data-ttu-id="826ff-109"><dt>**Servizi terminal \_ GEA \_ Hidden**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="826ff-109"><dt>**TS\_GEA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="826ff-110">Se il parametro *dwFlags* di [ITextStoreAnchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) è impostato su questo valore, un oggetto incorporato può trovarsi all'interno di un testo nascosto.</span><span class="sxs-lookup"><span data-stu-id="826ff-110">If *dwFlags* parameter of [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) is set to this value, an embedded object can be located within hidden text.</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <span data-ttu-id="826ff-111"><dt>**Servizi terminal \_ GTA \_ nascosto**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="826ff-111"><dt>**TS\_GTA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="826ff-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="826ff-112">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <span data-ttu-id="826ff-113"><dt>**Servizi terminal \_ \_Correzione St**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="826ff-113"><dt>**TS\_ST\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="826ff-114">Se il parametro *dwFlags* di [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)o [ITextStoreACPSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) è impostato su questo valore, il testo è una trasformazione (correzione) del contenuto esistente e vengono mantenute le informazioni di markup (metadati) speciali, ad esempio i dati del file con estensione wav o un identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="826ff-114">If *dwFlags* parameter of [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext), or [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <span data-ttu-id="826ff-115"><dt>**Servizi terminal \_ \_Correzione TC**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="826ff-115"><dt>**TS\_TC\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="826ff-116">Se il parametro *dwFlags* di [ITextStoreAnchorSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) è impostato su questo valore, il testo è una trasformazione (correzione) del contenuto esistente e vengono mantenute le informazioni di markup (metadati) speciali, ad esempio i dati del file WAV o un identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="826ff-116">If *dwFlags* parameter of [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <span data-ttu-id="826ff-117"><dt>**Servizi terminal \_ VCOOKIE \_ NUL**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="826ff-117"><dt>**TS\_VCOOKIE\_NUL**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                    | <span data-ttu-id="826ff-118">Utilizzato internamente da TSF.</span><span class="sxs-lookup"><span data-stu-id="826ff-118">Used internally by TSF.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="826ff-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="826ff-119">Requirements</span></span>



| <span data-ttu-id="826ff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="826ff-120">Requirement</span></span> | <span data-ttu-id="826ff-121">Valore</span><span class="sxs-lookup"><span data-stu-id="826ff-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="826ff-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="826ff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="826ff-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="826ff-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="826ff-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="826ff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="826ff-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="826ff-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="826ff-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="826ff-126">Redistributable</span></span><br/>          | <span data-ttu-id="826ff-127">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="826ff-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="826ff-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="826ff-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="826ff-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="826ff-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="826ff-130">IDL</span><span class="sxs-lookup"><span data-stu-id="826ff-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="826ff-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="826ff-131"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826ff-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="826ff-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826ff-133">ITfContext:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="826ff-133">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="826ff-134">ITextStoreACP:: SetText</span><span class="sxs-lookup"><span data-stu-id="826ff-134">ITextStoreACP::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[<span data-ttu-id="826ff-135">ITextStoreAnchor:: SetText</span><span class="sxs-lookup"><span data-stu-id="826ff-135">ITextStoreAnchor::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[<span data-ttu-id="826ff-136">ITextStoreAnchor:: getembedded</span><span class="sxs-lookup"><span data-stu-id="826ff-136">ITextStoreAnchor::GetEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[<span data-ttu-id="826ff-137">ITextStoreACPSink:: OnTextChange</span><span class="sxs-lookup"><span data-stu-id="826ff-137">ITextStoreACPSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="826ff-138">ITextStoreAnchorSink::OnTextChange</span><span class="sxs-lookup"><span data-stu-id="826ff-138">ITextStoreAnchorSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="826ff-139">Costanti del Framework varie</span><span class="sxs-lookup"><span data-stu-id="826ff-139">Miscellaneous Framework Constants</span></span>](miscellaneous-framework-constants.md)
</dt> </dl>

 

 






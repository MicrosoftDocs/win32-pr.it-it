---
title: Costanti del Framework varie (msctf. h)
description: Le costanti del Framework varie indicano le impostazioni per client, processi o testo.
ms.assetid: fa53c1f1-50eb-45eb-b2ea-f236a376d41a
topic_type:
- apiref
api_name:
- TF_CLIENTID_NULL
- TF_INVALID_GUIDATOM
- TF_DEFAULT_SELECTION
- TF_GTP_INCL_TEXT
- TF_HF_OBJECT
- TF_IE_CORRECTION
- TF_INVALID_COOKIE
- TF_INVALID_EDIT_COOKIE
- TF_POPF_ALL
- TF_ST_CORRECTION
- TF_TU_CORRECTION
- TF_US_HIDETIPUI
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9eab083f6763d4244d0720b04c2a22744febc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478424"
---
# <a name="miscellaneous-framework-constants"></a><span data-ttu-id="e3c77-103">Costanti del Framework varie</span><span class="sxs-lookup"><span data-stu-id="e3c77-103">Miscellaneous Framework Constants</span></span>

<span data-ttu-id="e3c77-104">Le costanti del Framework varie indicano le impostazioni per client, processi o testo.</span><span class="sxs-lookup"><span data-stu-id="e3c77-104">Miscellaneous framework constants indicate settings for clients, processes, or text.</span></span>



| <span data-ttu-id="e3c77-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="e3c77-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="e3c77-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3c77-106">Description</span></span>                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <span data-ttu-id="e3c77-107"><dt>**Tf \_ CLIENTId \_ null**</dt> <dt>((TfClientId) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-107"><dt>**TF\_CLIENTID\_NULL**</dt> <dt>((TfClientId)0)</dt></span></span> </dl>                        | <span data-ttu-id="e3c77-108">Indica a un servizio di testo che il client è disattivato.</span><span class="sxs-lookup"><span data-stu-id="e3c77-108">Indicates to a text service that the client is deactivated.</span></span> <span data-ttu-id="e3c77-109">Vedere [TfClientId](tfclientid.md).</span><span class="sxs-lookup"><span data-stu-id="e3c77-109">See [TfClientId](tfclientid.md).</span></span><br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <span data-ttu-id="e3c77-110"><dt>**Tf \_ \_GUIDATOM non valido**</dt> <dt>((TfGuidAtom) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-110"><dt>**TF\_INVALID\_GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt></span></span> </dl>               | <span data-ttu-id="e3c77-111">Il valore [TfGuidAtom](tfguidatom.md) per il processo corrente non è valido.</span><span class="sxs-lookup"><span data-stu-id="e3c77-111">The [TfGuidAtom](tfguidatom.md) value for the current process is invalid.</span></span><br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <span data-ttu-id="e3c77-112"><dt>**Tf \_ \_selezione predefinita**</dt> <dt>( \_ selezione predefinita \_ di servizi Terminal)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-112"><dt>**TF\_DEFAULT\_SELECTION**</dt> <dt>( TS\_DEFAULT\_SELECTION )</dt></span></span> </dl> | <span data-ttu-id="e3c77-113">Utilizzare la selezione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e3c77-113">Use the default selection.</span></span> <span data-ttu-id="e3c77-114">Utilizzato da [ITfContext:: Getselectation](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)e [ITextStoreAnchor:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span><span class="sxs-lookup"><span data-stu-id="e3c77-114">Used by [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection), and [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span></span><br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <span data-ttu-id="e3c77-115"><dt>**Tf \_ \_ \_ Testo**</dt> <dt>(0x1)</dt> di GTP</span><span class="sxs-lookup"><span data-stu-id="e3c77-115"><dt>**TF\_GTP\_INCL\_TEXT**</dt> <dt>( 0x1 )</dt></span></span> </dl>                               | <span data-ttu-id="e3c77-116">Specifica che il metodo [ITfEditRecord:: GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) otterrà la raccolta di oggetti Range che coprono il testo modificato durante la sessione di modifica.</span><span class="sxs-lookup"><span data-stu-id="e3c77-116">Specifies that the [ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) method will obtain the collection of range objects that cover the text changed during the edit session.</span></span><br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <span data-ttu-id="e3c77-117"><dt>**Tf \_ \_Oggetto HF**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-117"><dt>**TF\_HF\_OBJECT**</dt> <dt>( 1 )</dt></span></span> </dl>                                              | <span data-ttu-id="e3c77-118">Lo scorrimento dell'intervallo si interrompe se viene rilevato un oggetto incorporato.</span><span class="sxs-lookup"><span data-stu-id="e3c77-118">The range shift stops if an embedded object is encountered.</span></span> <span data-ttu-id="e3c77-119">Utilizzato nel membro **dwFlags** della struttura [tf \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .</span><span class="sxs-lookup"><span data-stu-id="e3c77-119">Used in **dwFlags** member of [TF\_HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) structure.</span></span><br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <span data-ttu-id="e3c77-120"><dt>**Tf \_ \_Correzione di IE**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-120"><dt>**TF\_IE\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="e3c77-121">Il testo è una trasformazione (correzione) del contenuto esistente, in modo che altri servizi di testo possano mantenere i dati associati al testo originale.</span><span class="sxs-lookup"><span data-stu-id="e3c77-121">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="e3c77-122">Usato nel parametro *dwFlags* di [ITfRange:: InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="e3c77-122">Used in *dwFlags* parameter of [ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span></span><br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <span data-ttu-id="e3c77-123"><dt>**Tf \_ \_Cookie non valido**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-123"><dt>**TF\_INVALID\_COOKIE**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                      | <span data-ttu-id="e3c77-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e3c77-124">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <span data-ttu-id="e3c77-125"><dt>**Tf \_ \_ \_ Cookie di modifica non valido**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-125"><dt>**TF\_INVALID\_EDIT\_COOKIE**</dt> <dt>( 0 )</dt></span></span> </dl>               | <span data-ttu-id="e3c77-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e3c77-126">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <span data-ttu-id="e3c77-127"><dt>**Tf \_ POPF \_ All**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-127"><dt>**TF\_POPF\_ALL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                               | <span data-ttu-id="e3c77-128">Tutti i contesti vengono rimossi dallo stack.</span><span class="sxs-lookup"><span data-stu-id="e3c77-128">All contexts are removed from the stack.</span></span> <span data-ttu-id="e3c77-129">Usato nel parametro *dwFlags* di [ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span><span class="sxs-lookup"><span data-stu-id="e3c77-129">Used in *dwFlags* parameter of [ITfDocumentMgr::Pop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span></span><br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <span data-ttu-id="e3c77-130"><dt>**Tf \_ \_Correzione St**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-130"><dt>**TF\_ST\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="e3c77-131">Il testo è una trasformazione (correzione) del contenuto esistente, in modo che altri servizi di testo possano mantenere i dati associati al testo originale.</span><span class="sxs-lookup"><span data-stu-id="e3c77-131">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="e3c77-132">Usato nel parametro *dwFlags* di [ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span><span class="sxs-lookup"><span data-stu-id="e3c77-132">Used in *dwFlags* parameter of [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span></span><br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <span data-ttu-id="e3c77-133"><dt>**Tf \_ \_Correzione tu**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-133"><dt>**TF\_TU\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                | <span data-ttu-id="e3c77-134">La modifica del testo è il risultato di una trasformazione (correzione) del contenuto esistente.</span><span class="sxs-lookup"><span data-stu-id="e3c77-134">The text change is the result of a transform (correction) of existing content.</span></span> <span data-ttu-id="e3c77-135">Ciò implica che la semantica del testo non è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="e3c77-135">This implies that the semantics of the text have not changed.</span></span> <span data-ttu-id="e3c77-136">Usato nel parametro *dwFlags* di [ITfPropertyStore:: OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span><span class="sxs-lookup"><span data-stu-id="e3c77-136">Used in *dwFlags* parameter of [ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span></span><br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <span data-ttu-id="e3c77-137"><dt>**Tf \_ Stati Uniti \_ HIDETIPUI**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-137"><dt>**TF\_US\_HIDETIPUI**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="e3c77-138">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e3c77-138">Not used.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="e3c77-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3c77-139">Requirements</span></span>



| <span data-ttu-id="e3c77-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3c77-140">Requirement</span></span> | <span data-ttu-id="e3c77-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c77-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c77-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3c77-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e3c77-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3c77-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e3c77-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3c77-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e3c77-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3c77-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e3c77-146">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e3c77-146">Redistributable</span></span><br/>          | <span data-ttu-id="e3c77-147">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e3c77-147">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="e3c77-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3c77-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3c77-149"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-149"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3c77-150">IDL</span><span class="sxs-lookup"><span data-stu-id="e3c77-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3c77-151"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3c77-151"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c77-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3c77-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c77-153">ITextStoreACP:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="e3c77-153">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="e3c77-154">ITextStoreAnchor:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="e3c77-154">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[<span data-ttu-id="e3c77-155">ITfContext:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="e3c77-155">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="e3c77-156">ITfDocumentMgr::P op</span><span class="sxs-lookup"><span data-stu-id="e3c77-156">ITfDocumentMgr::Pop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[<span data-ttu-id="e3c77-157">ITfEditRecord::GetTextAndPropertyUpdates</span><span class="sxs-lookup"><span data-stu-id="e3c77-157">ITfEditRecord::GetTextAndPropertyUpdates</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[<span data-ttu-id="e3c77-158">ITfPropertyStore::OnTextUpdated</span><span class="sxs-lookup"><span data-stu-id="e3c77-158">ITfPropertyStore::OnTextUpdated</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[<span data-ttu-id="e3c77-159">ITfRange::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="e3c77-159">ITfRange::InsertEmbedded</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[<span data-ttu-id="e3c77-160">ITfRange:: SetText</span><span class="sxs-lookup"><span data-stu-id="e3c77-160">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="e3c77-161">TfClientId</span><span class="sxs-lookup"><span data-stu-id="e3c77-161">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="e3c77-162">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="e3c77-162">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="e3c77-163">\_HALTCOND TF</span><span class="sxs-lookup"><span data-stu-id="e3c77-163">TF\_HALTCOND</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 






---
title: Costanti varie del framework (Msctf.h)
description: Le costanti varie del framework indicano le impostazioni per client, processi o testo.
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
ms.openlocfilehash: f9bcd6ad253e71d662cbc713398e65c6a250863e18a9fe2d461a2d93717fb7b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906011"
---
# <a name="miscellaneous-framework-constants"></a>Costanti varie del framework

Le costanti varie del framework indicano le impostazioni per client, processi o testo.



| Costante/valore                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**TF \_ CLIENTID \_ NULL**</dt> <dt>((TfClientId)0)</dt> </dl>                        | Indica a un servizio di testo che il client è disattivato. Vedere [TfClientId.](tfclientid.md)<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**TF \_ INVALID \_ GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt> </dl>               | Il [valore TfGuidAtom](tfguidatom.md) per il processo corrente non è valido.<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**TF \_ SELEZIONE \_ PREDEFINITA**</dt> <dt>(TS \_ DEFAULT \_ SELECTION)</dt> </dl> | Usare la selezione predefinita. Usato da [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)e [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**TF \_ TESTO \_ INCL \_ GTP**</dt> <dt>( 0x1 )</dt> </dl>                               | Specifica che il [metodo ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) otterrà la raccolta di oggetti intervallo che coprono il testo modificato durante la sessione di modifica.<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**TF \_ OGGETTO \_ HF**</dt> <dt>( 1 )</dt> </dl>                                              | Lo spostamento dell'intervallo si interrompe se viene rilevato un oggetto incorporato. Usato nel **membro dwFlags** della [struttura \_ TF HALTCOND.](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**TF \_ CORREZIONE \_ IE**</dt> <dt>( 1 )</dt> </dl>                                  | Il testo è una trasformazione (correzione) del contenuto esistente, in modo che altri servizi di testo possano mantenere i dati associati al testo originale. Usato nel *parametro dwFlags* di [ITfRange::InsertEmbedded.](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**TF \_ COOKIE \_ NON VALIDO**</dt> ( 0xffffffff <dt>)</dt> </dl>                      | Non usato.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**TF \_ COOKIE \_ DI \_ MODIFICA NON**</dt> VALIDO ( <dt>0 )</dt> </dl>               | Non usato.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**TF \_ POPF \_ ALL**</dt> <dt>( 0x1 )</dt> </dl>                                               | Tutti i contesti vengono rimossi dallo stack. Usato nel *parametro dwFlags* di [ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**TF \_ ST \_ CORRECTION**</dt> <dt>( 1 )</dt> </dl>                                  | Il testo è una trasformazione (correzione) del contenuto esistente, in modo che altri servizi di testo possano mantenere i dati associati al testo originale. Usato nel *parametro dwFlags* di [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**TF \_ TU \_ CORRECTION**</dt> <dt>( 0x1 )</dt> </dl>                                | La modifica del testo è il risultato di una trasformazione (correzione) del contenuto esistente. Ciò implica che la semantica del testo non è stata modificata. Usato nel *parametro dwFlags* di [ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**TF \_ US \_ HIDETIPUI**</dt> <dt>0x00000001</dt> </dl>                                | Non usato.<br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 






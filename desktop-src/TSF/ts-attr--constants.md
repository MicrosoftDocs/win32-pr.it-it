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
# <a name="ts_attr_-constants"></a>\_Costanti attr \_ di Servizi terminal \*

\_ \_ \* Per ottenere e modificare i valori degli attributi del documento vengono usate le costanti attr di Servizi terminal. Queste costanti formano i possibili valori dei flag bit nei metodi [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .



| Costante/valore                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <dt>**Servizi terminal \_ ATTR \_ trova \_ indietro**</dt> <dt>(0x1)</dt> </dl>        | Eseguire una ricerca all'indietro dal carattere iniziale o dalla posizione di ancoraggio per la posizione in cui si verifica una transizione in un valore di attributo documento. Il valore predefinito è ricerca in futuro.<br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <dt>**Servizi terminal \_ \_ \_ \_ Offset ricerca attr**</dt> <dt>(0x2)</dt> </dl> | Restituisce il numero di caratteri tra il carattere iniziale o la posizione di ancoraggio (**acpStart** in [ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) o **PaStart** in [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) e la posizione in cui si verifica la transizione di un attributo.<br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <dt>**Servizi terminal \_ ATTR \_ Find \_ updatestart**</dt> <dt>(0x4)</dt> </dl>  | Usato da [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) per posizionare l'ancoraggio di input alla successiva transizione dell'attributo, se ne viene trovata una. In caso contrario, l'ancoraggio di input non viene modificato.<br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <dt>**Servizi terminal \_ \_ \_ \_ Valore di Find want per attr**</dt> <dt>(0x8)</dt> </dl>    | Caricare i valori dell'attributo Document supportati nella struttura [ \_ ATTRVAL di Servizi terminal](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .<br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <dt>**Servizi terminal \_ ATTR \_ Find \_ want \_ end**</dt> <dt>(0x10)</dt> </dl>         | Usato da [ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) e [ITextStoreAnchor:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) per ottenere i valori dell'attributo del documento che terminano con il carattere o la posizione di ancoraggio specificata.<br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <dt>**Servizi terminal \_ ATTR \_ Find \_ Hidden**</dt> <dt>(0x20)</dt> </dl>                | Riservato.<br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ATTRID di Servizi terminal \_](ts-attrid.md)
</dt> <dt>

[ATTRVAL di Servizi terminal \_](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 






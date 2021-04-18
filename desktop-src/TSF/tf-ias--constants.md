---
title: Costanti TF_IAS_ (msctf. h)
description: Le \_ costanti TF IAS \_ \ vengono usate come flag bit nei metodi che inseriscono testo o oggetti incorporati a una selezione o a un punto di inserimento.
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301568"
---
# <a name="tf_ias_-constants"></a>\_Costanti IAS \_ \* TF

Le \_ costanti TF IAS \_ \* vengono usate come flag bit nei metodi che inseriscono testo o oggetti incorporati in una selezione o in un punto di inserimento.



| Costante/valore                                                                                                                                                                                                                                                                       | Descrizione                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <dt>**Tf \_ IAS \_ noquery**</dt> <dt>(0x1)</dt> </dl>                                                       | Il testo viene inserito e il puntatore di intervallo è impostato su **null** all'uscita. Non può essere combinato con il \_ flag QUERYONLY di TF IAS \_ .<br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <dt>**Tf \_ IAS \_ QUERYONLY**</dt> <dt>(0x2)</dt> </dl>                                                 | Non eseguire l'istruzione INSERT. Il chiamante richiede l'impostazione del puntatore di intervallo. Non può essere combinato con il \_ \_ flag noquery di TF IAS.<br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <dt>**Tf \_ IAS \_ Nessuna \_ \_ composizione predefinita**</dt> <dt>(0x80000000)</dt> </dl> | TSF non creerà una composizione predefinita se è necessaria una composizione. Il chiamante deve avviare una composizione sull'intervallo.<br/>         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITextStoreACP:: InsertEmbeddedAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[ITextStoreACP:: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[ITextStoreAnchor::InsertEmbeddedAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[ITextStoreAnchor::InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[ITfInsertAtSelection::InsertEmbeddedAtSelection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[ITfInsertAtSelection::InsertTextAtSelection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 






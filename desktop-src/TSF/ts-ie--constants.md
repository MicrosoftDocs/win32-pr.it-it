---
title: Costanti TS_IE_ (Textstor. h)
description: Le \_ costanti IE \_ \ ts \ descrivono come inserire testo che può contenere oggetti incorporati utilizzati da servizi di testo.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119387"
---
# <a name="ts_ie_-constants"></a>\_Costanti di IE di Servizi terminal \_ \*

Le \_ \_ \* costanti di IE TS descrivono come inserire testo che può contenere oggetti incorporati utilizzati da servizi di testo.



| Costante/valore                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <dt>**Servizi terminal \_ \_Correzione di IE**</dt> <dt>(0x1)</dt> </dl>    | Il testo è una trasformazione (correzione) del contenuto esistente e vengono mantenute le informazioni di markup di testo (metadati) speciali, ad esempio i dati del file WAV o un identificatore di lingua.<br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <dt>**Servizi terminal \_ \_Composizione IE**</dt> <dt>(0x2)</dt> </dl> | Non usato.<br/>                                                                                                                                                                  |



## <a name="remarks"></a>Commenti

Queste costanti vengono usate nel parametro *dwFlags* di [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) e [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).

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

[ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 






---
title: Costanti TF_ES_ (msctf. h)
description: Di seguito sono riportate le costanti utilizzate dal metodo RequestEditSession di ITfContext.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302234"
---
# <a name="tf_es_-constants"></a>\_Costanti TF es \_ \*

Di seguito sono riportate le costanti usate dal metodo [ITfContext:: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .



| Costante/valore                                                                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <dt>**Tf \_ ES \_ ASYNCDONTCARE**</dt> <dt>(0)</dt> </dl> | La sessione di modifica può essere eseguita in modalità sincrona o asincrona, a discrezione del responsabile. Il responsabile tenterà di pianificare una sessione di modifica sincrona per migliorare le prestazioni. Questo valore non può essere combinato con i \_ valori di sincronizzazione TF es \_ Async o TF \_ es \_ .<br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <dt>**Tf \_ \_Sincronizzazione es**</dt> <dt>(0x1)</dt> </dl>                          | La sessione di modifica deve essere sincrona o la richiesta avrà esito negativo (con TF \_ E \_ sincrono). Questo flag deve essere usato solo in situazioni documentate, ad esempio la gestione delle sequenze di tasti, in cui può essere previsto che abbia esito positivo. In caso contrario, la chiamata avrà probabilmente esito negativo. Questo valore non può essere combinato con i \_ \_ valori asincroni TF es ASYNCDONTCARE o TF \_ es \_ .<br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <dt>**Tf \_ \_Lettura es**</dt> <dt>(0x2)</dt> </dl>                          | Richiede l'accesso in sola lettura al contesto.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <dt>**Tf \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt> </dl>           | Richiede l'accesso in lettura/scrittura al contesto.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <dt>**Tf \_ ES \_ Async**</dt> <dt>(0x8)</dt> </dl>                       | La sessione di modifica deve essere asincrona o la richiesta avrà esito negativo. Questo valore non può essere combinato con i \_ valori della sincronizzazione TF es \_ ASYNCDONTCARE o TF \_ es \_ .<br/>                                                                                                                                                                                         |



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

[ITfContext:: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 






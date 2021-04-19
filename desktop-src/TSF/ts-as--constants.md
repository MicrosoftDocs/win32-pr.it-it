---
title: Costanti TS_AS_ (Textstor. h)
description: I flag seguenti specificano gli eventi che chiamano i metodi AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302233"
---
# <a name="ts_as_-constants"></a>\_Costanti di \_ Servizi terminal \*

I flag seguenti specificano gli eventi che chiamano i metodi **adviseSink** .



| Costante/valore                                                                                                                                                                                                                                                                                                                                         | Descrizione                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <dt>**Servizi terminal \_ COME \_ \_ modifica del testo**</dt> <dt>(0x1)</dt> </dl>                                                                                                               | Il testo viene modificato nel documento.<br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <dt>**Servizi terminal \_ COME \_ \_ modifica SEL**</dt> <dt>(0x2)</dt> </dl>                                                                                                                  | Il testo è selezionato nel documento.<br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <dt>**Servizi terminal \_ COME \_ \_ modifica del layout**</dt> <dt>(0x4)</dt> </dl>                                                                                                         | Il layout del documento è stato modificato.<br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <dt>**Servizi terminal \_ AS \_ attr \_ Change**</dt> <dt>(0x8)</dt> </dl>                                                                                                               | Gli attributi del documento vengono modificati.<br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <dt>**Servizi terminal \_ COME \_ \_ modifica dello stato**</dt> <dt>(0x10)</dt> </dl>                                                                                                        | Lo stato del documento è stato modificato.<br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <dt>**Servizi terminal \_ COME \_ tutti i \_ sink**</dt> <dt>(TS \_ come \_ testo \_ modificano \| TS \_ come \_ SEL \_ modificare \| TS \_ come layout modificare TS come \_ \_ \| \_ \_ attr \_ modificare TS come \| \_ \_ \_ modifica dello stato)</dt> </dl> | Uno dei quattro eventi precedenti si è verificato nel documento.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 






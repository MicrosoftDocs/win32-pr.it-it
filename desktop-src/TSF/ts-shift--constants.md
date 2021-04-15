---
title: Costanti TS_SHIFT_ (Textstor. h)
description: Le \_ costanti di spostamento di Servizi terminal \_ vengono utilizzate dall'interfaccia IAnchor per la manipolazione del testo nascosto e del conteggio dei caratteri.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400642"
---
# <a name="ts_shift_-constants"></a>\_Costanti di spostamento di Servizi terminal \_ \*

Le costanti di spostamento di Servizi terminal \_ \_ \* vengono utilizzate dall'interfaccia **IAnchor** per la manipolazione del testo nascosto e del conteggio dei caratteri.



| Costante/valore                                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <dt>**Servizi terminal \_ Conteggio di spostamento \_ \_ nascosto**</dt> <dt>(0x1)</dt> </dl> | Specifica che l'ancoraggio verrà spostato al limite dell'area successiva, incluso il limite di un'area di testo nascosta. Se non è impostato, l'ancoraggio verrà spostato oltre qualsiasi testo nascosto adiacente fino a quando non viene trovata un'area di testo visibile.<br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <dt>**Servizi terminal \_ MAIUSC \_ ALT \_ nascosto**</dt> <dt>(0x2)</dt> </dl>    | Non usato.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <dt>**Servizi terminal \_ MAIUSC \_ ALT \_ visibile**</dt> <dt>(0x4)</dt> </dl> | Non usato.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <dt>**Servizi terminal \_ \_ \_ Solo conteggio MAIUSC**</dt> <dt>(0x8)</dt> </dl>       | L'ancoraggio non viene spostato.<br/>                                                                                                                                                                                                           |



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

[IAnchor::ShiftRegion](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 






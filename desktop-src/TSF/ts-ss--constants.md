---
title: Costanti TS_SS_ (Textstor. h)
description: Le \_ costanti SS \_ \ ts \, definite prima della fase di esecuzione nella \_ struttura di stato TS, descrivono gli Stati dei documenti statici.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301061"
---
# <a name="ts_ss_-constants"></a>\_Costanti SS \_ di Servizi terminal \*

Le \_ costanti SS di Servizi terminal \_ \* , definite prima della fase di esecuzione nella struttura di [**\_ stato TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , descrivono gli Stati dei documenti statici.



| Costante/valore                                                                                                                                                                                                                                                      | Descrizione                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <dt>**Servizi terminal \_ SS \_ DISJOINTSEL**</dt> <dt>(0x1)</dt> </dl>                             | Il documento supporta selezioni multiple.<br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <dt>**Servizi terminal \_ \_Aree SS**</dt> <dt>(0x2)</dt> </dl>                                         | Il documento può contenere più aree.<br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <dt>**Servizi terminal \_ SS \_ transitorio**</dt> <dt>(0x4)</dt> </dl>                                | Si prevede un breve ciclo di utilizzo del documento.<br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <dt>**Servizi terminal \_ SS \_ NOHIDDENTEXT**</dt> <dt>(0x8)</dt> </dl>                          | Il documento non conterrà mai il testo nascosto.<br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <dt>**Servizi terminal \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(0x10)</dt> </dl> | **A partire da Windows 8:** Il documento supporta la correzione automatica fornita dalla tastiera touch.<br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <dt>**Servizi terminal \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(0x20)</dt> </dl>    | **A partire da Windows 8:** Il documento supporta i suggerimenti di testo forniti dalla tastiera touch.<br/> |



## <a name="remarks"></a>Commenti

Il membro **dwStaticFlags** della struttura **di \_ stato TS** usa queste costanti.

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

[**stato di Servizi terminal \_**](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[**\_stato TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 


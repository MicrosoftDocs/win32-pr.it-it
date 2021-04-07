---
title: Costanti TF_SS_ (msctf. h)
description: Le \_ costanti TF SS \_ \, definite prima della fase di esecuzione nella \_ struttura di stato TF, descrivono gli Stati dei documenti statici.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048468"
---
# <a name="tf_ss_-constants"></a>\_Costanti TF SS \_ \*

Le \_ costanti TF SS \_ \* , definite prima della fase di esecuzione nella struttura di [**\_ stato TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , descrivono gli Stati dei documenti statici.



| Costante/valore                                                                                                                                                                                                                                                                              | Descrizione                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <dt>**Tf \_ SS \_ DISJOINTSEL**</dt> <dt>(TS \_ SS \_ DISJOINTSEL)</dt> </dl>                                     | Il documento supporta selezioni multiple.<br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <dt>**Tf \_ \_aree SS**</dt> <dt>( \_ aree SS \_ di servizi Terminal)</dt> </dl>                                                     | Il documento può contenere più aree.<br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <dt>**Tf \_ SS \_ transitorio**</dt> <dt>(TS \_ SS \_ transitorio)</dt> </dl>                                         | Si prevede un breve ciclo di utilizzo del documento.<br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <dt>**Tf \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(TS \_ SS \_ TKBAUTOCORRECTENABLE)</dt> </dl> | **A partire da Windows 8:** Il documento supporta la correzione automatica fornita dalla tastiera touch.<br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <dt>**Tf \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(TS \_ SS \_ TKBPREDICTIONENABLE)</dt> </dl>     | **A partire da Windows 8:** Il documento supporta i suggerimenti di testo forniti dalla tastiera touch.<br/> |



## <a name="remarks"></a>Commenti

Il membro **dwStaticFlags** della struttura di \_ stato TF usa queste costanti.

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

[**\_stato TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 


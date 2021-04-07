---
title: Messaggio di EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Imposta la procedura estesa di Word break per un controllo Rich Edit.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- Controlli di Windows Message EM_SETWORDBREAKPROCEX
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964050"
---
# <a name="em_setwordbreakprocex-message"></a>\_Messaggio SETWORDBREAKPROCEX em

Imposta la procedura estesa di Word break per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una funzione [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) o **null** per utilizzare la procedura predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce l'indirizzo della precedente procedura di Breaking di Word estesa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EditWordBreakProcEx**](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[**\_GETWORDBREAKPROCEX em**](em-getwordbreakprocex.md)
</dt> </dl>

 

 






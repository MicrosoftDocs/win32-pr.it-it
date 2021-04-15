---
title: Messaggio di EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Ottiene un puntatore alla funzione AutoCorrectProc definita dall'applicazione.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- Controlli di Windows Message EM_GETAUTOCORRECTPROC
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477116"
---
# <a name="em_getautocorrectproc-message"></a>\_Messaggio GETAUTOCORRECTPROC em

Ottiene un puntatore alla funzione [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definita dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore alla funzione [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definita dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**\_CALLAUTOCORRECTPROC em**](em-callautocorrectproc.md)
</dt> <dt>

[**\_SETAUTOCORRECTPROC em**](em-setautocorrectproc.md)
</dt> </dl>

 

 






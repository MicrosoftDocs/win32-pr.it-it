---
title: Messaggio di EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Definisce la procedura di callback di correzione automatica corrente.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- Controlli di Windows Message EM_SETAUTOCORRECTPROC
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478592"
---
# <a name="em_setautocorrectproc-message"></a>\_Messaggio SETAUTOCORRECTPROC em

Definisce la procedura di callback di correzione automatica corrente.


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Funzione di callback [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è zero. Se l'operazione ha esito negativo, il valore restituito è un valore diverso da zero.

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

[**\_GETAUTOCORRECTPROC em**](em-getautocorrectproc.md)
</dt> </dl>

 

 






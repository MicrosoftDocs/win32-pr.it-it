---
title: Messaggio di EM_SETUIANAME (RichEdit. h)
description: Imposta il nome di un controllo Rich Edit per l'automazione interfaccia utente (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- Controlli di Windows Message EM_SETUIANAME
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964386"
---
# <a name="em_setuianame-message"></a>\_Messaggio SETUIANAME em

Imposta il nome di un controllo Rich Edit per l'automazione interfaccia utente (UIA).


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa del nome con terminazione null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE se il nome di UIA è stato impostato correttamente; in caso contrario, FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 






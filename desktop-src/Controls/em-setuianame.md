---
title: EM_SETUIANAME messaggio (Richedit.h)
description: Imposta il nome di un controllo Rich Edit per Automazione interfaccia utente (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- EM_SETUIANAME controlli di Windows messaggio
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
ms.openlocfilehash: 603d59b7bf246ee8ed7987d42399281ac1b0520ef27e206f2f8eeddf8f363d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412326"
---
# <a name="em_setuianame-message"></a>Messaggio \_ EM SETUIANAME

Imposta il nome di un controllo Rich Edit per Automazione interfaccia utente (UIA).


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa del nome con terminazione Null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE se il nome dell'interfaccia utente è impostato correttamente; in caso contrario, FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 






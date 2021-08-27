---
title: EM_GETELLIPSISSTATE messaggio (Richedit.h)
description: Recupera lo stato corrente dei puntini di sospensione.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- EM_GETELLIPSISSTATE controlli di Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aaa02fa5ecfdaa5e9f24a41a28ab696e6f2e76224cff8443fab3aa558d1e5a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049251"
---
# <a name="em_getellipsisstate-message"></a>MESSAGGIO \_ EM GETELLIPSISSTATE

Recupera lo stato corrente dei puntini di sospensione.


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è TRUE se vengono visualizzati i puntini di sospensione e FALSE in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETELLIPSISMODE**](em-getellipsismode.md)
</dt> <dt>

[**EM \_ SETELLIPSISMODE**](em-setellipsismode.md)
</dt> </dl>

 

 






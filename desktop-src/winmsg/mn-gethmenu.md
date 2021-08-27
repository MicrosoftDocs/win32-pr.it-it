---
description: Recupera l'handle di menu per la finestra corrente.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: MN_GETHMENU messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cfc1eb6086f94f64e1a0e152e6f86fe89a0ea0278a6c4cc25a487edb6f93ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089931"
---
# <a name="mn_gethmenu-message"></a>Messaggio \_ GETHMENU MN

Recupera l'handle di menu per la finestra corrente.


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HMENU**

Se ha esito positivo, il valore restituito è **HMENU** per la finestra corrente. Se ha esito negativo, il valore restituito è **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

 





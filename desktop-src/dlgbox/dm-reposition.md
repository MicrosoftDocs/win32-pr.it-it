---
title: Messaggio DM_REPOSITION (winuser. h)
description: Riposiziona una finestra di dialogo di primo livello in modo che rientri nell'area del desktop. Un'applicazione può inviare questo messaggio a una finestra di dialogo dopo il ridimensionamento per garantire che l'intera finestra di dialogo rimanga visibile.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- Finestre di dialogo DM_REPOSITION messaggio
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048719"
---
# <a name="dm_reposition-message"></a>\_Messaggio di riposizionamento DM

Riposiziona una finestra di dialogo di primo livello in modo che rientri nell'area del desktop. Un'applicazione può inviare questo messaggio a una finestra di dialogo dopo il ridimensionamento per garantire che l'intera finestra di dialogo rimanga visibile.


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Questo messaggio non ha alcun effetto se la finestra di dialogo è una finestra figlio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari sulle finestre di dialogo](dialog-boxes.md)
</dt> </dl>

 

 






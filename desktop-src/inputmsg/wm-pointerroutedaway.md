---
title: WM_POINTERROUTEDAWAY messaggio
description: Si verifica nel processo che riceve l'input quando l'input del puntatore viene indirizzato a un altro processo. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- WM_POINTERROUTEDAWAY messaggi di input e notifiche
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d6df21a5464aa44621c2eca760690806237f9e75a79c5f695d3df5b7604a6878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964221"
---
# <a name="wm_pointerroutedaway-message"></a>WM_POINTERROUTEDAWAY messaggio

Si verifica nel processo che riceve l'input quando l'input del puntatore viene indirizzato a un altro processo.

Inviato quando l'input del puntatore passa da un processo a un altro nel contenuto configurato per il concatenamento tra processi ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Questo messaggio viene inviato al processo che attualmente riceve l'input del puntatore.


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

NULL

## <a name="remarks"></a>Commenti

Questo messaggio non viene inviato con un messaggio [**WM_POINTERUP**](wm-pointerup.md) o [**un**](wm-pointercapturechanged.md) WM_POINTERCAPTURECHANGED messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDTO**](wm-pointerroutedto.md)
</dt> </dl>

 


---
title: WM_PASTE messaggio (Winuser.h)
description: Un'applicazione invia un messaggio WM PASTE a un controllo di modifica o a una casella combinata per copiare il contenuto corrente degli Appunti nel controllo di modifica in corrispondenza della posizione corrente \_ del cursore. I dati vengono inseriti solo se gli Appunti contengono dati in formato CF \_ TEXT.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE messaggio Data Exchange
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3cc1815349a2194d5dd7e2a65eb1c9ae77a2947f41361a90e92bae73357f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499121"
---
# <a name="wm_paste-message"></a>Messaggio \_ WM PASTE

Un'applicazione invia un **messaggio \_ WM PASTE** a un controllo di modifica o a una casella combinata per copiare il contenuto corrente degli Appunti nel controllo di modifica in corrispondenza della posizione corrente del cursore. I dati vengono inseriti solo se gli Appunti contengono dati in [**formato CF \_ TEXT.**](standard-clipboard-formats.md)


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando viene inviato a una casella combinata, il **messaggio \_ WM PASTE** viene gestito dal relativo controllo di modifica. Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo [**stile \_ DROPDOWNLIST di CBS.**](../controls/combo-box-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**WM \_ CLEAR**](wm-clear.md)
</dt> <dt>

[**WM \_ COPY**](wm-copy.md)
</dt> <dt>

[**WM \_ CUT**](wm-cut.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 


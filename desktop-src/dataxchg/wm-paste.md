---
title: Messaggio WM_PASTE (winuser. h)
description: Un'applicazione invia un messaggio di inserimento di WM \_ a un controllo di modifica o una casella combinata per copiare il contenuto corrente degli Appunti nel controllo di modifica in corrispondenza della posizione corrente del punto di inserimento. I dati vengono inseriti solo se gli Appunti contengono dati in \_ formato testo CF.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- Scambio di dati del messaggio WM_PASTE
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
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400842"
---
# <a name="wm_paste-message"></a>\_Messaggio incolla WM

Un'applicazione invia un messaggio di **\_ inserimento di WM** a un controllo di modifica o una casella combinata per copiare il contenuto corrente degli Appunti nel controllo di modifica in corrispondenza della posizione corrente del punto di inserimento. I dati vengono inseriti solo se gli Appunti contengono dati in formato [**\_ testo CF**](standard-clipboard-formats.md) .


```C++
#define WM_PASTE                        0x0302
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

Quando viene inviato a una casella combinata, il messaggio di **\_ copia di WM** viene gestito dal controllo di modifica. Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo stile [**\_ DropDownList CBS**](../controls/combo-box-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**chiaro di WM \_**](wm-clear.md)
</dt> <dt>

[**\_copia WM**](wm-copy.md)
</dt> <dt>

[**\_taglia WM**](wm-cut.md)
</dt> <dt>

[**\_annullamento WM**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 


---
title: Messaggio WM_CLEAR (winuser. h)
description: Un'applicazione invia un \_ messaggio Clear WM a un controllo di modifica o a una casella combinata per eliminare (cancellare) la selezione corrente, se presente, dal controllo di modifica.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- Scambio di dati del messaggio WM_CLEAR
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301774"
---
# <a name="wm_clear-message"></a>\_Messaggio Clear WM

Un'applicazione invia un **messaggio \_ Clear WM** a un controllo di modifica o a una casella combinata per eliminare (cancellare) la selezione corrente, se presente, dal controllo di modifica.


```C++
#define WM_CLEAR                        0x0303
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

Per annullare l'operazione di eliminazione del messaggio **WM \_ Clear** , è possibile inviare il controllo di modifica un messaggio di [**\_ annullamento em**](../controls/em-undo.md) .

Per eliminare la selezione corrente e inserire il contenuto eliminato negli Appunti, usare il messaggio [**WM \_ Cut**](wm-cut.md) .

Quando viene inviato a una casella combinata, il messaggio **WM \_ Clear** viene gestito dal relativo controllo di modifica. Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo stile [**\_ DropDownList CBS**](../controls/combo-box-styles.md) .

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

[**\_copia WM**](wm-copy.md)
</dt> <dt>

[**\_taglia WM**](wm-cut.md)
</dt> <dt>

[**\_Incolla WM**](wm-paste.md)
</dt> <dt>

[**\_annullamento WM**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 


---
title: Messaggio WM_COPY (winuser. h)
description: Un'applicazione invia il \_ messaggio di copia WM a una casella combinata o un controllo di modifica per copiare la selezione corrente negli Appunti nel \_ formato di testo CF.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- Scambio di dati del messaggio WM_COPY
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320823"
---
# <a name="wm_copy-message"></a>\_Messaggio copia WM

Un'applicazione invia il messaggio di **\_ copia WM** a una casella combinata o un controllo di modifica per copiare la selezione corrente negli Appunti nel formato di [**\_ testo CF**](standard-clipboard-formats.md) .


```C++
#define WM_COPY                         0x0301
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

Restituisce un valore diverso da zero in caso di esito positivo, altrimenti zero.

## <a name="remarks"></a>Commenti

Quando viene inviato a una casella combinata, il messaggio di **\_ copia WM** viene gestito dal controllo di modifica. Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo stile [**\_ DropDownList CBS**](../controls/combo-box-styles.md) .

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

 


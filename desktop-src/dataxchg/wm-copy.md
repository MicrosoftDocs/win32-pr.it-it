---
title: WM_COPY messaggio (Winuser.h)
description: Un'applicazione invia il messaggio WM COPY a un controllo di modifica o a una casella combinata per copiare la selezione corrente \_ negli Appunti in formato CF \_ TEXT.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY messaggio Data Exchange
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
ms.openlocfilehash: 2d7774b1e2d52cbe21b8636bcaa1c695f9f49b319280ebc89c74fd652533066b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096751"
---
# <a name="wm_copy-message"></a>Messaggio \_ WM COPY

Un'applicazione invia il **messaggio \_ WM COPY** a un controllo di modifica o a una casella combinata per copiare la selezione corrente negli Appunti in formato CF [**\_ TEXT.**](standard-clipboard-formats.md)


```C++
#define WM_COPY                         0x0301
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

Restituisce un valore diverso da zero in caso di esito positivo, altrimenti zero.

## <a name="remarks"></a>Commenti

Quando viene inviato a una casella combinata, il **messaggio \_ WM COPY** viene gestito dal relativo controllo di modifica. Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo [**stile \_ DROPDOWNLIST di CBS.**](../controls/combo-box-styles.md)

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

[**WM \_ CUT**](wm-cut.md)
</dt> <dt>

[**WM \_ PASTE**](wm-paste.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 


---
title: WM_CLEAR messaggio (Winuser.h)
description: Un'applicazione invia un messaggio WM CLEAR a un controllo di modifica o a una casella combinata per eliminare (cancellare) la selezione corrente, se \_ presente, dal controllo di modifica.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- WM_CLEAR messaggio Data Exchange
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
ms.openlocfilehash: c6820a9134f112b51474cd5b73e8545583cb02969b02a1bd1428138ebf1049dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029111"
---
# <a name="wm_clear-message"></a>Messaggio WM \_ CLEAR

Un'applicazione invia un **messaggio WM \_ CLEAR** a un controllo di modifica o a una casella combinata per eliminare (cancellare) la selezione corrente, se presente, dal controllo di modifica.


```C++
#define WM_CLEAR                        0x0303
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

L'eliminazione eseguita dal **messaggio WM \_ CLEAR** può essere annullata inviando al controllo di modifica un [**messaggio EM \_ UNDO.**](../controls/em-undo.md)

Per eliminare la selezione corrente e inserire il contenuto eliminato negli Appunti, usare il [**messaggio WM \_ CUT.**](wm-cut.md)

Quando viene inviato a una casella combinata, il **messaggio WM \_ CLEAR** viene gestito dal relativo controllo di modifica. Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo [**stile \_ DROPDOWNLIST di CBS.**](../controls/combo-box-styles.md)

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

[**WM \_ COPY**](wm-copy.md)
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

 


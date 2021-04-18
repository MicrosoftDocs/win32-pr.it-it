---
title: Messaggio WM_CUT (winuser. h)
description: Un'applicazione invia un \_ messaggio WM Cut a un controllo di modifica o a una casella combinata per eliminare (tagliare) la selezione corrente, se presente, nel controllo di modifica e copiare il testo eliminato negli Appunti nel \_ formato di testo CF.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- Scambio di dati del messaggio WM_CUT
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301494"
---
# <a name="wm_cut-message"></a>\_Messaggio WM Cut

Un'applicazione invia un messaggio **WM \_ Cut** a un controllo di modifica o a una casella combinata per eliminare (tagliare) la selezione corrente, se presente, nel controllo di modifica e copiare il testo eliminato negli Appunti nel formato di [**\_ testo CF**](standard-clipboard-formats.md) .


```C++
#define WM_CUT                          0x0300
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

L'eliminazione eseguita dal messaggio **WM \_ Cut** può essere annullata inviando il controllo di modifica un messaggio di [**\_ annullamento em**](../controls/em-undo.md) .

Per eliminare la selezione corrente senza inserire il testo eliminato negli Appunti, usare il messaggio [**\_ Clear di WM**](wm-clear.md) .

Quando viene inviato a una casella combinata, il messaggio **WM \_ Cut** viene gestito dal controllo di modifica. Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo stile [**\_ DropDownList CBS**](../controls/combo-box-styles.md) .

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

[**\_Incolla WM**](wm-paste.md)
</dt> <dt>

[**\_annullamento WM**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_Annulla**](../controls/em-undo.md)
</dt> </dl>

 


---
title: WM_CUT messaggio (Winuser.h)
description: Un'applicazione invia un messaggio WM CUT a un controllo di modifica o a una casella combinata per eliminare (tagliare) la selezione corrente, se presente, nel controllo di modifica e copiare il testo eliminato negli Appunti in formato \_ CF \_ TEXT.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT messaggio Dati Exchange
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
ms.openlocfilehash: d117e0a942c0d9e24e1a9c40d3d66e605ab8d5cf26bbad0e287e9b03a9b25780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304494"
---
# <a name="wm_cut-message"></a>Messaggio WM \_ CUT

Un'applicazione invia un messaggio **WM \_ CUT** a un controllo di modifica o a una casella combinata per eliminare (tagliare) la selezione corrente, se presente, nel controllo di modifica e copiare il testo eliminato negli Appunti in formato [**CF \_ TEXT.**](standard-clipboard-formats.md)


```C++
#define WM_CUT                          0x0300
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

L'eliminazione eseguita dal **messaggio WM \_ CUT** può essere annullata inviando al controllo di modifica un [**messaggio EM \_ UNDO.**](../controls/em-undo.md)

Per eliminare la selezione corrente senza inserire il testo eliminato negli Appunti, usare il [**messaggio WM \_ CLEAR.**](wm-clear.md)

Quando viene inviato a una casella combinata, il **messaggio WM \_ CUT** viene gestito dal relativo controllo di modifica. Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo [**stile \_ CBS DROPDOWNLIST.**](../controls/combo-box-styles.md)

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

[**COPIA \_ WM**](wm-copy.md)
</dt> <dt>

[**INCOLLA \_ WM**](wm-paste.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**EM \_ UNDO**](../controls/em-undo.md)
</dt> </dl>

 


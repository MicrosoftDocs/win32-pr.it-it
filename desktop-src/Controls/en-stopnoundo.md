---
title: EN_STOPNOUNDO codice di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit che si è verificata un'azione per cui il controllo non è in grado di allocare memoria sufficiente per mantenere lo stato di annullamento. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2bd22161f215e9544db08f845eb144fe94ec083b8a887a3db6fc46220d822d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047391"
---
# <a name="en_stopnoundo-notification-code"></a>Codice di notifica EN \_ STOPNOUNDO

Notifica alla finestra padre di un controllo Rich Edit che si è verificata un'azione per cui il controllo non è in grado di allocare memoria sufficiente per mantenere lo stato di annullamento. Un controllo Rich Edit invia questo codice di notifica sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire zero per continuare **l'operazione di** annullamento.

Restituisce un valore diverso da zero per arrestare **l'operazione di** annullamento.

## <a name="remarks"></a>Commenti

La finestra padre riceverà sempre un [**messaggio WM \_ NOTIFY**](wm-notify.md) per questo evento, non richiede una maschera di notifica inviata con [**EM \_ SETEVENTMASK**](em-seteventmask.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 






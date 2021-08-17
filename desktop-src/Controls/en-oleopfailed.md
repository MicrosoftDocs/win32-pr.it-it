---
title: EN_OLEOPFAILED di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit che un'azione dell'utente su un oggetto Component Object Model (COM) non è riuscita. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0391bfc61ff9350758ac81ff6f54fb1cff61d0dd1ebbcb2b8ef02ada9fe3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436681"
---
# <a name="en_oleopfailed-notification-code"></a>Codice \_ di notifica EN OLEOPFAILED

Notifica alla finestra padre di un controllo Rich Edit che un'azione dell'utente su un oggetto Component Object Model (COM) non è riuscita. Un controllo Rich Edit invia questo codice di notifica sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) che contiene informazioni sull'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica restituisce zero.

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

[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 






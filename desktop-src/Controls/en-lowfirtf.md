---
title: EN_LOWFIRTF di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Microsoft Rich Edit che è stata ricevuta una parola chiave RTF (Rich Text Format) non supportata. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffafccf7fc52506ce72c6591ae9d4b5e3f5ee8855788267fbfae98497165e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576321"
---
# <a name="en_lowfirtf-notification-code"></a>Codice \_ di notifica EN LOWFIRTF

Notifica alla finestra padre di un controllo Microsoft Rich Edit che è stata ricevuta una parola chiave RTF (Rich Text Format) non supportata. Un controllo Rich Edit invia questo codice di notifica sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENLOWFIRTF.**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce un valore.

## <a name="remarks"></a>Commenti

Per ricevere una notifica EN LOWFIRTF, specificare il flag ENM LOWFIRTF nella maschera inviata con il messaggio \_ \_ EM [**\_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 






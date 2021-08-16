---
title: TTN_SHOW codice di notifica (Commctrl.h)
description: Notifica alla finestra proprietaria che sta per essere visualizzato un controllo descrizione comando. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74397223f20668487e78cea15e2e1507026ee65089e5011065b3f177514e899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408813"
---
# <a name="ttn_show-notification-code"></a>Codice di notifica TTN \_ SHOW

Notifica alla finestra proprietaria che sta per essere visualizzato un controllo descrizione comando. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

[Versione 4.70](common-control-versions.md). Per visualizzare la descrizione comando nella posizione predefinita, restituire zero. Per personalizzare la posizione della descrizione comando, riposizionare la finestra della descrizione comando con la [**funzione SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) e restituire **TRUE.**

> [!Note]  
> Per le versioni precedenti alla 4.70, non è presente alcun valore restituito.

 

## <a name="remarks"></a>Commenti

Un rettangolo della finestra della descrizione comando è leggermente più grande del rettangolo di visualizzazione del testo e la relativa origine viene offset verso l'alto e verso sinistra. Se è necessario posizionare in modo accurato il rettangolo di visualizzazione del testo di una descrizione comando, il messaggio [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) converte un rettangolo di visualizzazione del testo nel rettangolo della finestra della descrizione comando corrispondente e viceversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 


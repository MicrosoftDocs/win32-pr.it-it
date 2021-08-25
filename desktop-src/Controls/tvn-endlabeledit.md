---
title: TVN_ENDLABELEDIT di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero la fine della modifica delle etichette per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38be7b9fde4b96f3510cd59683ee9df471cc4d77342fe375d9b1818b8ae7da46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408201"
---
# <a name="tvn_endlabeledit-notification-code"></a>Codice di \_ notifica TVN ENDLABELEDIT

Notifica alla finestra padre di un controllo visualizzazione albero la fine della modifica delle etichette per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) Il **membro** item di questa struttura è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **hItem**, **lParam** e **pszText** contengono informazioni valide sull'elemento modificato. Se la modifica dell'etichetta è stata annullata, il **membro pszText** della **struttura TVITEM** è **NULL.** in caso **contrario, pszText** è l'indirizzo del testo modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il **membro pszText** è diverso da **NULL,** restituisce **TRUE** per impostare l'etichetta dell'elemento sul testo modificato. Restituisce **FALSE** per rifiutare il testo modificato e ripristinare l'etichetta originale.

## <a name="remarks"></a>Commenti

Se il **membro pszText** è **NULL,** il valore restituito viene ignorato.

Se è stato specificato il valore LPSTR TEXTCALLBACK per questo elemento e il membro pszText è diverso da NULL, il gestore TVN ENDLABELEDIT deve copiare il testo da \_   \_ **pszText** nella memoria locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) e **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 






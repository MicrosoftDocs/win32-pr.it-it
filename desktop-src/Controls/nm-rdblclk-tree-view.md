---
title: NM_RDBLCLK (visualizzazione albero) codice di notifica (Commctrl.h)
description: Notifica all'elemento padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- NM_RDBLCLK codice di notifica (visualizzazione albero) Windows controlli
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da45d7ac3363a5dc362ef6d34255531f71ce780075e8106fb9579126298a1e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826071"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a>Codice \_ di notifica NM RDBLCLK (visualizzazione albero)

Notifica all'elemento padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






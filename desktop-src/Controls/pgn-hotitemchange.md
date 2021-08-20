---
title: PGN_HOTITEMCHANGE messaggio (Commctrl.h)
description: Notifica alla finestra padre di un controllo pager che l'elemento con stato attiva (evidenziato) è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- PGN_HOTITEMCHANGE controlli Windows messaggio
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510eeb648ad883d04ccc0baf916223bb5209d110c2237ef3bf618d241c2ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830135"
---
# <a name="pgn_hotitemchange-message"></a>Messaggio \_ HOTITEMCHANGE PGN

Notifica alla finestra padre di un controllo pager che l'elemento con stato attiva (evidenziato) è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire zero per evidenziare l'elemento o un valore diverso da zero per impedire l'evidenziazione.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo codice di notifica, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






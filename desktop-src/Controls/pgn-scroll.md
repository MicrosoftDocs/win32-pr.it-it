---
title: PGN_SCROLL di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo pager che la finestra contenuta sta per essere scorrendo. Questa notifica viene inviata sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 864903c73eeb611d1c748ec6a4d936192a1a27f22d3f37115af8879916286a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830145"
---
# <a name="pgn_scroll-notification-code"></a>PGN SCROLL notification code (Codice di \_ notifica PGN SCROLL)

Notifica alla finestra padre di un controllo pager che la finestra contenuta sta per essere scorrendo. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) che contiene e riceve informazioni sul codice di notifica. Il **membro iDir** di questa struttura indica la direzione dello scorrimento. I **membri iXpos** **e iYpos** contengono la posizione orizzontale e verticale della finestra contenuta prima dello scorrimento. Il **membro iScroll** contiene la quantità delta di scorrimento predefinita. Se si desidera, è possibile modificare questo membro in modo che lo scorrimento sia diverso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






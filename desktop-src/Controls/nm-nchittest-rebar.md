---
title: NM_NCHITTEST di notifica (rebar) (Commctrl.h)
description: 'NM_NCHITTEST codice di notifica (rebar): inviato da un controllo rebar quando il controllo riceve un messaggio \_ WM NCHITTEST. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.'
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST di notifica (rebar) Windows controlli
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5831ca9dbeda35c7757613cae1d31db921aa80f4b749d4c9407339a2531abcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410702"
---
# <a name="nm_nchittest-rebar-notification-code"></a>Codice di notifica NM \_ NCHITTEST (rebar)

Inviato da un controllo rebar quando il controllo riceve un [**messaggio WM \_ NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest) Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni sul codice di notifica. Il **membro dwItemSpec** contiene l'indice della banda su cui si è verificato il messaggio di hit test e il membro **pt** contiene le coordinate del mouse del messaggio di hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire zero per consentire all'oggetto rebar di eseguire l'elaborazione predefinita del messaggio di hit test o restituire uno dei valori HT documentati in \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) per eseguire l'override dell'elaborazione dell'hit test predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 


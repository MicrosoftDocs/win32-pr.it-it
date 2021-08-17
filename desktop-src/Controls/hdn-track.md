---
title: HDN_TRACK di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo intestazione che l'utente sta trascinando un divisore nel controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb32a553c85c8fb1bc8321dae5e85b3e7832cf90e4a6652ad163511ad4420d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435221"
---
# <a name="hdn_track-notification-code"></a>Codice di notifica \_ TRACK HDN

Notifica alla finestra padre di un controllo intestazione che l'utente sta trascinando un divisore nel controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni sul controllo intestazione e sull'elemento di cui viene trascinato il divisore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **FALSE per** continuare a tenere traccia del divisore o TRUE **per** terminare il rilevamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ TRACKW** (Unicode) e **HDN \_ TRACKA** (ANSI)<br/>                       |



 

 






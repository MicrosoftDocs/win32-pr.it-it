---
title: Codice di notifica HDN_TRACK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente sta trascinando un divisore nel controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- Controlli di Windows per il codice di notifica HDN_TRACK
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
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874118"
---
# <a name="hdn_track-notification-code"></a>HDN \_ traccia del codice di notifica

Notifica alla finestra padre di un controllo di intestazione che l'utente sta trascinando un divisore nel controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento il cui divisore viene trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **false** per continuare a tenere traccia del divisore o **true** per terminare la verifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ TRACKW** (Unicode) e **HDN \_ tracka** (ANSI)<br/>                       |



 

 






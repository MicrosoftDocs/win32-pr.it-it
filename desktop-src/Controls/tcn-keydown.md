---
title: Codice di notifica TCN_KEYDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che è stato premuto un tasto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- Controlli di Windows per il codice di notifica TCN_KEYDOWN
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300964"
---
# <a name="tcn_keydown-notification-code"></a>\_Codice di notifica KeyDown TCN

Notifica alla finestra padre di un controllo struttura a schede che è stato premuto un tasto. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






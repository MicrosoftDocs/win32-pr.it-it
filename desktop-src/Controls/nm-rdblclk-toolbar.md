---
title: Codice di notifica NM_RDBLCLK (barra degli strumenti) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- Codice di notifica di NM_RDBLCLK (barra degli strumenti) controlli Windows
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
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478256"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a>\_Codice di notifica RDBLCLK di Nm (barra degli strumenti)

Notifica alla finestra padre di un controllo che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni su questo codice di notifica. Se è stato fatto clic con il mouse su un elemento della barra degli strumenti, il membro **dwItemSpec** contiene l'identificatore dell'elemento e il membro **dwItemData** contiene i dati dell'elemento. Se è stato fatto clic con il mouse su un separatore o su uno spazio vuoto sulla barra degli strumenti, il membro **dwItemSpec** conterrà-1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **false** per consentire al controllo Toolbar di eseguire l'elaborazione predefinita dell'evento o **true** per impedire l'elaborazione dell'evento da parte del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






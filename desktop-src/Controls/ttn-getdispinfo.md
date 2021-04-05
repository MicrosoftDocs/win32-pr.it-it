---
title: Codice di notifica TTN_GETDISPINFO (COMmctrl. h)
description: Inviato da un controllo ToolTip per recuperare le informazioni necessarie per visualizzare una finestra di descrizione comando. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- Controlli di Windows per il codice di notifica TTN_GETDISPINFO
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874109"
---
# <a name="ttn_getdispinfo-notification-code"></a>\_Codice di notifica GETDISPINFO di TTN

Inviato da un controllo ToolTip per recuperare le informazioni necessarie per visualizzare una finestra di descrizione comando. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) che identifica lo strumento che necessita di testo e riceve le informazioni richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

Compilare i membri appropriati della struttura per restituire le informazioni richieste al controllo ToolTip. Se il gestore di messaggi imposta il membro **uFlags** della struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) su ttf \_ di \_ SetItem, il controllo ToolTip archivia le informazioni e non le richiede di nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTN \_ GETDISPINFOW** (Unicode) e **TTN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 






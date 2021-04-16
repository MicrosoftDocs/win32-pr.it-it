---
title: Codice di notifica PSN_WIZFINISH (Prsht. h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante fine in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- Controlli di Windows per il codice di notifica PSN_WIZFINISH
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477891"
---
# <a name="psn_wizfinish-notification-code"></a>\_Codice di notifica WIZFINISH PSN

Notifica a una pagina che l'utente ha fatto clic sul pulsante **fine** in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica. Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà. Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

-   Restituisce **true** per impedire il completamento della procedura guidata.
-   [Versione 5,80.](common-control-versions.md) e versioni successive. Restituisce un handle di finestra per impedire il completamento della procedura guidata. La procedura guidata imposta lo stato attivo su tale finestra. La finestra deve essere di proprietà della pagina della procedura guidata.
-   Restituisce **false** per consentire il completamento della procedura guidata.

## <a name="remarks"></a>Commenti

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il \_ valore MSGRESULT di DWL e la routine della finestra di dialogo deve restituire **true**.

[Versione 5,80.](common-control-versions.md) Se l'applicazione restituisce **true** per impedire che venga completata una procedura guidata, non ha alcun controllo su quale finestra della pagina riceve lo stato attivo. Le applicazioni che devono arrestare una procedura guidata devono in genere eseguire questa operazione restituendo l'handle della finestra nella pagina della procedura guidata che consente di ricevere lo stato attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 


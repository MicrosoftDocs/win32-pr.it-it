---
title: PSN_WIZFINISH di notifica (Prsht.h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante Fine in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH del codice di notifica Windows controlli
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
ms.openlocfilehash: b9a11b018a57126c0882862271fa209fcd507224a46180ebb5fbaed4355fc040
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588181"
---
# <a name="psn_wizfinish-notification-code"></a>Codice di notifica \_ PSN WIZFINISH

Notifica a una pagina che l'utente ha fatto clic sul **pulsante** Fine in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica. Questa struttura contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà. Il **membro lParam** della **struttura PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

-   Restituisce **TRUE per** impedire il completamento della procedura guidata.
-   [Versione 5.80.](common-control-versions.md) e versioni successive. Restituisce un handle di finestra per impedire il completamento della procedura guidata. La procedura guidata imposta lo stato attivo su tale finestra. La finestra deve essere di proprietà della pagina della procedura guidata.
-   Restituisce **FALSE** per consentire il completamento della procedura guidata.

## <a name="remarks"></a>Commenti

Per impostare il valore restituito, la procedura della finestra di dialogo per la pagina deve usare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore MSGRESULT DWL e la routine della finestra di dialogo \_ deve restituire **TRUE.**

[Versione 5.80.](common-control-versions.md) Se l'applicazione **restituisce TRUE** per impedire il completamento di una procedura guidata, non ha alcun controllo sulla finestra della pagina che riceve lo stato attivo. Le applicazioni che devono interrompere il completamento di una procedura guidata devono normalmente eseguire questa operazione restituisce l'handle della finestra nella pagina della procedura guidata che deve ricevere lo stato attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 


---
title: PSN_SETACTIVE codice di notifica (Prsht.h)
description: Notifica a una pagina che sta per essere attivata. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e7b656f5497065378af87408fa87fc16cf9ca2cef3cc710f52a1cd643c2927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409733"
---
# <a name="psn_setactive-notification-code"></a>Codice di notifica \_ PSN SETACTIVE

Notifica a una pagina che sta per essere attivata. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica. Questa struttura contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà. Il **membro lParam** della **struttura PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per accettare l'attivazione o -1 per attivare la pagina successiva  o precedente (a seconda che l'utente ha fatto clic sul pulsante Avanti **o** Indietro). Per impostare l'attivazione su una pagina specifica, restituire l'identificatore di risorsa della pagina.

## <a name="remarks"></a>Commenti

Il codice di notifica \_ PSN SETACTIVE viene inviato prima che la pagina sia visibile. Un'applicazione può usare questo codice di notifica per inizializzare i dati nella pagina.

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando viene inviato il codice di notifica \_ PSN SETACTIVE. Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione di questo codice di notifica. Questa operazione avrà risultati imprevedibili.

 

Per impostare il valore restituito, la routine della finestra di dialogo per la pagina deve usare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore MSGRESULT DWL e la routine della finestra di dialogo deve \_ restituire **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 


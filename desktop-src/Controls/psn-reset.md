---
title: PSN_RESET codice di notifica (Prsht.h)
description: Notifica a una pagina che la finestra delle proprietà sta per essere distrutta. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9f14b037d8757469497e644d870a887e6db36172b171f31b00d5615ff39532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409812"
---
# <a name="psn_reset-notification-code"></a>Codice di notifica \_ PSN RESET

Notifica a una pagina che la finestra delle proprietà sta per essere distrutta. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Tutte le modifiche apportate dopo l'ultimo codice di notifica [PSN \_ APPLY](psn-apply.md) vengono annullate, tranne nel caso di [**PSH \_ AEROWIZARD,**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)che non supporta tale codice di notifica.

Il **membro lParam** della struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) a cui punta *lParam* verrà impostato su **TRUE** se l'utente ha fatto clic sul **pulsante X** nell'angolo superiore destro della finestra delle proprietà. Sarà FALSE **se** l'utente ha fatto clic sul **pulsante** Annulla. La **struttura PSHNOTIFY** contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà.

Un'applicazione può usare questo codice di notifica come opportunità per eseguire operazioni di pulizia.

> [!Note]  
> La finestra delle proprietà è in corso di modifica dell'elenco di pagine quando viene inviato il codice di notifica PSN \_ RESET. Non tentare di aggiungere, rimuovere o inserire pagine durante la gestione di questo codice di notifica. Questa operazione avrà risultati imprevedibili.

 

Non chiamare la funzione [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) durante l'elaborazione di questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 


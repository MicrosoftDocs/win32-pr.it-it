---
title: Codice di notifica PSN_HELP (Prsht. h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante della guida. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- Controlli di Windows per il codice di notifica PSN_HELP
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301936"
---
# <a name="psn_help-notification-code"></a>Codice di notifica della Guida di PSN \_

Notifica a una pagina che l'utente ha fatto clic sul pulsante della guida. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica. Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà. Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve visualizzare le informazioni della Guida per la pagina.

> [!Note]  
> Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 






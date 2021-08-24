---
title: PSN_HELP codice di notifica (Prsht.h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante ? . Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- PSN_HELP codice di notifica Windows controlli
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
ms.openlocfilehash: 9f03dc1e016780494c8c5ca35e62baf2570af04ee77daf21f404d7371e9df168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588201"
---
# <a name="psn_help-notification-code"></a>Codice di notifica \_ PSN HELP

Notifica a una pagina che l'utente ha fatto clic sul pulsante ? . Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) che contiene informazioni sul codice di notifica. Questa struttura contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **hdr**. Il **membro hwndFrom** di questa **struttura NMHDR** contiene l'handle per la finestra delle proprietà. Il **membro lParam** della **struttura PSHNOTIFY** non contiene informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione dovrebbe visualizzare le informazioni della Guida per la pagina.

> [!Note]  
> Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 






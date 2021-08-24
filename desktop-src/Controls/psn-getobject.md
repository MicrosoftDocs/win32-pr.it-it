---
title: PSN_GETOBJECT di notifica (Prsht.h)
description: Inviato da una finestra delle proprietà per richiedere un oggetto destinazione di rilascio quando il cursore passa su uno dei pulsanti del controllo Struttura a schede. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81803a950c7b8eb9a41d31178c8f57d7e4199f802538616d4ced20c5a5cb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798631"
---
# <a name="psn_getobject-notification-code"></a>Codice di notifica \_ PSN GETOBJECT

Inviato da una finestra delle proprietà per richiedere un oggetto destinazione di rilascio quando il cursore passa su uno dei pulsanti del controllo Struttura a schede. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) che, all'ingresso, contiene informazioni sul codice di notifica. Se questo codice di notifica viene elaborato, è necessario inserire le informazioni sull'oggetto in questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che elabora questo codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

Per fornire un oggetto, un'applicazione deve impostare i valori in alcuni membri della [**struttura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) in *lParam*. Il **membro pObject** deve essere impostato su un puntatore a oggetto valido e il membro **hResult** deve essere impostato su un flag di operazione riuscita. Per rispettare gli standard Component Object Model (COM), incrementare sempre il conteggio dei riferimenti dell'oggetto quando si specifica un puntatore a un oggetto.

Se un'applicazione non fornisce un oggetto, deve impostare **pObject** su **NULL** e **hResult** su un flag di errore.

> [!Note]  
> Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ ACROBATWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 






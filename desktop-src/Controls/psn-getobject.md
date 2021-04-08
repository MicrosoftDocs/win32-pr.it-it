---
title: Codice di notifica PSN_GETOBJECT (Prsht. h)
description: Inviato da una finestra delle proprietà per richiedere un oggetto destinazione di rilascio quando il cursore passa su uno dei pulsanti del controllo struttura a schede. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- Controlli di Windows per il codice di notifica PSN_GETOBJECT
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
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048068"
---
# <a name="psn_getobject-notification-code"></a>\_Codice di notifica GetObject PSN

Inviato da una finestra delle proprietà per richiedere un oggetto destinazione di rilascio quando il cursore passa su uno dei pulsanti del controllo struttura a schede. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) che, in ingresso, contiene informazioni sul codice di notifica. Se il codice di notifica viene elaborato, è necessario inserire le informazioni sugli oggetti nella struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'elaborazione dell'applicazione del codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

Per fornire un oggetto, un'applicazione deve impostare i valori in alcuni membri della struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) in *lParam*. Il membro **pObject** deve essere impostato su un puntatore a un oggetto valido e il membro **HRESULT** deve essere impostato su un flag Success. Per rispettare gli standard Component Object Model (COM), incrementare sempre il conteggio dei riferimenti dell'oggetto quando viene fornito un puntatore a un oggetto.

Se un'applicazione non fornisce un oggetto, deve impostare **pObject** su **null** e **HRESULT** su un flag di errore.

> [!Note]  
> Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 






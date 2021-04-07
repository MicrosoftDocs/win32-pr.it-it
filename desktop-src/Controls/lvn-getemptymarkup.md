---
title: Codice di notifica LVN_GETEMPTYMARKUP (COMmctrl. h)
description: Inviato dal controllo visualizzazione elenco alla relativa finestra padre quando il controllo non dispone di elementi. Il \_ codice di notifica GETEMPTYMARKUP di LVN è una richiesta che la finestra padre fornisca il testo di markup. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- Controlli di Windows per il codice di notifica LVN_GETEMPTYMARKUP
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874705"
---
# <a name="lvn_getemptymarkup-notification-code"></a>\_Codice di notifica GETEMPTYMARKUP di LVN

Inviato dal controllo visualizzazione elenco alla relativa finestra padre quando il controllo non dispone di elementi. Il \_ codice di notifica GETEMPTYMARKUP di LVN è una richiesta che la finestra padre fornisca il testo di markup. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Impostare i membri di questa struttura per fornire il testo di markup per il controllo visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per impostare il testo del markup nel controllo visualizzazione elenco oppure **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Il parametro *wParam* contiene l'ID del controllo che invia questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






---
title: MCN_SELECT di notifica (Commctrl.h)
description: Inviato da un controllo calendario mensile quando l'utente effettua una selezione esplicita della data all'interno di un controllo calendario mensile. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71674ebccd9a896a92f701e65c7767866b64edac25208248f4683792b5261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018969"
---
# <a name="mcn_select-notification-code"></a>Codice di notifica \_ MCN SELECT

Inviato da un controllo calendario mensile quando l'utente effettua una selezione esplicita della data all'interno di un controllo calendario mensile. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) che contiene informazioni sull'intervallo di date attualmente selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il **codice di notifica \_ MCN SELECT** è simile a [**MCN \_ SELCHANGE,**](mcn-selchange.md)ma **MCN \_ SELECT** viene inviato solo in risposta alle selezioni esplicite della data di un utente. **MCN \_ SELCHANGE si** applica a qualsiasi modifica della selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






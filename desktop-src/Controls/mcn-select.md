---
title: Codice di notifica MCN_SELECT (COMmctrl. h)
description: Inviato da un controllo di calendario mensile quando l'utente crea una selezione di data esplicita all'interno di un controllo di calendario mensile. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- Controlli di Windows per il codice di notifica MCN_SELECT
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
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047995"
---
# <a name="mcn_select-notification-code"></a>MCN \_ selezionare il codice di notifica

Inviato da un controllo di calendario mensile quando l'utente crea una selezione di data esplicita all'interno di un controllo di calendario mensile. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) che contiene informazioni sull'intervallo di date attualmente selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il codice di notifica **\_ Select di MCN** è simile a [**MCN \_ selChange**](mcn-selchange.md), ma **MCN \_ Select** viene inviato solo in risposta alle selezioni di data esplicite di un utente. **MCN \_ SELCHANGE** si applica a qualsiasi modifica di selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






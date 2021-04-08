---
title: Codice di notifica di NM_CLICK (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 39b5716d-cae7-4dc4-b257-0118f4f432c6
keywords:
- NM_CLICK (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45809a683d06871398e79419ec08729b1edcd2c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743986"
---
# <a name="nm_click-tree-view-notification-code"></a>NM \_ clic (visualizzazione albero) codice di notifica

Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






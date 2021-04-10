---
title: Codice di notifica di NM_RCLICK (intestazione) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b453db51-9c41-4a85-8bc0-72bec10f8646
keywords:
- Codice di notifica di NM_RCLICK (intestazione) controlli Windows
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab91d3e35f4da74657faa2fce0e9a9881577087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964649"
---
# <a name="nm_rclick-header-notification-code"></a>\_Codice di notifica di RCLICK (intestazione) Nm

Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_RCLICK

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per non consentire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






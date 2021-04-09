---
title: Codice di notifica HDN_BEGINTRACK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha iniziato il trascinamento di un divisore nel controllo, ovvero l'utente ha premuto il pulsante sinistro del mouse mentre il cursore si trova su un divisore nel controllo intestazione.
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- Controlli di Windows per il codice di notifica HDN_BEGINTRACK
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121774"
---
# <a name="hdn_begintrack-notification-code"></a>\_Codice di notifica BEGINTRACK di HDN

Notifica alla finestra padre di un controllo di intestazione che l'utente ha iniziato il trascinamento di un divisore nel controllo, ovvero l'utente ha premuto il pulsante sinistro del mouse mentre il cursore si trova su un divisore nel controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni sul controllo intestazione e l'elemento di cui deve essere trascinato il separatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **false** per consentire il rilevamento del divisore o **true** per impedire il rilevamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ BEGINTRACKW** (Unicode) e **HDN \_ BEGINTRACKA** (ANSI)<br/>             |



 

 






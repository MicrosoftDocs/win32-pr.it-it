---
title: Codice di notifica HDN_ENDFILTEREDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che è terminata la modifica di un filtro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d3832875-4cde-4d8a-b3a4-a8dae0742c56
keywords:
- Controlli di Windows per il codice di notifica HDN_ENDFILTEREDIT
topic_type:
- apiref
api_name:
- HDN_ENDFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a557278598600f1bd11ebfbe791691de954a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744010"
---
# <a name="hdn_endfilteredit-notification-code"></a>\_Codice di notifica ENDFILTEREDIT di HDN

Notifica alla finestra padre di un controllo di intestazione che è terminata la modifica di un filtro. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_ENDFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni aggiuntive sul filtro in corso di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






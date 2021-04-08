---
title: Codice di notifica HDN_BEGINFILTEREDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che è iniziata la modifica di un filtro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- Controlli di Windows per il codice di notifica HDN_BEGINFILTEREDIT
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965022"
---
# <a name="hdn_beginfilteredit-notification-code"></a>\_Codice di notifica BEGINFILTEREDIT di HDN

Notifica alla finestra padre di un controllo di intestazione che è iniziata la modifica di un filtro. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_BEGINFILTEREDIT

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



 

 






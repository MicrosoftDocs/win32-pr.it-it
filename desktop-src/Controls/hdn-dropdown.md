---
title: Codice di notifica HDN_DROPDOWN (COMmctrl. h)
description: Inviato da un controllo intestazione al relativo elemento padre quando si fa clic sulla freccia a discesa del controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- Controlli di Windows per il codice di notifica HDN_DROPDOWN
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874717"
---
# <a name="hdn_dropdown-notification-code"></a>\_Codice di notifica a discesa HDN

Inviato da un controllo intestazione al relativo elemento padre quando si fa clic sulla freccia a discesa del controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni sul controllo intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Nell'esempio nella sezione Syntax viene illustrato come il ricevitore di notifiche esegue il cast di **lParam** per recuperare la struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contiene l'ID del controllo che invia questo messaggio.

Questo messaggio viene inviato solo se lo stile HDF \_ SPLITBUTTON è impostato sull'elemento dell'intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






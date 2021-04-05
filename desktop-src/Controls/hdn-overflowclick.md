---
title: Codice di notifica HDN_OVERFLOWCLICK (COMmctrl. h)
description: Inviato da un controllo intestazione al relativo padre quando si fa clic sul pulsante di overflow dell'intestazione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- Controlli di Windows per il codice di notifica HDN_OVERFLOWCLICK
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873898"
---
# <a name="hdn_overflowclick-notification-code"></a>\_Codice di notifica OVERFLOWCLICK di HDN

Inviato da un controllo intestazione al relativo padre quando si fa clic sul pulsante di overflow dell'intestazione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che descrive il codice di notifica. Il processo chiamante è responsabile dell'allocazione di questa struttura, inclusa la struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta. Impostare i membri della struttura **NMHDR** , incluso il membro di *codice* che deve essere impostato su HDN \_ OVERFLOWCLICK.

Impostare il membro **iItem** della struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) sull'indice della prima voce di intestazione che non è visibile e pertanto deve essere visualizzato in un overflow.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore di notifiche esegue il cast di **lParam** per recuperare la struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contiene l'ID del controllo che invia la notifica.

Questo messaggio viene inviato solo quando lo stile di [**\_ overflow HDS**](header-control-styles.md) è impostato sul controllo intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






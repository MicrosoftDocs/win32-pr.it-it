---
title: Codice di notifica HDN_ITEMCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto clic sul controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874350"
---
# <a name="hdn_itemclick-notification-code"></a>\_Codice di notifica ITEMCLICK di HDN

Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto clic sul controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che identifica il controllo intestazione e specifica l'indice dell'elemento dell'intestazione su cui è stato fatto clic e il pulsante del mouse utilizzato per fare clic sull'elemento. Il membro **pItem** è impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un controllo intestazione Invia questo codice di notifica dopo che l'utente rilascia il pulsante sinistro del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ ITEMCLICKW** (Unicode) e **HDN \_ ITEMCLICKA** (ANSI)<br/>               |



 

 






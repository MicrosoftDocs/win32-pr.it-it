---
title: Codice di notifica HDN_ITEMCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che gli attributi di un elemento di intestazione stanno per essere modificati. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMCHANGING
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873377"
---
# <a name="hdn_itemchanging-notification-code"></a>\_Codice di notifica ITEMCHANGING di HDN

Notifica alla finestra padre di un controllo di intestazione che gli attributi di un elemento di intestazione stanno per essere modificati. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento intestazione, inclusi gli attributi che stanno per essere modificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **false** per consentire le modifiche o **true** per impedirne l'esecuzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ ITEMCHANGINGW** (Unicode) e **HDN \_ ITEMCHANGINGA** (ANSI)<br/>         |



 

 






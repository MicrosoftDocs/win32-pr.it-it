---
title: Codice di notifica RBN_SPLITTERDRAG (COMmctrl. h)
description: Inviato da un controllo Rebar quando l'utente trascina una barra di divisione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- Controlli di Windows per il codice di notifica RBN_SPLITTERDRAG
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518268"
---
# <a name="rbn_splitterdrag-notification-code"></a>\_Codice di notifica SPLITTERDRAG di RBN

Inviato da un controllo Rebar quando l'utente trascina una barra di divisione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) contenente informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






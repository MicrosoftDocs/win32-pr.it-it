---
title: RBN_SPLITTERDRAG di notifica (Commctrl.h)
description: Inviato da un controllo Rebar quando l'utente trascina una barra di divisione. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- RBN_SPLITTERDRAG del codice di notifica Windows controlli
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
ms.openlocfilehash: e3de913b5815acbdf8b0a98d8131d0a6f071f157fd5bb78040422b6892d7fe09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984941"
---
# <a name="rbn_splitterdrag-notification-code"></a>Codice di \_ notifica RBN SPLITTERDRAG

Inviato da un controllo Rebar quando l'utente trascina una barra di divisione. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) che contiene informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






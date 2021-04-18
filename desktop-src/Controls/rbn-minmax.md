---
title: Codice di notifica RBN_MINMAX (COMmctrl. h)
description: Inviato da un controllo Rebar prima di massimizzare o ridurre al minimo un gruppo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- Controlli di Windows per il codice di notifica RBN_MINMAX
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301762"
---
# <a name="rbn_minmax-notification-code"></a>\_Codice di notifica MinMax di RBN

Inviato da un controllo Rebar prima di massimizzare o ridurre al minimo un gruppo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
RBN_MINMAX
```



## <a name="parameters"></a>Parametri

Questo codice di notifica non contiene parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire l'esecuzione dell'operazione, ovvero zero per consentire la continuazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






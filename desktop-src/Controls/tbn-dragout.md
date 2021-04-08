---
title: Codice di notifica TBN_DRAGOUT (COMmctrl. h)
description: Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante e quindi sposta il cursore dal pulsante. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- Controlli di Windows per il codice di notifica TBN_DRAGOUT
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048111"
---
# <a name="tbn_dragout-notification-code"></a>Codice di notifica per il \_ trascinamento TBN

Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante e quindi sposta il cursore dal pulsante. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che contiene informazioni su questo codice di notifica. Per questo codice di notifica, sono validi solo i membri **HDR** e **iItem** di questa struttura. Il membro **iItem** della struttura contiene l'identificatore di comando del pulsante trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo codice di notifica consente a un'applicazione di implementare la funzionalità di trascinamento della selezione per i pulsanti della barra degli strumenti. Quando si elabora questo codice di notifica, l'applicazione avvierà l'operazione di trascinamento della selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






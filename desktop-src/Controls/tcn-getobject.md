---
title: Codice di notifica TCN_GETOBJECT (COMmctrl. h)
description: Inviato da un controllo struttura a schede quando dispone dello \_ \_ stile esteso TCS ex REGISTERDROP e un oggetto viene trascinato su un elemento di scheda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- Controlli di Windows per il codice di notifica TCN_GETOBJECT
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300963"
---
# <a name="tcn_getobject-notification-code"></a>TCN \_ codice di notifica GETobject

Inviato da un controllo struttura a schede quando dispone dello stile esteso [**TCS \_ ex \_ REGISTERDROP**](tab-control-extended-styles.md) e un oggetto viene trascinato su un elemento di scheda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) che contiene informazioni sull'elemento di tabulazione su cui l'oggetto è stato trascinato e riceve i dati restituiti dall'applicazione in risposta a questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'elaborazione dell'applicazione del codice di notifica deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






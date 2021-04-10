---
title: Codice di notifica TBN_MAPACCELERATOR (COMmctrl. h)
description: Richiede l'indice del pulsante sulla barra degli strumenti corrispondente al carattere dell'acceleratore specificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- Controlli di Windows per il codice di notifica TBN_MAPACCELERATOR
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963751"
---
# <a name="tbn_mapaccelerator-notification-code"></a>\_Codice di notifica MAPACCELERATOR di TBN

Richiede l'indice del pulsante sulla barra degli strumenti corrispondente al carattere dell'acceleratore specificato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) che contiene il carattere del tasto di scelta rapida e che riceve l'indice del pulsante corrispondente. Il campo **dwItemNext** è-1 se il tasto di scelta rapida non corrisponde a un comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE se **NMCHAR. dwItemNext** è impostato su un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






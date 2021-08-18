---
title: TBN_MAPACCELERATOR di notifica (Commctrl.h)
description: Richiede l'indice del pulsante nella barra degli strumenti corrispondente al carattere di scelta rapida specificato. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR del codice di notifica Windows controlli
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
ms.openlocfilehash: 488c78ff00b75c42f6646e314c75d63445c7400eb9130464b126e75bcf2df942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434191"
---
# <a name="tbn_mapaccelerator-notification-code"></a>Codice di \_ notifica TBN MAPACCELERATOR

Richiede l'indice del pulsante nella barra degli strumenti corrispondente al carattere di scelta rapida specificato. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) che contiene il carattere del tasto di scelta rapida e che riceve l'indice del pulsante corrispondente. Il **campo dwItemNext** è -1 se l'acceleratore non corrisponde a un comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE se **NMCHAR.dwItemNext** è impostato su un valore .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






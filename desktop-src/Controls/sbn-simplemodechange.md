---
title: Codice di notifica SBN_SIMPLEMODECHANGE (COMmctrl. h)
description: Inviato da un controllo barra di stato quando la modalità semplice cambia a causa di un \_ messaggio semplice SB. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- Controlli di Windows per il codice di notifica SBN_SIMPLEMODECHANGE
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302127"
---
# <a name="sbn_simplemodechange-notification-code"></a>\_Codice di notifica SIMPLEMODECHANGE di SBN

Inviato da un controllo barra di stato quando la modalità semplice cambia a causa di un messaggio [**\_ semplice SB**](sb-simple.md) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dalla barra di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






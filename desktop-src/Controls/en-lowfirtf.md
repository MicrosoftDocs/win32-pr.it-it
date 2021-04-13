---
title: Codice di notifica EN_LOWFIRTF (RichEdit. h)
description: Notifica alla finestra padre di un controllo Microsoft Rich Edit che è stata ricevuta una parola chiave RTF (Rich Text Format) non supportata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- Controlli di Windows per il codice di notifica EN_LOWFIRTF
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518663"
---
# <a name="en_lowfirtf-notification-code"></a>\_Codice di notifica en LOWFIRTF

Notifica alla finestra padre di un controllo Microsoft Rich Edit che è stata ricevuta una parola chiave RTF (Rich Text Format) non supportata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Per ricevere una \_ notifica en LOWFIRTF, specificare il \_ flag ENM LOWFIRTF nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**\_notifica WM**](wm-notify.md)
</dt> </dl>

 

 






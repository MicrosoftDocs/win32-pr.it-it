---
title: Codice di notifica EN_OLEOPFAILED (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che un'azione dell'utente su un oggetto Component Object Model (COM) ha avuto esito negativo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- Controlli di Windows per il codice di notifica EN_OLEOPFAILED
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 139c51642c8cb6d5efd369cf6b373068604439b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873901"
---
# <a name="en_oleopfailed-notification-code"></a>\_Codice di notifica en OLEOPFAILED

Notifica alla finestra padre di un controllo Rich Edit che un'azione dell'utente su un oggetto Component Object Model (COM) ha avuto esito negativo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) che contiene informazioni sull'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica restituisce zero.

## <a name="remarks"></a>Commenti

La finestra padre otterrà sempre un messaggio [**di \_ notifica WM**](wm-notify.md) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 






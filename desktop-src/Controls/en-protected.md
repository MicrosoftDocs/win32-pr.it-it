---
title: Codice di notifica EN_PROTECTED (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che l'utente sta eseguendo un'azione che modifica un intervallo di testo protetto. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- Controlli di Windows per il codice di notifica EN_PROTECTED
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476978"
---
# <a name="en_protected-notification-code"></a>\_Codice di notifica protetto da it

Notifica alla finestra padre di un controllo Rich Edit che l'utente sta eseguendo un'azione che modifica un intervallo di testo protetto. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**protetta**](/windows/desktop/api/Richedit/ns-richedit-enprotected) contenente le informazioni sul messaggio che ha attivato il codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire l'operazione.

Restituisce un valore diverso da zero per impedire l'operazione.

## <a name="remarks"></a>Commenti

Se viene restituito zero e i membri **msg**, **wParam** e **lParam** della struttura [**protetta**](/windows/desktop/api/Richedit/ns-richedit-enprotected) vengono modificati, il controllo elabora il messaggio modificato anziché il messaggio originale.

Per ricevere \_ i codici di notifica protetti it, specificare [**ENM \_ protected**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

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

[**PROTETTO**](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[**\_notifica WM**](wm-notify.md)
</dt> </dl>

 

 






---
title: Codice di notifica EN_CORRECTTEXT (RichEdit. h)
description: Notifica a una finestra padre di un controllo Rich Edit che \_ si è verificato un gesto Syv corretto, assegnando alla finestra padre la possibilità di annullare la correzione del testo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- Controlli di Windows per il codice di notifica EN_CORRECTTEXT
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119087"
---
# <a name="en_correcttext-notification-code"></a>\_Codice di notifica en CORRECTTEXT

Notifica a una finestra padre di un controllo Rich Edit che \_ si è verificato un gesto Syv corretto, assegnando alla finestra padre la possibilità di annullare la correzione del testo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) che specifica la selezione da correggere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per ignorare l'azione.

Restituisce un valore diverso da zero per elaborare l'azione.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo se sono disponibili funzionalità di penna.

Per ricevere \_ i codici di notifica en CORRECTTEXT, specificare [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

> [!Note]  
> Il \_ codice di notifica en CORRECTTEXT è supportato solo in Rich Edit version 1,0. Non è supportata nelle versioni successive di Rich Edit. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

 

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

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 






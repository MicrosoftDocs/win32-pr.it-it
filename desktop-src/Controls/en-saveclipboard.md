---
title: Codice di notifica EN_SAVECLIPBOARD (RichEdit. h)
description: Notifica alla finestra padre del controllo Rich Edit che il controllo viene chiuso e gli Appunti contengono informazioni. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- Controlli di Windows per il codice di notifica EN_SAVECLIPBOARD
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873665"
---
# <a name="en_saveclipboard-notification-code"></a>\_Codice di notifica en SAVECLIPBOARD

Notifica alla finestra padre del controllo Rich Edit che il controllo viene chiuso e gli Appunti contengono informazioni. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) che contiene informazioni sulle informazioni sugli Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se gli Appunti devono essere resi disponibili ad altre applicazioni.

Restituisce un valore diverso da zero se gli Appunti non devono essere salvati.

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

[**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 






---
title: Codice di notifica EN_ENDCOMPOSITION (RichEdit. h)
description: Notifica a una finestra padre del controllo Rich Edit che l'utente ha immesso nuovi dati o ha terminato l'immissione dei dati durante l'uso di IME o del Framework dei servizi di testo.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- Controlli di Windows per il codice di notifica EN_ENDCOMPOSITION
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475389"
---
# <a name="en_endcomposition-notification-code"></a>\_Codice di notifica en ENDCOMPOSITION

Notifica a una finestra padre del controllo Rich Edit che l'utente ha immesso nuovi dati o ha terminato l'immissione dei dati durante l'uso di IME o del [Framework dei servizi di testo](/windows/desktop/TSF/text-services-framework).


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) che riceve informazioni sulla condizione di composizione finale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 


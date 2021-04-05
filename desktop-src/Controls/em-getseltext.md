---
title: Messaggio di EM_GETSELTEXT (RichEdit. h)
description: Recupera il testo attualmente selezionato in un controllo Rich Edit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- Controlli di Windows Message EM_GETSELTEXT
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873714"
---
# <a name="em_getseltext-message"></a>\_Messaggio GETSELTEXT em

Recupera il testo attualmente selezionato in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che riceve il testo selezionato. L'applicazione chiamante deve garantire che il buffer sia sufficientemente grande da poter essere in possesso del testo selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il numero di caratteri copiati, escluso il carattere null di terminazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 






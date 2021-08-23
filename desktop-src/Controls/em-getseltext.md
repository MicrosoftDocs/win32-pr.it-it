---
title: EM_GETSELTEXT messaggio (Richedit.h)
description: Recupera il testo attualmente selezionato in un controllo Rich Edit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT dei messaggi Windows controlli
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
ms.openlocfilehash: 540567f1b52c936ad085acac8e0374fdb0a912bae06480632263f9676f2948e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019499"
---
# <a name="em_getseltext-message"></a>Messaggio \_ GETSELTEXT EM

Recupera il testo attualmente selezionato in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che riceve il testo selezionato. L'applicazione chiamante deve assicurarsi che il buffer sia sufficientemente grande da contenere il testo selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il numero di caratteri copiati, senza includere il carattere Null di terminazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 






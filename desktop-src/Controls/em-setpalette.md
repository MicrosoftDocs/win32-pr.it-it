---
title: EM_SETPALETTE messaggio (Richedit.h)
description: Modifica il riquadro utilizzato da un controllo Rich Edit per la relativa finestra di visualizzazione.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- EM_SETPALETTE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93225a7a550f86bb8b32bf5939a8c7b7aa862ac96c8459bd6bcceb4c6b76e516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831152"
---
# <a name="em_setpalette-message"></a>Messaggio \_ EM SETPALETTE

Modifica il riquadro utilizzato da un controllo Rich Edit per la relativa finestra di visualizzazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il nuovo riquadro utilizzato dal controllo Rich Edit.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il controllo Rich Edit non controlla se il nuovo riquadro è valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 






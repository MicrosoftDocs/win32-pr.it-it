---
title: EM_SHOWSCROLLBAR messaggio (Richedit.h)
description: Mostra o nasconde una delle barre di scorrimento nella finestra host di un controllo Rich Edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3988ced825fed457549fc9f662a418295de7df6085f04c3e71255ca4ad54c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831142"
---
# <a name="em_showscrollbar-message"></a>Messaggio EM \_ SHOWSCROLLBAR

Mostra o nasconde una delle barre di scorrimento nella finestra host di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identifica la barra di scorrimento da visualizzare: orizzontale o verticale. Questo parametro deve essere **SB \_ VERT** o **SB \_ HORZ.**

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica se visualizzare o nascondere la barra di scorrimento. Specificare **TRUE** per visualizzare la barra di scorrimento e **FALSE** per nasconderla.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo è valido solo quando il controllo è attivo sul posto. Le chiamate effettuate mentre il controllo è inattivo potrebbero non riuscire.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

 






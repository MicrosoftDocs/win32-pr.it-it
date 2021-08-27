---
title: EM_GETFIRSTVISIBLELINE messaggio (Winuser.h)
description: Ottiene l'indice in base zero della riga visibile più in alto in un controllo di modifica su più righe. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11eb93c1c7dcce7f502945df4e063b22c29514bc79fe7310875e9de055e1d745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049211"
---
# <a name="em_getfirstvisibleline-message"></a>Messaggio \_ EM GETFIRSTVISIBLELINE

Ottiene l'indice in base zero della riga visibile più in alto in un controllo di modifica su più righe. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero della riga visibile più in alto in un controllo di modifica su più righe.

**Controlli di modifica:** Per i controlli di modifica a riga singola, il valore restituito è l'indice in base zero del primo carattere visibile.

**Controlli Rich Edit:** Per i controlli Rich Edit a riga singola, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Il numero di righe e la lunghezza delle righe in un controllo di modifica dipendono dalla larghezza del controllo e dall'impostazione wordwrap corrente.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

 






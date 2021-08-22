---
title: EM_GETTEXTLENGTHEX messaggio (Richedit.h)
description: Calcola la lunghezza del testo in vari modi. Viene in genere chiamato prima di creare un buffer per ricevere il testo dal controllo .
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6cf0a094edc2288dbeae6f735e8c10fb72f943f99f9a41b15fc1ef3136168d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540940"
---
# <a name="em_gettextlengthex-message"></a>Messaggio \_ EM GETTEXTLENGTHEX

Calcola la lunghezza del testo in vari modi. Viene in genere chiamato prima di creare un buffer per ricevere il testo dal controllo .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a [**una struttura GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) che riceve le informazioni sulla lunghezza del testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il messaggio restituisce il numero **di TCHAR** nel controllo di modifica, a seconda dell'impostazione dei flag nella [**struttura GETTEXTLENGTHEX.**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) Se nel membro flags  sono stati impostati flag incompatibili, il messaggio restituisce E \_ INVALIDARG .

## <a name="remarks"></a>Commenti

Questo messaggio è un modo rapido e semplice per determinare il numero di caratteri nella versione Unicode del controllo Rich Edit. Tuttavia, per una tabella codici di destinazione non Unicode è potenzialmente possibile eseguire la conversione in una combinazione di caratteri a byte singolo e a byte doppio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 






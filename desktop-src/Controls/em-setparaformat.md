---
title: EM_SETPARAFORMAT messaggio (Richedit.h)
description: Imposta la formattazione del paragrafo per la selezione corrente in un controllo Rich Edit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- EM_SETPARAFORMAT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db0ba4e4bf505c5fb1b746b84cae71dcc621635a0a33b4a533ce8551486fe6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062911"
---
# <a name="em_setparaformat-message"></a>Messaggio \_ EM SETPARAFORMAT

Imposta la formattazione del paragrafo per la selezione corrente in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) che specifica i nuovi attributi di formattazione del paragrafo. Vengono modificati solo gli attributi specificati dal membro **dwMask.**

Microsoft Rich Edit 2.0 e versioni successive: questo parametro può essere un puntatore a una struttura [**PARAFORMAT2,**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) che è un'estensione della [**struttura PARAFORMAT.**](/windows/desktop/api/Richedit/ns-richedit-paraformat) Prima di **inviare il messaggio EM \_ SETPARAFORMAT,** impostare il membro **cbSize** della struttura per indicare la versione della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione non riesce, il valore restituito è zero.

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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 






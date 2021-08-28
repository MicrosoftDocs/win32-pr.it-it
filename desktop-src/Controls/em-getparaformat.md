---
title: EM_GETPARAFORMAT messaggio (Richedit.h)
description: Recupera la formattazione del paragrafo della selezione corrente in un controllo Rich Edit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eda99d1fefc0e2a13cc989726c86588103b7f94d7042b98393709cf4a2cd5f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048851"
---
# <a name="em_getparaformat-message"></a>Messaggio \_ EM GETPARAFORMAT

Recupera la formattazione del paragrafo della selezione corrente in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) che riceve gli attributi di formattazione del paragrafo della selezione corrente.

Se è selezionato più di un paragrafo, la struttura riceve gli attributi del primo paragrafo e il membro **dwMask** specifica quali attributi sono coerenti per l'intera selezione.

Microsoft Rich Edit 2.0 e versioni successive: questo parametro può essere un puntatore a una struttura [**PARAFORMAT2,**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) che è un'estensione della [**struttura PARAFORMAT.**](/windows/desktop/api/Richedit/ns-richedit-paraformat) Prima di **inviare il messaggio EM \_ GETPARAFORMAT,** impostare il membro **cbSize** della struttura per indicare la versione della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il valore del **membro dwMask** della [**struttura PARAFORMAT.**](/windows/desktop/api/Richedit/ns-richedit-paraformat)

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

 

 






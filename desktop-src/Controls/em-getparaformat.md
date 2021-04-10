---
title: Messaggio di EM_GETPARAFORMAT (RichEdit. h)
description: Recupera la formattazione del paragrafo della selezione corrente in un controllo Rich Edit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- Controlli di Windows Message EM_GETPARAFORMAT
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
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964757"
---
# <a name="em_getparaformat-message"></a>\_Messaggio GETPARAFORMAT em

Recupera la formattazione del paragrafo della selezione corrente in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PARAformata**](/windows/desktop/api/Richedit/ns-richedit-paraformat) che riceve gli attributi di formattazione del paragrafo della selezione corrente.

Se viene selezionato più di un paragrafo, la struttura riceve gli attributi del primo paragrafo e il membro **dwMask** specifica quali attributi sono coerenti nell'intera selezione.

Microsoft Rich Edit 2,0 e versioni successive: questo parametro può essere un puntatore a una struttura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , che è un'estensione della struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) . Prima di inviare il messaggio **\_ GETPARAFORMAT em** , impostare il membro **cbSize** della struttura per indicare la versione della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il valore del membro **dwMask** della struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .

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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 






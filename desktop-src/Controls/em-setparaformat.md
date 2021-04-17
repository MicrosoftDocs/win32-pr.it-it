---
title: Messaggio di EM_SETPARAFORMAT (RichEdit. h)
description: Imposta la formattazione del paragrafo per la selezione corrente in un controllo Rich Edit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- Controlli di Windows Message EM_SETPARAFORMAT
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
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476337"
---
# <a name="em_setparaformat-message"></a>\_Messaggio SETPARAFORMAT em

Imposta la formattazione del paragrafo per la selezione corrente in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) che specifica i nuovi attributi di formattazione del paragrafo. Vengono modificati solo gli attributi specificati dal membro **dwMask** .

Microsoft Rich Edit 2,0 e versioni successive: questo parametro può essere un puntatore a una struttura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , che è un'estensione della struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) . Prima di inviare il messaggio **\_ SETPARAFORMAT em** , impostare il membro **cbSize** della struttura per indicare la versione della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione ha esito negativo, il valore restituito è zero.

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

 

 






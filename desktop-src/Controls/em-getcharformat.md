---
title: Messaggio di EM_GETCHARFORMAT (RichEdit. h)
description: Determina la formattazione dei caratteri in un controllo Rich Edit.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- Controlli di Windows Message EM_GETCHARFORMAT
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048448"
---
# <a name="em_getcharformat-message"></a>\_Messaggio GETCHARFORMAT em

Determina la formattazione dei caratteri in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'intervallo di testo da cui recuperare la formattazione. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**\_impostazione predefinita SCF**</dt> </dl>       | Formattazione dei caratteri predefinita.<br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**\_selezione SCF**</dt> </dl> | Formattazione dei caratteri della selezione corrente.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) che riceve gli attributi del primo carattere. Il membro **dwMask** specifica quali attributi sono coerenti nell'intera selezione. Se, ad esempio, l'intera selezione è in corsivo o non in corsivo, \_ viene impostato cfm Italic; se la selezione è parzialmente in corsivo e non è in parte, cfm \_ corsivo non è impostato.

Microsoft Rich Edit 2,0 e versioni successive: questo parametro può essere un puntatore a una struttura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , che è un'estensione della struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) . Prima di inviare il messaggio **\_ GETCHARFORMAT em** , impostare il membro **cbSize** della struttura per indicare la versione della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il valore del membro **dwMask** della struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) .

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

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 






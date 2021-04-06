---
title: Messaggio di EM_FINDTEXTW (RichEdit. h)
description: Trova il testo Unicode in un controllo Rich Edit.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- Controlli di Windows Message EM_FINDTEXTW
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742826"
---
# <a name="em_findtextw-message"></a>\_Messaggio FINDTEXTW em

Trova il testo Unicode in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica i parametri dell'operazione di ricerca. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ giù**</dt> </dl>                               | Se impostato, l'operazione esegue la ricerca dalla fine della selezione corrente fino alla fine del documento. Se non impostato, l'operazione esegue la ricerca dalla fine della selezione corrente fino all'inizio del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Per impostazione predefinita, tutti i Alef arabi e ebraici con accenti diversi corrispondono al carattere Alef. Impostare questo flag se si desidera che la ricerca differenzi tra alef con accenti diversi.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Se impostato, l'operazione di ricerca fa distinzione tra maiuscole e minuscole. Se non è impostato, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Per impostazione predefinita, i contrassegni diacritici arabi e ebraici vengono ignorati. Impostare questo flag se si desidera che l'operazione di ricerca consideri segni diacritici.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Per impostazione predefinita, i Kashida arabi e ebraici vengono ignorati. Impostare questo flag se si desidera che l'operazione di ricerca consideri Kashida.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Se impostato, l'operazione cerca solo le parole intere che corrispondono alla stringa di ricerca. Se non impostato, l'operazione Cerca anche frammenti di parola che corrispondono alla stringa di ricerca.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) che contiene informazioni sull'operazione di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza. Se la destinazione non viene trovata, il valore restituito è-1.

## <a name="remarks"></a>Commenti

**Em \_ FINDTEXTW** usa la struttura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) , mentre [**em \_ FINDTEXTEXW**](em-findtextexw.md) usa la struttura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) . La differenza consiste nel fatto che **FINDTEXTEXW** restituisce l'intervallo di testo trovato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_FINDTEXTEXW em**](em-findtextexw.md)
</dt> </dl>

 

 






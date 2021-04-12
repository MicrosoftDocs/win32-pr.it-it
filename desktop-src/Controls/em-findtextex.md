---
title: Messaggio di EM_FINDTEXTEX (RichEdit. h)
description: Trova il testo in un controllo Rich Edit.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- Controlli di Windows Message EM_FINDTEXTEX
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e52f7d51ee7a186a8a9e66f11884d6c2e9bca2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120134"
---
# <a name="em_findtextex-message"></a>\_Messaggio FINDTEXTEX em

Trova il testo in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il comportamento dell'operazione di ricerca. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ giù**</dt> </dl>                               | Microsoft Rich Edit 2,0 e versioni successive: se impostato, la ricerca è diretta da **FINDTEXTEX. CTO Intrac. cpMin**; Se non è impostato, la ricerca è indietro rispetto a **FINDTEXTEX. CTO Intrac. cpMin**. <br/> Microsoft Rich Edit 1,0: il \_ flag fr down viene ignorato. La ricerca è sempre in futuro.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3,0 e versioni successive: se impostato, la ricerca distingue tra l'arabo e l'ebraico alef con accenti diversi. Se non è impostato, tutti i Alef vengono confrontati solo con il carattere Alef. <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Se impostato, l'operazione di ricerca fa distinzione tra maiuscole e minuscole. Se non è impostato, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole. <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3,0 e versioni successive: se impostato, l'operazione di ricerca considera i segni diacritici arabi e ebraici. Se non è impostato, i segni diacritici vengono ignorati. <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3,0 e versioni successive: se impostato, l'operazione di ricerca considera i Kashida arabi ed ebraici. Se non è impostato, Kashida vengono ignorati. <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Se impostato, l'operazione cerca solo le parole intere che corrispondono alla stringa di ricerca. Se non impostato, l'operazione Cerca anche frammenti di parola che corrispondono alla stringa di ricerca.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) che contiene informazioni sull'operazione di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza. Se la destinazione non viene trovata, il valore restituito è-1.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio per trovare stringhe ANSI. Per Unicode, usare [**em \_ FINDTEXTEXW**](em-findtextexw.md).

Il membro **cpMin** di **FINDTEXTEX. CTO Intrac** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale. Quando si esegue la ricerca indietro, **cpMin** deve essere uguale o maggiore di **cpMax**. Quando si esegue la ricerca in futuro, un valore pari a-1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.

Se l'operazione di ricerca trova una corrispondenza, il membro **chrgText** della struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) restituisce l'intervallo di posizioni dei caratteri che contiene il testo corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_FindText em**](em-findtext.md)
</dt> </dl>

 

 






---
title: EM_FINDTEXTEX messaggio (Richedit.h)
description: "EM_FINDTEXTEX messaggio: trova testo all'interno di un controllo Rich Edit."
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX messaggio Controlli Windows
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
ms.openlocfilehash: 2158dabf9ea17d1bd4cac48454bdbb4056765752
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109839"
---
# <a name="em_findtextex-message"></a>Messaggio \_ EM FINDTEXTEX

Trova il testo all'interno di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il comportamento dell'operazione di ricerca. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 e versioni successive: se impostato, la ricerca viene inoltrata da **FINDTEXTEX.chrg.cpMin**; se non è impostata, la ricerca è all'indietro rispetto **a FINDTEXTEX.chrg.cpMin**. <br/> Microsoft Rich Edit 1.0: il flag FR \_ DOWN viene ignorato. La ricerca è sempre in avanti.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3.0 e versioni successive: se impostata, la ricerca distingue tra alefs arabo ed ebraico con accenti diversi. Se non è impostato, tutte le alef vengono abbinate solo dal carattere alef. <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Se impostata, l'operazione di ricerca fa distinzione tra maiuscole e minuscole. Se non è impostata, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole. <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3.0 e versioni successive: se impostato, l'operazione di ricerca considera i segni diacritici arabo ed ebraico. Se non è impostato, i segni diacritici vengono ignorati. <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3.0 e versioni successive: se impostato, l'operazione di ricerca considera le kashida arabo ed ebraico. Se non impostato, i kashida vengono ignorati. <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Se impostata, l'operazione cerca solo parole intere che corrispondono alla stringa di ricerca. Se non è impostata, l'operazione cerca anche frammenti di parole che corrispondono alla stringa di ricerca.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) contenente informazioni sull'operazione di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza. Se la destinazione non viene trovata, il valore restituito è -1.

## <a name="remarks"></a>Commenti

Usare questo messaggio per trovare stringhe ANSI. Per Unicode, usare [**EM \_ FINDTEXTEXW**](em-findtextexw.md).

Il **membro cpMin** di **FINDTEXTEX.chrg** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale. Quando si esegue la ricerca **all'indietro, cpMin** deve essere uguale o maggiore di **cpMax**. Durante la ricerca in avanti, il valore -1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.

Se l'operazione di ricerca trova una corrispondenza, il membro **chrgText** della struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) restituisce l'intervallo di posizioni di caratteri che contiene il testo corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows \[ Vista\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ FINDTEXT**](em-findtext.md)
</dt> </dl>

 

 






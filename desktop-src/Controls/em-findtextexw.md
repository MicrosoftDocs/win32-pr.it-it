---
title: EM_FINDTEXTEXW messaggio (Richedit.h)
description: "EM_FINDTEXTEXW: trova testo Unicode all'interno di un controllo Rich Edit."
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW di windows del messaggio
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5278726ca4d3e4748e96d8095a411bcebd5637ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109809"
---
# <a name="em_findtextexw-message"></a>Messaggio \_ EM FINDTEXTEXW

Trova testo Unicode all'interno di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il comportamento dell'operazione di ricerca. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 e versioni successive: se impostato, la ricerca viene inoltrata da **FINDTEXTEX.chrg.cpMin**; Se non è impostata, la ricerca viene a ritroso da **FINDTEXTEX.chrg.cpMin**. <br/> Microsoft Rich Edit 1.0: il \_ flag FR DOWN viene ignorato. La ricerca è sempre in avanti.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Se impostata, la ricerca distingue tra alefs con accenti diversi. Se non impostato, le alef in arabo ed ebraico con accenti diversi vengono tutte associate al carattere alef. <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Se impostata, l'operazione di ricerca fa distinzione tra maiuscole e minuscole. Se non impostato, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole.<br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Se impostata, l'operazione di ricerca considera i segni diacritici. Se non impostato, i segni diacritici in arabo ed ebraico vengono ignorati. <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Se impostato, l'operazione di ricerca considera i kashida. Se non è impostato, le kashida arabo ed ebraico vengono ignorate. <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Se impostata, l'operazione cerca solo parole intere che corrispondono alla stringa di ricerca. Se non è impostata, l'operazione cerca anche frammenti di parole che corrispondono alla stringa di ricerca.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) contenente informazioni sull'operazione di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza. Se la destinazione non viene trovata, il valore restituito è -1.

## <a name="remarks"></a>Commenti

Usare questo messaggio per trovare stringhe Unicode. Per ANSI; usare [**EM \_ FINDTEXTEX**](em-findtextex.md).

Il **membro cpMin** di **FINDTEXTEX.chrg** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale. Quando si esegue la ricerca **all'indietro, cpMin** deve essere uguale o maggiore di **cpMax**. Durante la ricerca in avanti, il valore -1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.

Se l'operazione di ricerca trova una corrispondenza, il membro **chrgText** della struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) restituisce l'intervallo di posizioni di caratteri che contiene il testo corrispondente.

**EM \_ FINDTEXTEXW** usa la [**struttura FINDTEXTEXW,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) [**mentre EM \_ FINDTEXTW**](em-findtextw.md) usa la [**struttura FINDTEXTW.**](/windows/win32/api/richedit/ns-richedit-findtexta) La differenza è che **EM \_ FINDTEXTEXW** segnala l'intervallo di testo trovato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows \[ Vista\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ FINDTEXTW**](em-findtextw.md)
</dt> </dl>

 

 






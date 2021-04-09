---
title: Messaggio di EM_FINDTEXT (RichEdit. h)
description: Trova il testo in un controllo Rich Edit.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- Controlli di Windows Message EM_FINDTEXT
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964396"
---
# <a name="em_findtext-message"></a>\_Messaggio FindText em

Trova il testo in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specificare i parametri dell'operazione di ricerca. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ giù**</dt> </dl>                               | Microsoft Rich Edit 2,0 e versioni successive: se impostato, la ricerca viene effettuata dalla fine della selezione corrente fino alla fine del documento. Se non è impostato, la ricerca viene effettuata dalla fine della selezione corrente fino all'inizio del documento. <br/> Microsoft Rich Edit 1,0: il \_ flag fr down viene ignorato. La ricerca è sempre dalla fine della selezione corrente fino alla fine del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3,0 e versioni successive: se impostato, la ricerca distingue tra Alef arabi con accenti diversi. Se non è impostato, tutti i Alef vengono confrontati solo con il carattere Alef. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3,0 e versioni successive: se impostato, l'operazione di ricerca considera i segni diacritici arabi e ebraici. Se non è impostato, i segni diacritici vengono ignorati. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3,0 e versioni successive: se impostato, l'operazione di ricerca considera i Kashida Arabi. Se non è impostato, Kashida vengono ignorati. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**FR \_ MATCHWIDTH**</dt> </dl>             | Windows 8: se impostato, le versioni a byte singolo e a byte doppio dello stesso carattere sono considerate non uguali.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Se impostato, l'operazione cerca solo le parole intere che corrispondono alla stringa di ricerca. Se non impostato, l'operazione Cerca anche frammenti di parola che corrispondono alla stringa di ricerca.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) che contiene informazioni sull'operazione di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza. Se la destinazione non viene trovata, il valore restituito è-1.

## <a name="remarks"></a>Commenti

Il membro **cpMin** di **FindText. CTO Intrac** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale. Quando si esegue la ricerca indietro, **cpMin** deve essere uguale o maggiore di **cpMax**. Quando si esegue la ricerca in futuro, un valore pari a-1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 






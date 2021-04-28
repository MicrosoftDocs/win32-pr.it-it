---
title: EM_FINDTEXT messaggio (Richedit.h)
description: "EM_FINDTEXT messaggio: trova il testo all'interno di un controllo Rich Edit."
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT messaggio controlli Windows
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
ms.openlocfilehash: 452d4e2534fb05cbbbf4c02ac4146f2f8914c9bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109849"
---
# <a name="em_findtext-message"></a>Messaggio \_ EM FINDTEXT

Trova il testo all'interno di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specificare i parametri dell'operazione di ricerca. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 e versioni successive: se impostato, la ricerca viene effettuata dalla fine della selezione corrente alla fine del documento. Se non è impostata, la ricerca viene effettuata dalla fine della selezione corrente all'inizio del documento. <br/> Microsoft Rich Edit 1.0: il flag FR \_ DOWN viene ignorato. La ricerca viene sempre effettuata dalla fine della selezione corrente alla fine del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3.0 e versioni successive: se impostata, la ricerca distingue tra alefs arabi con accenti diversi. Se non è impostato, tutte le alef vengono abbinate solo dal carattere alef. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3.0 e versioni successive: se impostato, l'operazione di ricerca considera i segni diacritici arabo ed ebraico. Se non è impostato, i segni diacritici vengono ignorati. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3.0 e versioni successive: se impostato, l'operazione di ricerca considera i kashida arabi. Se non impostato, i kashida vengono ignorati. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**FR \_ MATCHWIDTH**</dt> </dl>             | Windows 8: se impostata, le versioni a byte singolo e a byte doppio dello stesso carattere vengono considerate non uguali.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Se impostata, l'operazione cerca solo parole intere che corrispondono alla stringa di ricerca. Se non impostata, l'operazione cerca anche i frammenti di parole che corrispondono alla stringa di ricerca.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) contenente informazioni sull'operazione di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza. Se la destinazione non viene trovata, il valore restituito è -1.

## <a name="remarks"></a>Commenti

Il **membro cpMin** di **FINDTEXT.chrg** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale. Quando si esegue una ricerca **all'indietro, cpMin** deve essere uguale o maggiore di **cpMax**. Durante la ricerca in avanti, il valore -1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Findtext**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 






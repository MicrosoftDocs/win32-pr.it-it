---
title: EM_SETTABLEPARMS messaggio (Richedit.h)
description: Modifica i parametri delle righe in una tabella.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccb6258f03d76391bf2288331efb3d9ebde4fb903fe907eaa5e9d37e7497a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576351"
---
# <a name="em_settableparms-message"></a>Messaggio \_ EM SETTABLEPARMS

Modifica i parametri delle righe in una tabella.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una [**struttura TABLEROWPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TABLECELLPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo o uno dei codici di errore seguenti.



| Codice restituito                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Non è possibile apportare modifiche. Ciò può verificarsi se il controllo è un controllo di testo normale o a riga singola o se il punto di inserimento si trova all'interno di un oggetto matematico. Si verifica anche se le tabelle sono disabilitate o se il [**messaggio EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) imposta il **valore SES EX \_ \_ NOTABLE.** <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *wParam o* *lParam* è NULL o punta a una struttura non valida. Il **membro cCell** della [**struttura TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere almeno 1 e non superiore a 63. Il **membro cbRow** deve essere uguale `sizeof(TABLEROWPARMS)` a o `sizeof(TABLEROWPARMS)   2*sizeof(long)` . Il secondo valore è la dimensione della struttura **TABLEROWPARMS** di RichEdit 4.1. Il **membro cbCell** di **TABLEROWPARMS** deve essere uguale a `sizeof(TABLECELLPARMS)` . Il punto di inserimento deve essere all'inizio di una tabella o all'interno di una riga della tabella e il numero di celle può cambiare solo di una. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Questo messaggio modifica i parametri del numero di righe specificato dal membro **cRow** della struttura [**TABLEROWPARMS,**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) se la tabella contiene tale numero di righe consecutive. Se **cRow** è minore di 0, il messaggio scorre fino alla fine della tabella. Se il nuovo conteggio delle celle è diverso da quello corrente per +1 o 1, inserisce o elimina la cella in corrispondenza dell'indice specificato dal membro **iCell** di **TABLEROWPARMS.** La riga iniziale della tabella è identificata da una posizione di carattere. Questa posizione viene specificata dai **membri cpStartRow** con valori maggiori o uguali a zero. La posizione deve essere all'interno della riga della tabella, ma non all'interno di una tabella nidificata, a meno che non si desideri modificare i parametri della tabella. Se il **membro cpStartRow** è 1, la posizione del carattere viene specificata dalla selezione corrente. A tale scopo, posizionare la selezione in un punto qualsiasi all'interno della riga della tabella oppure selezionare la riga con l'estremità attiva della selezione alla fine della riga della tabella.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETTABLEPARMS**](em-gettableparms.md)
</dt> </dl>

 

 






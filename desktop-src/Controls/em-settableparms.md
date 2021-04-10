---
title: Messaggio di EM_SETTABLEPARMS (RichEdit. h)
description: Modifica i parametri delle righe in una tabella.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- Controlli di Windows Message EM_SETTABLEPARMS
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
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964051"
---
# <a name="em_settableparms-message"></a>\_Messaggio SETTABLEPARMS em

Modifica i parametri delle righe in una tabella.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o uno dei codici di errore seguenti.



| Codice restituito                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ Non riuscita**</dt> </dl>        | Non è possibile apportare modifiche. Questa situazione può verificarsi se il controllo è un controllo di testo normale o a riga singola o se il punto di inserimento si trova all'interno di un oggetto matematico. Si verifica anche se le tabelle sono disabilitate o se il messaggio [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) imposta il valore **\_ \_ rilevante ses ex** . <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il valore *wParam* o *lParam* è null o punta a una struttura non valida. Il membro **cCell** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere almeno 1 e non superiore a 63. Il membro **cbRow** deve essere uguale a `sizeof(TABLEROWPARMS)` o `sizeof(TABLEROWPARMS)   2*sizeof(long)` . Il secondo valore è la dimensione della struttura **TABLEROWPARMS** richedit 4,1. Il membro **cbCell** di **TABLEROWPARMS** deve essere uguale a `sizeof(TABLECELLPARMS)` . Il punto di inserimento deve trovarsi all'inizio di una tabella o all'interno di una riga di tabella e il numero di celle può essere modificato solo di uno. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria disponibile è insufficiente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Questo messaggio modifica i parametri del numero di righe specificato dal membro **Crow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , se la tabella contiene molte righe consecutive. Se **Crow** è minore di 0, il messaggio scorre fino alla fine della tabella. Se il nuovo numero di celle è diverso dal numero di celle corrente per + 1 o 1, inserisce o Elimina la cella in corrispondenza dell'indice specificato dal membro **iCell** di **TABLEROWPARMS**. La riga della tabella iniziale è identificata da una posizione del carattere. Questa posizione viene specificata dai membri **cpStartRow** con valori maggiori o uguali a zero. La posizione deve essere all'interno della riga della tabella, ma non all'interno di una tabella nidificata, a meno che non si desideri modificare i parametri della tabella. Se il membro **cpStartRow** è 1, la posizione del carattere viene fornita dalla selezione corrente. A questo scopo, posizionare la selezione in un punto qualsiasi all'interno della riga della tabella oppure selezionare la riga con la fine attiva della selezione alla fine della riga della tabella.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETTABLEPARMS em**](em-gettableparms.md)
</dt> </dl>

 

 






---
title: Messaggio di EM_GETTABLEPARMS (RichEdit. h)
description: Recupera i parametri della tabella per una riga della tabella e i parametri della cella per il numero di celle specificato.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- Controlli di Windows Message EM_GETTABLEPARMS
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873710"
---
# <a name="em_gettableparms-message"></a>\_Messaggio GETTABLEPARMS em

Recupera i parametri della tabella per una riga della tabella e i parametri della cella per il numero di celle specificato.


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



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



| Codice restituito                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ Non riuscita**</dt> </dl>        | Non è possibile apportare modifiche. Questa situazione può verificarsi se il controllo è un controllo di testo normale o a riga singola o se il punto di inserimento si trova all'interno di un oggetto matematico. Si verifica anche se le tabelle sono disabilitate se il messaggio [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) imposta il valore **\_ \_ rilevante ses ex** . <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il valore *wParam* o *lParam* è null o punta a una struttura non valida. Il membro **cbRow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere uguale a `sizeof(TABLEROWPARMS)` o sizeof (TABLEROWPARMS) 2 \* sizeof (Long). Il secondo valore è la dimensione della struttura **TABLEROWPARMS** richedit 4,1. Il membro **cbCell** della struttura **TABLEROWPARMS** deve essere uguale a `sizeof(TABLECELLPARMS)` . La posizione del carattere di query deve trovarsi in un delimitatore di riga della tabella. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria disponibile è insufficiente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Questo messaggio ottiene i parametri della tabella per la riga nella posizione del carattere specificata dal membro **cpStartRow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) e il numero di celle specificate dal membro **cCells** della struttura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

La posizione del carattere specificata dal membro **cpStartRow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere all'inizio della riga della tabella o al delimitatore finale della riga della tabella. Se **cpStartRow** è impostato su 1, la posizione del carattere viene fornita dalla selezione corrente. In questo caso, posizionare la selezione alla fine della riga (tra il contrassegno della cella e il delimitatore finale della riga della tabella) oppure selezionare la riga.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTABLEPARMS em**](em-settableparms.md)
</dt> </dl>

 

 






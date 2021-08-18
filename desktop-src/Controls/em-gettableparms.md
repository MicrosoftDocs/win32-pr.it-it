---
title: EM_GETTABLEPARMS messaggio (Richedit.h)
description: Recupera i parametri di tabella per una riga di tabella e i parametri di cella per il numero specificato di celle.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS dei controlli Windows messaggio
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
ms.openlocfilehash: c2ddca96ce29a0f7b7076580b48cfeceecf1f638830b7c77bc9406a39e97de57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545031"
---
# <a name="em_gettableparms-message"></a>Messaggio \_ EM GETTABLEPARMS

Recupera i parametri di tabella per una riga di tabella e i parametri di cella per il numero specificato di celle.


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



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



| Codice restituito                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Non è possibile apportare modifiche. Ciò può verificarsi se il controllo è un controllo di testo normale o a riga singola o se il punto di inserimento si trova all'interno di un oggetto matematico. Si verifica anche se le tabelle sono disabilitate se [**il messaggio EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) imposta il **valore SES EX \_ \_ NOTABLE.** <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *wParam o* *lParam* è NULL o punta a una struttura non valida. Il **membro cbRow** della [**struttura TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere uguale a o `sizeof(TABLEROWPARMS)` sizeof(TABLEROWPARMS) 2 \* sizeof(long). Il secondo valore è la dimensione della struttura **TABLEROWPARMS** di RichEdit 4.1. Il **membro cbCell** della **struttura TABLEROWPARMS** deve essere uguale a `sizeof(TABLECELLPARMS)` . La posizione del carattere di query deve essere in corrispondenza di un delimitatore di riga della tabella. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Questo messaggio ottiene i parametri di tabella per la riga nella posizione del carattere specificata dal membro **cpStartRow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) e il numero di celle specificato dal membro **cCells** della struttura [**TABLECELLPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)

La posizione del carattere specificata dal membro **cpStartRow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere all'inizio della riga della tabella o al delimitatore finale della riga della tabella. Se **cpStartRow è** impostato su 1, la posizione del carattere viene specificata dalla selezione corrente. In questo caso, posizionare la selezione alla fine della riga (tra il segno di cella e il delimitatore finale della riga della tabella) oppure selezionare la riga.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETTABLEPARMS**](em-settableparms.md)
</dt> </dl>

 

 






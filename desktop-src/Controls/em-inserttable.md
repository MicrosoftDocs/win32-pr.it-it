---
title: EM_INSERTTABLE messaggio (Richedit.h)
description: Inserisce una o più righe di tabella identiche con celle vuote.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a015ae2b9a886ddfa24591944f3f70eca8cb192af771c821df9e4a403c837d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413059"
---
# <a name="em_inserttable-message"></a>Messaggio \_ EM INSERTTABLE

Inserisce una o più righe di tabella identiche con celle vuote.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
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

Restituisce S \_ OK se la tabella viene inserita o un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Se il membro **cpStartRow** di [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) è 1, questo messaggio elimina il testo selezionato (se presente) e quindi inserisce righe vuote della tabella con i parametri di riga e cella specificati da *wParam* *e lParam*. Lascia la selezione che punta all'inizio della prima cella nella prima riga. Il client può quindi popolare le celle della tabella puntando la selezione (o un [**oggetto ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) ai vari contrassegni di fine cella e inserendo e formattazione il testo desiderato. Tale testo può includere righe di tabella nidificata. In alternativa, se il **membro cpStartRow** di **TABLEROWPARMS** è uguale o maggiore di 0, le righe della tabella vengono inserite nella posizione del carattere specificata da **cpStartRow**. In questo modo viene modificata la selezione corrente solo se la tabella viene inserita all'interno del testo selezionato.

Una tabella Di Microsoft Rich Edit è costituita da una sequenza di righe di tabella che, a sua volta, sono costituite da sequenze di paragrafi. Una riga di tabella inizia con il paragrafo speciale delimitatore di due caratteri U+FFF9 U+000D e termina con il paragrafo del delimitatore a due caratteri U+FFFB U+000D. Ogni cella viene terminata dal contrassegno di cella U+0007, che viene considerato come un segno di fine paragrafo rigido esattamente come U+000D (CR). I parametri di riga e cella della tabella vengono considerati come formattazione speciale del paragrafo dei delimitatori di riga della tabella. La formattazione contiene le informazioni nella [**struttura TABLEROWPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) I parametri della cella specificati dalla [**struttura TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) vengono archiviati in una versione espansa della matrice tabs. Questo formato consente di annidare le tabelle all'interno di altre tabelle, fino a 15 livelli di profondità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ INSERTIMAGE**](em-insertimage.md)
</dt> </dl>

 

 






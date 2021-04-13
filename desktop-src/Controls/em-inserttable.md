---
title: Messaggio di EM_INSERTTABLE (RichEdit. h)
description: Inserisce una o più righe di tabella identiche con celle vuote.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- Controlli di Windows Message EM_INSERTTABLE
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
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475556"
---
# <a name="em_inserttable-message"></a>\_Messaggio INSERTTABLE em

Inserisce una o più righe di tabella identiche con celle vuote.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
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

Restituisce \_ OK se la tabella viene inserita oppure un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Se il membro **cpStartRow** di [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) è 1, questo messaggio Elimina il testo selezionato, se presente, e quindi inserisce righe della tabella vuote con i parametri di riga e di cella forniti da *wParam* e *lParam*. Lascia la selezione che punta all'inizio della prima cella nella prima riga. Il client può quindi popolare le celle della tabella puntando alla selezione (o a un [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) ai vari contrassegni di fine cella e inserendo e formattando il testo desiderato. Tale testo può includere righe della tabella nidificata. In alternativa, se il membro **cpStartRow** di **TABLEROWPARMS** è maggiore o uguale a 0, le righe della tabella vengono inserite nella posizione del carattere specificata da **cpStartRow**. Questa operazione modifica solo la selezione corrente se la tabella viene inserita all'interno del testo selezionato.

Una tabella Microsoft Rich Edit è costituita da una sequenza di righe di tabella che, a sua volta, è costituita da sequenze di paragrafi. Una riga di tabella inizia con il paragrafo speciale delimitatore di due caratteri U + FFF9 U + d e termina con il paragrafo di delimitatore di due caratteri U + FFFB U + d. Ogni cella viene terminata dal contrassegno di cella U + 0007, che viene considerato come un segno di fine del paragrafo rigido esattamente come U + d (CR). La riga della tabella e i parametri delle celle vengono considerati come formattazione speciale dei delimitatori di riga della tabella. La formattazione contiene le informazioni contenute nella struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) . I parametri della cella forniti dalla struttura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) vengono archiviati in una versione espansa della matrice di schede. Questo formato consente di annidare le tabelle all'interno di altre tabelle, fino a un massimo di quindici livelli di profondità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_INSERTIMAGE em**](em-insertimage.md)
</dt> </dl>

 

 






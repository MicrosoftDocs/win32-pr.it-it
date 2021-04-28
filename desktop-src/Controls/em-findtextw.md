---
title: EM_FINDTEXTW messaggio (Richedit.h)
description: "EM_FINDTEXTW messaggio: trova testo Unicode all'interno di un controllo Rich Edit."
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW messaggio Controlli Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 325ff948c4c8f03e8051248f15928d8e8c56e52f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109799"
---
# <a name="em_findtextw-message"></a>Messaggio \_ EM FINDTEXTW

Trova testo Unicode all'interno di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica i parametri dell'operazione di ricerca. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Se impostata, l'operazione cerca dalla fine della selezione corrente alla fine del documento. Se non è impostata, l'operazione cerca dalla fine della selezione corrente all'inizio del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Per impostazione predefinita, le alef arabo ed ebraico con accenti diversi vengono tutte abbinate dal carattere alef. Impostare questo flag se si vuole che la ricerca distinzioni tra alefs con accenti diversi.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Se impostata, l'operazione di ricerca fa distinzione tra maiuscole e minuscole. Se non è impostata, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Per impostazione predefinita, i segni diacritici arabo ed ebraico vengono ignorati. Impostare questo flag se si vuole che l'operazione di ricerca consideri i segni diacritici.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Per impostazione predefinita, le kashida in arabo ed ebraico vengono ignorate. Impostare questo flag se si vuole che l'operazione di ricerca consideri i kashida.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Se impostata, l'operazione cerca solo parole intere che corrispondono alla stringa di ricerca. Se non impostata, l'operazione cerca anche i frammenti di parole che corrispondono alla stringa di ricerca.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) contenente informazioni sull'operazione di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza. Se la destinazione non viene trovata, il valore restituito è -1.

## <a name="remarks"></a>Commenti

**EM \_ FINDTEXTW** usa la [**struttura FINDTEXTW,**](/windows/win32/api/richedit/ns-richedit-findtexta) mentre [**EM \_ FINDTEXTEXW**](em-findtextexw.md) usa la [**struttura FINDTEXTEXW.**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) La differenza è che **FINDTEXTEXW riporta** l'intervallo di testo trovato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ FINDTEXTEXW**](em-findtextexw.md)
</dt> </dl>

 

 






---
description: Questi caratteri di escape vengono usati con la funzione ImmEscape.
ms.assetid: ede886dc-8a92-428c-8975-3feadc1d4f90
title: Escape IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4764e884a65069d73c535d38d5ee2896b1d2ecaeb66600bd868f8830cddcfc4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107211"
---
# <a name="ime-escapes"></a>Escape IME

Questi caratteri di escape vengono usati con la [**funzione ImmEscape.**](/windows/desktop/api/Imm/nf-imm-immescapea)



| Carattere speciale di escape                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ ESC \_ GET \_ EUDC \_ DICTIONARY  | Recuperare il percorso del file del dizionario EUDC. In input, il *parametro lpData* deve essere il puntatore al buffer per ricevere il percorso. Questo buffer deve essere uguale o maggiore di 80 \* sizeof(TCHAR). In caso di restituzione, il buffer contiene la stringa con terminazione Null che specifica il percorso completo del dizionario. Solo per l'uso da parte dell'editor EUDC cinese; non utilizzare in altre applicazioni.                                                                                  |
| MODALITÀ IME \_ ESC \_ HANJA \_            | Eseguire la conversione da Hangul a Hanja. In input, *lpData* deve puntare al buffer che contiene il carattere Hangul da convertire. nell'output riceve l'hanja convertito come stringa con terminazione Null. Per l'uso da parte dell'editor coreano; non utilizzare in altre applicazioni.                                                                                                                                                                                                           |
| NOME IME \_ \_ IME ESC \_              | Recuperare il nome dell'IME. In input, il *parametro lpData* deve essere il puntatore al buffer per ricevere il nome. In caso di restituzione, il buffer contiene la stringa con terminazione Null che specifica il nome IME. Solo per l'uso da parte dell'editor EUDC cinese; non utilizzare in altre applicazioni. **Windows Me/98/95:** Il buffer non deve essere minore di 16 \* sizeof(TCHAR).<br/> **Windows NT, Windows 2000, Windows XP:** Il buffer non deve contenere meno di 64 caratteri.<br/> |
| TASTO \_ ESC \_ MAX \_ IME               | Il valore restituito della funzione è il numero massimo di key stoke per un carattere EUDC. Solo per l'uso da parte dell'editor EUDC cinese; non utilizzare in altre applicazioni.                                                                                                                                                                                                                                                                                                         |
| SUPPORTO DELLE \_ QUERY ESC \_ \_ IME         | Verificare l'implementazione. In input, *lpData punta* al buffer che contiene il valore di escape IME. La funzione restituisce 0 se l'escape non è implementato.                                                                                                                                                                                                                                                                                                             |
| SEQUENZA ESC IME \_ \_ A \_ \_ INTERNO | Restituisce il codice carattere corrispondente al codice di sequenza specificato. In input, il *parametro lpData* è il puntatore a una variabile a 32 bit che contiene il codice della sequenza. Solo per l'uso da parte dell'editor EUDC cinese; non utilizzare in altre applicazioni. In genere, l'IME cinese codifica i codici carattere di lettura nella sequenza da 1 a n.                                                                                                                               |
| IME \_ ESC \_ SET \_ EUDC \_ DICTIONARY  | Impostare il file del dizionario EUDC. In input, il *parametro lpData* è il puntatore a una stringa con terminazione Null che specifica il percorso completo. Il percorso deve essere minore di 80 \* sizeof(TCHAR). Solo per l'uso da parte dell'editor EUDC cinese; non utilizzare in altre applicazioni.                                                                                                                                                                                                           |
| IME \_ ESC \_ GETHELPFILENAME        | **Windows Me/98, Windows 2000, Windows XP:** Restituisce il nome del file della Guida dell'IME. Al ritorno il *parametro lpData* è il percorso completo del file della Guida dell'IME. Il percorso deve essere minore di 80 \* sizeof(TCHAR).                                                                                                                                                                                                                                                           |



 

Il sistema operativo riserva i caratteri di escape nell'intervallo IME \_ ESC RESERVED FIRST a \_ \_ IME ESC RESERVED LAST \_ per uso \_ \_ personale.

Il sistema operativo riserva i caratteri di escape nell'intervallo IME ESC PRIVATE FIRST a IME ESC PRIVATE LAST per l'uso \_ privato da parte degli \_ \_ \_ \_ \_ IME.

 

 





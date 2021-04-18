---
description: Questi caratteri di escape vengono usati con la funzione ImmEscape.
ms.assetid: ede886dc-8a92-428c-8975-3feadc1d4f90
title: Caratteri di escape IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff93751450ee6eb6957482362cc8bc22f41d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307859"
---
# <a name="ime-escapes"></a>Caratteri di escape IME

Questi caratteri di escape vengono usati con la funzione [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea) .



| Carattere speciale di escape                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ ESC \_ get \_ EUDC \_ Dictionary  | Recuperare il percorso del file del dizionario EUDC. In input il parametro *lpData* deve essere il puntatore al buffer per ricevere il percorso. Questo buffer deve essere maggiore o uguale a 80 \* sizeof (TCHAR). Al ritorno, il buffer contiene la stringa con terminazione null che specifica il percorso completo del dizionario. Per l'uso solo da parte dell'editor EUDC cinese; Non usare in altre applicazioni.                                                                                  |
| \_ \_ modalità Hanja IME \_ ESC            | Conversione da Hangul a Hanja. In fase di input, *lpData* deve puntare al buffer che contiene il carattere Hangul da convertire. nell'output riceve l'oggetto Hanja convertito come stringa con terminazione null. Per l'uso da parte dell'editor coreano; Non usare in altre applicazioni.                                                                                                                                                                                                           |
| \_ \_ nome IME ESC \_ IME              | Recuperare il nome dell'IME. In input il parametro *lpData* deve essere il puntatore al buffer per ricevere il nome. Al ritorno, il buffer contiene la stringa con terminazione null che specifica il nome dell'IME. Per l'uso solo da parte dell'editor EUDC cinese; Non usare in altre applicazioni. **Windows Me/98/95:** Il buffer non può essere inferiore a 16 \* sizeof (TCHAR).<br/> **Windows NT, windows 2000, Windows XP:** Il buffer non può contenere meno di 64 caratteri.<br/> |
| \_ \_ chiave max ESC \_ IME               | Il valore restituito della funzione è il numero massimo di Stokes chiave per un carattere EUDC. Per l'uso solo da parte dell'editor EUDC cinese; Non usare in altre applicazioni.                                                                                                                                                                                                                                                                                                         |
| \_ \_ supporto query IME \_ ESC         | Verificare l'implementazione. In input *lpData* punta al buffer che contiene il valore di escape IME. La funzione restituisce 0 se l'escape non è implementato.                                                                                                                                                                                                                                                                                                             |
| \_sequenza ESC \_ IME \_ nell' \_ interno | Restituisce il codice carattere che corrisponde al codice di sequenza specificato. In input il parametro *lpData* è il puntatore a una variabile a 32 bit che contiene il codice di sequenza. Per l'uso solo da parte dell'editor EUDC cinese; Non usare in altre applicazioni. In genere, l'IME cinese codifica i codici carattere di lettura nella sequenza da 1 a n.                                                                                                                               |
| \_ \_ \_ dizionario EUDC set ESC \_ ESC  | Impostare il file del dizionario EUDC. In input il parametro *lpData* è il puntatore a una stringa con terminazione null che specifica il percorso completo. Il percorso deve essere minore di 80 \* sizeof (TCHAR). Per l'uso solo da parte dell'editor EUDC cinese; Non usare in altre applicazioni.                                                                                                                                                                                                           |
| IME \_ ESC \_ GETHELPFILENAME        | **Windows Me/98, windows 2000, Windows XP:** Restituisce il nome del file della Guida dell'IME. In return il parametro *lpData* è il percorso completo del file della Guida di IME. Il percorso deve essere minore di 80 \* sizeof (TCHAR).                                                                                                                                                                                                                                                           |



 

Il sistema operativo riserva i caratteri di escape nell'intervallo IME \_ ESC \_ riservato \_ per primo ad \_ IME ESC \_ riservato per l' \_ uso personale.

Il sistema operativo riserva il numero di caratteri di escape nell'intervallo IME \_ ESC \_ privato \_ prima ad IME \_ ESC \_ private \_ Last per l'utilizzo privato da parte degli IME.

 

 





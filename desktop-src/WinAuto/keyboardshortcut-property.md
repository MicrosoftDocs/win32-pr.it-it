---
title: Proprietà KeyboardShortcut
description: La proprietà KeyboardShortcut descrive una combinazione di chiave o chiave che attiva un oggetto accessibile specificato.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221457"
---
# <a name="keyboardshortcut-property"></a>Proprietà KeyboardShortcut

La proprietà **KeyboardShortcut** descrive una combinazione di chiave o chiave che attiva un oggetto accessibile specificato.

La proprietà **KeyboardShortcut** viene recuperata chiamando [**IAccessible:: Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).

La stringa recuperata descrive un *tasto di scelta rapida* (detto anche tasto *di scelta rapida) o* un *tasto* di scelta (detto *anche tasto di scelta).* Una chiave di accesso è un carattere sottolineato nel testo di un menu, di una voce di menu o di un'etichetta di un controllo, ad esempio un pulsante di push.

La stringa recuperata deve contenere il nome della chiave insieme al tasto di modifica o alle chiavi. Il formato della stringa deve essere il seguente, in modo che i client possano analizzarlo facilmente: \[ \[ tasto di modifica... \] + \[ \] + \] nome della chiave.

Gli esempi includono ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + MAIUSC + BACKSPACE o semplicemente BACKSPACE.

Nella tabella seguente sono elencati i tasti di modifica.



| Tasto di modifica | Descrizione                        |
|--------------|------------------------------------|
| ALT          | Tasto di modifica alternativo             |
| CTRL         | Tasto di modifica controllo               |
| MAIUSC        | Tasto di modifica MAIUSC                 |
| WIN          | Tasto logo Windows                   |
| FN           | Tasto funzione sui computer portatili |



 

Non localizzare stringhe di tasti di scelta rapida.

## <a name="handling-objects-that-have-both-key-types"></a>Gestione di oggetti con entrambi i tipi di chiave

Se un oggetto ha sia un tasto di scelta rapida che una chiave di accesso, la proprietà **KeyboardShortcut** restituisce il tasto di scelta. La chiave di accesso è quella che un utente preme quando l'oggetto o l'elemento padre dell'oggetto ha lo stato attivo. Ad esempio, la voce di menu **stampa** potrebbe avere sia un tasto di scelta rapida (Ctrl + p) che un tasto di scelta (P). Se un utente preme CTRL + P mentre il menu è attivo, non viene eseguita alcuna operazione. Tuttavia, se un utente preme P mentre il menu è attivo, richiama la finestra di dialogo **stampa** dell'applicazione. In questo caso, la proprietà **KeyboardShortcut** è "P" per riflettere gli elementi che l'utente deve premere quando il menu ha lo stato attivo della tastiera.

 

 





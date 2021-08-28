---
title: Come interagire con la selezione corrente
description: L'utente può selezionare il testo in un controllo Rich Edit usando il mouse o la tastiera.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6e60ef0ba4aa9a8034256c8c272950f4983d16c0195737065563b378e14202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434641"
---
# <a name="how-to-interact-with-the-current-selection"></a>Come interagire con la selezione corrente

L'utente può selezionare il testo in un controllo Rich Edit usando il mouse o la tastiera. La *selezione corrente* è l'intervallo di caratteri selezionati o la posizione del punto di inserimento se non è selezionato alcun carattere. Un'applicazione può ottenere informazioni sulla selezione corrente, impostarla, determinare quando cambia e mostrare o nascondere l'evidenziazione della selezione.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="interact-with-the-current-selection"></a>Interagire con la selezione corrente

Per determinare la selezione corrente in un controllo Rich Edit, usare il [**messaggio \_ EM EXGETSEL.**](em-exgetsel.md) Per impostare la selezione corrente, usare il [**messaggio EM \_ EXSETSEL.**](em-exsetsel.md) La [**struttura CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) viene usata con entrambi i messaggi e specifica un intervallo di caratteri. Per recuperare informazioni sul contenuto della selezione corrente, è possibile usare il [**messaggio EM \_ SELECTIONTYPE.**](em-selectiontype.md)

Un'applicazione può rilevare quando la selezione corrente cambia elaborando il codice di notifica [EN \_ SELCHANGE.](en-selchange.md) Il codice di notifica specifica una [**struttura SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) che contiene informazioni sulla nuova selezione. Un controllo Rich Edit invia questo codice di notifica solo se lo si abilita usando il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md)

Per impostazione predefinita, un controllo Rich Edit mostra e nasconde l'evidenziazione della selezione quando ottiene e perde lo stato attivo. È possibile visualizzare o nascondere l'evidenziazione della selezione in qualsiasi momento usando il [**messaggio EM \_ HIDESELECTION.**](em-hideselection.md) Ad esempio, un'applicazione potrebbe fornire una finestra di dialogo Cerca per trovare testo in un controllo Rich Edit. L'applicazione potrebbe selezionare il testo corrispondente senza chiudere la finestra di dialogo, nel qual caso deve usare il messaggio **EM \_ HIDESELECTION** per evidenziare la selezione.

Come per i controlli di modifica, è possibile specificare lo stile della finestra [**ES \_ NOHIDESEL**](edit-control-styles.md) per impedire a un controllo Rich Edit di nascondere l'evidenziazione della selezione quando perde lo stato attivo.

In alternativa all'uso dei messaggi [**EM \_ EXGETSEL**](em-exgetsel.md) ed [**EM \_ EXSETSEL,**](em-exsetsel.md) è possibile recuperare e impostare la selezione corrente usando i messaggi di controllo di modifica [**EM \_ GETSEL**](em-getsel.md) ed [**EM \_ SETSEL.**](em-setsel.md) Il **messaggio EM \_ GETSEL** contiene due indici di caratteri a 16 bit nel relativo valore restituito a 32 bit e pertanto funziona solo per le selezioni che rientrano interamente nei primi 64 KB. Tuttavia, un controllo Rich Edit non conterrà mai più di 32.000 caratteri di testo, a meno che non si estenda questo limite usando il messaggio [**EM \_ LIMITTEXT**](em-limittext.md) o [**EM \_ EXLIMITTEXT.**](em-exlimittext.md) Per le selezioni che si estendono oltre i primi 64 KB di testo, il **messaggio EM \_ GETSEL** restituisce –1. In tal caso è comunque possibile usare i valori restituiti in *wParam* e *lParam* per trovare i caratteri iniziale e finale della selezione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





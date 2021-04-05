---
title: Come interagire con la selezione corrente
description: L'utente può selezionare il testo in un controllo Rich Edit utilizzando il mouse o la tastiera.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724282"
---
# <a name="how-to-interact-with-the-current-selection"></a>Come interagire con la selezione corrente

L'utente può selezionare il testo in un controllo Rich Edit utilizzando il mouse o la tastiera. La *selezione corrente* è l'intervallo di caratteri selezionati o la posizione del punto di inserimento se non è selezionato alcun carattere. Un'applicazione può ottenere informazioni sulla selezione corrente, impostarla, determinare quando viene modificata e mostrare o nascondere l'evidenziazione della selezione.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="interact-with-the-current-selection"></a>Interagire con la selezione corrente

Per determinare la selezione corrente in un controllo Rich Edit, usare il [**messaggio \_ EXGETSEL em**](em-exgetsel.md) . Per impostare la selezione corrente, utilizzare il [**messaggio \_ EXSETSEL em**](em-exsetsel.md) . La struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) viene utilizzata con entrambi i messaggi e specifica un intervallo di caratteri. Per recuperare informazioni sul contenuto della selezione corrente, è possibile usare il messaggio [**\_ SELECTIONTYPE em**](em-selectiontype.md) .

Un'applicazione può rilevare quando la selezione corrente viene modificata elaborando il codice di notifica [en \_ selChange](en-selchange.md) . Il codice di notifica specifica una struttura [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) contenente informazioni sulla nuova selezione. Un controllo Rich Edit invia questo codice di notifica solo se lo si Abilita usando il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .

Per impostazione predefinita, un controllo Rich Edit Mostra e nasconde l'evidenziazione della selezione quando ottiene lo stato attivo e lo perde. È possibile mostrare o nascondere l'evidenziazione della selezione in qualsiasi momento usando il messaggio [**\_ HIDESELECTION em**](em-hideselection.md) . Ad esempio, un'applicazione potrebbe fornire una finestra di dialogo di ricerca per trovare il testo in un controllo Rich Edit. L'applicazione potrebbe selezionare testo corrispondente senza chiudere la finestra di dialogo. in questo caso, è necessario usare il messaggio **\_ HIDESELECTION em** per evidenziare la selezione.

Come per i controlli di modifica, è possibile specificare lo stile della finestra [**es \_ NOHIDESEL**](edit-control-styles.md) per evitare che un controllo Rich Edit nasconda l'evidenziazione della selezione quando perde lo stato attivo.

In alternativa all'uso dei messaggi [**em \_ EXGETSEL**](em-exgetsel.md) e [**em \_ EXSETSEL**](em-exsetsel.md) , è possibile recuperare e impostare la selezione corrente usando i messaggi [**em \_ GETSEL**](em-getsel.md) e [**em \_ SETSEL**](em-setsel.md) Edit Control. Il **\_ GETSEL** di messaggi em indici di tipo carattere a 2 16 bit nel valore restituito a 32 bit e pertanto funziona solo per le selezioni che rientrano interamente nei primi 64K. Tuttavia, un controllo Rich Edit non conterrà mai più di 32K caratteri di testo, a meno che non si estenda questo limite usando il messaggio [**em \_ LIMITTEXT**](em-limittext.md) o [**em \_ EXLIMITTEXT**](em-exlimittext.md) . Per le selezioni che si estendono oltre i primi 64 KB di testo, il messaggio **em \_ GETSEL** restituisce-1. In tal caso, è ancora possibile utilizzare i valori restituiti in *wParam* e *lParam* per trovare i caratteri iniziale e finale della selezione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





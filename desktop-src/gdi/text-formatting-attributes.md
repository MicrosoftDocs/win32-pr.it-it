---
description: "Un'applicazione può usare sei funzioni per impostare gli attributi di formattazione del testo per un contesto di dispositivo: SetBkColor, SetBkMode, SetTextAlign, SetTextCharacterExtra, SetTextColor e SetTextJustification."
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Attributi di Text-Formatting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d345bfcfe1693a7ff0b25bb323615dffe221ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553622"
---
# <a name="text-formatting-attributes"></a>Attributi di Text-Formatting

Un'applicazione può usare sei funzioni per impostare gli attributi di formattazione del testo per un contesto di dispositivo: [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor), [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode), [setTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign), [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra), [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)e [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification). Queste funzioni influiscono sull'allineamento del testo, la spaziatura tra caratteri, la giustificazione del testo e i colori di sfondo e di testo. Inoltre, è possibile usare altre sei funzioni per recuperare gli attributi di formattazione del testo correnti per qualsiasi contesto di dispositivo: [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor), [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode), [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign), [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra), [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)e [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a).

## <a name="text-alignment"></a>Allineamento testo

Le applicazioni possono utilizzare la funzione [setTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) per specificare il modo in cui il sistema deve posizionare i caratteri in una stringa di testo quando chiamano una delle funzioni di disegno. Questa funzione può essere utilizzata per posizionare le intestazioni, i numeri di pagina, i callout e così via. Il sistema posiziona una stringa di testo allineando un punto di riferimento su un rettangolo immaginario che racchiude la stringa, con la posizione corrente del cursore o con un punto passato come argomento a una delle funzioni di disegno del testo. La funzione [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) consente all'applicazione di specificare la posizione del punto di riferimento. Di seguito è riportato un elenco delle possibili posizioni dei punti di riferimento.



| Location         | Descrizione                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| a sinistra/in basso      | Il punto di riferimento si trova nell'angolo inferiore sinistro del rettangolo.                                               |
| riga a sinistra/base   | Il punto di riferimento si trova in corrispondenza dell'intersezione tra la linea di base della cella di caratteri e il bordo sinistro del rettangolo.  |
| sinistra/superiore         | Il punto di riferimento si trova nell'angolo superiore sinistro del rettangolo.                                                 |
| al centro/inferiore    | Il punto di riferimento si trova al centro della parte inferiore del rettangolo.                                            |
| linea al centro/base | Il punto di riferimento si trova in corrispondenza dell'intersezione tra la linea di base della cella di caratteri e il centro del rettangolo.     |
| al centro/superiore       | Il punto di riferimento si trova al centro della parte superiore del rettangolo.                                               |
| a destra/in basso     | Il punto di riferimento si trova nell'angolo inferiore destro del rettangolo.                                              |
| a destra/linea di base  | Il punto di riferimento si trova in corrispondenza dell'intersezione tra la linea di base della cella di caratteri e il bordo destro del rettangolo. |
| a destra/in alto        | Il punto di riferimento si trova nell'angolo superiore destro del rettangolo.                                                |



 

Nella figura seguente viene illustrata una stringa di testo disegnata chiamando la funzione di [testo](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . Prima di disegnare il testo, è stata chiamata la funzione [setTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) per spostare il punto di riferimento in ognuna delle nove posizioni possibili.

![illustrazione che mostra lo stesso testo per nove volte, una per ogni possibile posizione dei punti di riferimento](images/csftx-04.png)

L'allineamento del testo predefinito per un contesto di dispositivo è l'angolo superiore sinistro del rettangolo immaginario che racchiude il testo. Un'applicazione può recuperare l'impostazione di allineamento del testo corrente per qualsiasi contesto di dispositivo chiamando la funzione [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) .

## <a name="intercharacter-spacing"></a>Spaziatura tra caratteri

Le applicazioni possono usare la funzione [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) per modificare la spaziatura tra caratteri per tutte le operazioni di output di testo in un contesto di dispositivo specificato. Nella figura seguente viene illustrata una stringa di testo disegnata due volte chiamando la funzione di [testo](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . Prima di disegnare il testo la seconda volta, è stata chiamata la funzione [**SetTextCharacterExtra**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) per incrementare la spaziatura tra caratteri.

![l'illustrazione shoing lo stesso testo due volte: prima con la spaziatura tra caratteri normali, quindi con spaziatura più ampia](images/csftx-06.png)

Il valore di spaziatura tra caratteri predefinito per qualsiasi contesto di dispositivo è zero. Un'applicazione può recuperare il valore di spaziatura tra caratteri corrente per un contesto di dispositivo chiamando la funzione [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) .

## <a name="text-justification"></a>Giustificazione testo

Le applicazioni possono utilizzare le funzioni [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) e [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) per giustificare una riga di testo. La giustificazione del testo è un'operazione comune in qualsiasi pubblicazione desktop e nella maggior parte delle applicazioni di elaborazione di Word. La funzione [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) calcola la larghezza e l'altezza di una stringa di testo. Una volta calcolata la larghezza, l'applicazione può chiamare la funzione [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) per distribuire la spaziatura aggiuntiva tra le parole in una riga di testo. Nella figura seguente viene illustrato un paragrafo di testo stampato due volte: nel primo paragrafo il testo non è stato giustificato; nel secondo paragrafo, il testo è stato giustificato chiamando le funzioni **GetTextExtentPoint32** e **SetTextJustification** .

![illustrazione che mostra un paragrafo che allinea solo a sinistra, quindi lo stesso paragrafo allineato a sinistra e a destra](images/csftx-05.png)

## <a name="text-and-background-color"></a>Testo e colore di sfondo

Le applicazioni possono utilizzare la funzione [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) per impostare il colore del testo disegnato nell'area client delle rispettive finestre, nonché il colore del testo disegnato su una stampante di colori. Un'applicazione può utilizzare la funzione [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) per impostare il colore che viene visualizzato dietro ogni carattere e la funzione [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) per specificare il modo in cui il sistema deve fondere il colore di sfondo selezionato con il colore o i colori correnti della visualizzazione video.

Il colore del testo predefinito per un contesto di dispositivo di visualizzazione è nero; il colore di sfondo predefinito è bianco; e la modalità di sfondo predefinita è OPACa. Un'applicazione può recuperare il colore del testo corrente per un contesto di dispositivo chiamando la funzione [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) . Un'applicazione può recuperare il colore di sfondo corrente per un contesto di dispositivo chiamando la funzione [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) e la modalità di sfondo corrente chiamando la funzione [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) .

 

 

---
description: "Un'applicazione può usare sei funzioni per impostare gli attributi di formattazione del testo per un contesto di dispositivo: SetBkColor, SetBkMode, SetTextAlign, SetTextCharacterExtra, SetTextColor e SetTextJustification."
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Text-Formatting attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e74cb8d30a0eb9b44f05be611da963b413e8798b81da2a334dc083bd3cc1651
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015281"
---
# <a name="text-formatting-attributes"></a>Text-Formatting attributi

Un'applicazione può usare sei funzioni per impostare gli attributi di formattazione del testo per un contesto di dispositivo: [SetBkColor,](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) [SetBkMode,](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) [SetTextAlign,](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) [SetTextCharacterExtra,](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)e [SetTextJustification.](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) Queste funzioni influiscono sull'allineamento del testo, sulla spaziatura tra caratteri, sulla giustificazione del testo e sui colori del testo e dello sfondo. È inoltre possibile usare altre sei funzioni per recuperare gli attributi di formattazione del testo correnti per qualsiasi contesto di dispositivo: [GetBkColor,](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) [GetBkMode,](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) [GetTextAlign,](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) [GetTextCharacterExtra,](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)e [GetTextExtentPoint32.](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)

## <a name="text-alignment"></a>Allineamento testo

Le applicazioni possono usare [la funzione SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) per specificare come il sistema deve posizionare i caratteri in una stringa di testo quando chiama una delle funzioni di disegno. Questa funzione può essere usata per posizionare intestazioni, numeri di pagina, callout e così via. Il sistema posiziona una stringa di testo allineando un punto di riferimento su un rettangolo immaginario che circonda la stringa, con la posizione corrente del cursore o con un punto passato come argomento a una delle funzioni di disegno del testo. La [**funzione SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) consente all'applicazione di specificare il percorso di questo punto di riferimento. Di seguito è riportato un elenco delle possibili posizioni dei punti di riferimento.



| Location         | Descrizione                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| sinistra/inferiore      | Il punto di riferimento si trova nell'angolo inferiore sinistro del rettangolo.                                               |
| riga sinistra/base   | Il punto di riferimento si trova all'intersezione tra la linea di base della cella carattere e il bordo sinistro del rettangolo.  |
| sinistra/superiore         | Il punto di riferimento si trova nell'angolo superiore sinistro del rettangolo.                                                 |
| al centro/in basso    | Il punto di riferimento si trova al centro della parte inferiore del rettangolo.                                            |
| linea centrale/di base | Il punto di riferimento si trova all'intersezione tra la linea di base della cella carattere e il centro del rettangolo.     |
| center/top       | Il punto di riferimento si trova al centro della parte superiore del rettangolo.                                               |
| destra/inferiore     | Il punto di riferimento si trova nell'angolo inferiore destro del rettangolo.                                              |
| destra/linea di base  | Il punto di riferimento si trova in corrispondenza dell'intersezione tra la linea di base della cella carattere e il bordo destro del rettangolo. |
| a destra/in alto        | Il punto di riferimento si trova nell'angolo superiore destro del rettangolo.                                                |



 

La figura seguente mostra una stringa di testo disegnata chiamando la [funzione TextOut.](/windows/desktop/api/Wingdi/nf-wingdi-textouta) Prima di disegnare il testo, è stata chiamata la funzione [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) per spostare il punto di riferimento in ognuna delle nove posizioni possibili.

![Figura che mostra lo stesso testo nove volte, una per ogni possibile posizione del punto di riferimento](images/csftx-04.png)

L'allineamento del testo predefinito per un contesto di dispositivo è l'angolo superiore sinistro del rettangolo immaginario che circonda il testo. Un'applicazione può recuperare l'impostazione di allineamento del testo corrente per qualsiasi contesto di dispositivo chiamando la [funzione GetTextAlign.](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)

## <a name="intercharacter-spacing"></a>Spaziatura intercharacter

Le applicazioni possono usare [la funzione SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) per modificare la spaziatura intercharacter per tutte le operazioni di output di testo in un contesto di dispositivo specificato. La figura seguente mostra una stringa di testo disegnata due volte chiamando la [funzione TextOut.](/windows/desktop/api/Wingdi/nf-wingdi-textouta) Prima di disegnare il testo la seconda volta, è stata chiamata la [**funzione SetTextCharacterExtra**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) per incrementare la spaziatura tra caratteri.

![illustrazione che insacca lo stesso testo due volte: prima con una spaziatura intercharacter normale, quindi con una spaziatura più ampia](images/csftx-06.png)

Il valore predefinito della spaziatura intercharacter per qualsiasi contesto di dispositivo è zero. Un'applicazione può recuperare il valore di spaziatura intercharacter corrente per un contesto di dispositivo chiamando la [funzione GetTextCharacterExtra.](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)

## <a name="text-justification"></a>Giustificazione del testo

Le applicazioni possono usare [le funzioni GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) e [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) per giustificare una riga di testo. La giustificazione del testo è un'operazione comune in qualsiasi pubblicazione desktop e nella maggior parte delle applicazioni di elaborazione testi. La [**funzione GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) calcola la larghezza e l'altezza di una stringa di testo. Dopo aver calcolato la larghezza, l'applicazione può chiamare la [**funzione SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) per distribuire una spaziatura aggiuntiva tra ognuna delle parole in una riga di testo. La figura seguente mostra un paragrafo di testo stampato due volte: nel primo paragrafo il testo non è stato giustificato; nel secondo paragrafo, il testo è stato giustificato chiamando le **funzioni GetTextExtentPoint32** **e SetTextJustification.**

![figura che mostra un paragrafo allineato solo a sinistra, quindi lo stesso paragrafo allineato a sinistra e a destra](images/csftx-05.png)

## <a name="text-and-background-color"></a>Colore del testo e dello sfondo

Le applicazioni possono usare la [funzione SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) per impostare il colore del testo disegnato nell'area client delle finestre, nonché il colore del testo disegnato su una stampante a colori. Un'applicazione può usare la [funzione SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) per impostare il colore visualizzato dietro ogni carattere e la [funzione SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) per specificare in che modo il sistema deve unire il colore di sfondo selezionato con il colore o i colori correnti sullo schermo video.

Il colore del testo predefinito per un contesto di dispositivo di visualizzazione è nero. il colore di sfondo predefinito è bianco; e la modalità in background predefinita è OPAQUE. Un'applicazione può recuperare il colore del testo corrente per un contesto di dispositivo chiamando la [funzione GetTextColor.](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) Un'applicazione può recuperare il colore di sfondo corrente per un contesto di dispositivo chiamando la [funzione GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) e la modalità di sfondo corrente chiamando la [funzione GetBkMode.](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)

 

 

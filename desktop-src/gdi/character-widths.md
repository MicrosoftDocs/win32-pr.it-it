---
description: Le applicazioni devono recuperare dati a larghezza di carattere quando eseguono attività come l'adattamento di stringhe di testo a larghezze di pagine o colonne.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Larghezze dei caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822ae01ea1ccd5a2a7ec118cb1b93211b1c2e5c0a215737a600d9450b8996117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888100"
---
# <a name="character-widths"></a>Larghezze dei caratteri

Le applicazioni devono recuperare dati a larghezza di carattere quando eseguono attività come l'adattamento di stringhe di testo a larghezze di pagine o colonne. Un'applicazione può usare quattro funzioni per recuperare dati a larghezza di carattere. Due di queste funzioni recuperano la larghezza di avanzamento carattere e due di queste funzioni recuperano i dati effettivi della larghezza dei caratteri.

Un'applicazione può usare le [funzioni GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) e [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) per recuperare la larghezza di avanzamento per singoli caratteri o simboli in una stringa di testo. La larghezza di avanzamento è la distanza che il cursore su una visualizzazione video o la testina di stampa su una stampante deve avanzare prima di stampare il carattere successivo in una stringa di testo. La [**funzione GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) restituisce la larghezza di avanzamento come valore intero. Se è necessaria una maggiore precisione, un'applicazione può usare la [**funzione GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) per recuperare i valori di avanzamento frazionari della larghezza.

Un'applicazione può recuperare dati effettivi a larghezza di carattere usando le [funzioni GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) e [**GetCharABCWidthsFloat.**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) La **funzione GetCharABCWidthsFloat** funziona con tutti i tipi di carattere. La [**funzione GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) funziona solo con i tipi di carattere TrueType e OpenType. Per altre informazioni sui tipi di carattere TrueType e OpenType, vedere Tipi di carattere [Raster, Vector, TrueType e OpenType](raster--vector--truetype--and-opentype-fonts.md).

La figura seguente mostra i tre componenti di una larghezza di carattere:

![Figura che mostra la spaziatura a, la spaziatura b e la spaziatura c di due caratteri adiacenti](images/csftx-02.png)

La spaziatura A è la larghezza da aggiungere alla posizione corrente prima di posizionare il carattere. La spaziatura B è la larghezza del carattere stesso. La spaziatura C è lo spazio vuoto a destra del carattere. La larghezza di avanzamento totale viene determinata calcolando la somma di A+B+C. La cella carattere è un rettangolo immaginario che racchiude ogni carattere o simbolo in un tipo di carattere. Poiché i caratteri possono sovrassare o sottofasare la cella del carattere, uno o entrambi gli incrementi A e C possono essere un numero negativo.

 

 

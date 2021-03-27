---
description: Le applicazioni devono recuperare i dati di larghezza dei caratteri quando eseguono attività come l'adattamento di stringhe di testo a larghezze di pagina o di colonna.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Larghezza caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fbb7e6ad1e5f4ef12f2abd9e528ce3158a869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880330"
---
# <a name="character-widths"></a>Larghezza caratteri

Le applicazioni devono recuperare i dati di larghezza dei caratteri quando eseguono attività come l'adattamento di stringhe di testo a larghezze di pagina o di colonna. Sono disponibili quattro funzioni che possono essere utilizzate da un'applicazione per recuperare dati di larghezza del carattere. Due di queste funzioni recuperano la larghezza dei caratteri di avanzamento e due di queste funzioni recuperano i dati effettivi della larghezza dei caratteri.

Un'applicazione può utilizzare le funzioni [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) e [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) per recuperare la larghezza di avanzamento per i singoli caratteri o simboli in una stringa di testo. La larghezza progressiva è la distanza con cui il cursore su uno schermo video o l'intestazione di stampa su una stampante deve avanzare prima di stampare il carattere successivo in una stringa di testo. La funzione [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) restituisce la larghezza di avanzamento come valore integer. Se è necessaria una maggiore precisione, un'applicazione può usare la funzione [**GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) per recuperare i valori di larghezza in avanti frazionari.

Un'applicazione può recuperare i dati effettivi della larghezza del carattere usando le funzioni [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) e [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) . La funzione **GetCharABCWidthsFloat** funziona con tutti i tipi di carattere. La funzione [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) funziona solo con i tipi di carattere TrueType e OpenType. Per ulteriori informazioni sui tipi di carattere TrueType e OpenType, vedere [raster, Vector, TrueType e OpenType](raster--vector--truetype--and-opentype-fonts.md).

Nella figura seguente sono illustrati i tre componenti di una larghezza di caratteri:

![illustrazione che mostra la spaziatura, la spaziatura b e la spaziatura c di due caratteri adiacenti](images/csftx-02.png)

La spaziatura a è la larghezza da aggiungere alla posizione corrente prima di inserire il carattere. La spaziatura B corrisponde alla larghezza del carattere stesso. La spaziatura C rappresenta lo spazio vuoto a destra del carattere. La larghezza di avanzamento totale viene determinata calcolando la somma di A + B + C. La cella del carattere è un rettangolo immaginario che racchiude ogni carattere o simbolo in un tipo di carattere. Poiché i caratteri possono sporgere o sottoappendere la cella di tipo carattere, uno o entrambi gli incrementi A e C possono essere un numero negativo.

 

 

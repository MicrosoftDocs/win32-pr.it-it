---
description: Nel testo unidirezionale, la posizione del punto di inserimento non ha ambiguità perché il bordo principale di un carattere si trova nella stessa posizione del bordo finale del carattere precedente.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Visualizzazione del cursore nelle stringhe bidirezionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317167"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a>Visualizzazione del cursore nelle stringhe bidirezionali

Nel testo unidirezionale, la posizione del punto di inserimento non ha ambiguità perché il bordo principale di un carattere si trova nella stessa posizione del bordo finale del carattere precedente. Tuttavia, nel testo bidirezionale, la posizione del punto di inserimento tra le esecuzioni della direzione opposta è ambigua. Nel paragrafo da sinistra a destra "hellosalaam", ad esempio, l'ultima lettera di "Hello" precede immediatamente la prima lettera di "Salaam". La posizione migliore in cui visualizzare il punto di inserimento dipende dal fatto che venga considerata come segue "o" di "Hello" o che preceda "s" di "Salaam".

Uniscribe usa le convenzioni di posizionamento del cursore indicate nella tabella seguente.



| Situazione       | Posizionamento del cursore visivo                       |
|-----------------|----------------------------------------------|
| Digitazione          | Bordo finale dell'ultimo carattere digitato.       |
| Incollare         | Bordo finale dell'ultimo carattere incollato.      |
| Avanzamento del cursore | Bordo finale dell'ultimo carattere passato. |
| Ritiro del cursore  | Bordo principale dell'ultimo carattere passato.  |
| Home page            | Bordo principale della linea.                        |
| Fine             | Bordo finale della linea.                       |



 

Il punto di inserimento può essere posizionato come illustrato nell'esempio seguente:


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



Il posizionamento del punto di inserimento può essere più semplice, come illustrato di seguito, dato un valore *fAdvancing* limitato a **true** o **false**:


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) gestisce logicamente le posizioni fuori intervallo. Restituisce il bordo principale dell'esecuzione per *iCharPos* <0 e il bordo finale dell'esecuzione per *iCharPos* >= length. Per ulteriori informazioni, vedere [gestione del posizionamento del cursore e hit testing](managing-caret-placement-and-hit-testing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




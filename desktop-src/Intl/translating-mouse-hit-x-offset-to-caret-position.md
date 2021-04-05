---
description: Convenzionalmente, l'utente può selezionare la posizione del punto di inserimento (CP) facendo clic sulla metà finale del carattere &\# 0034; CP-1&\# 0034; o sulla metà principale del carattere &\# 0034; CP&\# 0034;.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Conversione dell'offset X del mouse nella posizione del punto di inserimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f993de35ebffac4740b367927d1a8edf864a813e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882129"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Conversione dell'offset X del mouse nella posizione del punto di inserimento

Convenzionalmente, l'utente può selezionare la posizione del punto di inserimento (CP) facendo clic sulla metà finale del carattere "CP-1" o sulla metà principale del carattere "CP". Un'applicazione può implementare la conversione dell'offset x del mouse nella posizione del punto di inserimento, come indicato di seguito:


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



Per gli script che bloccano il punto di inserimento ai limiti del cluster, una chiamata a [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) restituisce con *fTrailing* impostato su 0 o la larghezza del cluster nei punti di codice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




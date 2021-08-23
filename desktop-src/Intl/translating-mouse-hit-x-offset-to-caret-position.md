---
description: In modo convenzionale, l'utente può selezionare la posizione del cursore (cp) facendo clic sulla metà finale del carattere &\# 0034;cp-1&0034; o sulla metà iniziale del carattere \# &\# 0034;cp&\# 0034;.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Conversione dell'offset X dell'hit del mouse nella posizione del cursore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e135efaccb6454e55999d21f00e762d749eb380751848aef88cf4b4e5b8e913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693181"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Conversione dell'offset X dell'hit del mouse nella posizione del cursore

In modo convenzionale, l'utente può selezionare la posizione del cursore (cp) facendo clic sulla metà finale del carattere "cp-1" o sulla metà iniziale del carattere "cp". Un'applicazione può implementare la conversione dell'offset x dell'hit del mouse nella posizione del cursore, come indicato di seguito:


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



Per gli script che bloccano il punto di aggancio ai limiti del cluster, una chiamata a [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) restituisce con *fTrailing* impostato su 0 o sulla larghezza del cluster nei punti di codice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




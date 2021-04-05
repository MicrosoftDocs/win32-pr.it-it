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
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a><span data-ttu-id="5bdb1-103">Conversione dell'offset X del mouse nella posizione del punto di inserimento</span><span class="sxs-lookup"><span data-stu-id="5bdb1-103">Translating Mouse Hit X Offset to Caret Position</span></span>

<span data-ttu-id="5bdb1-104">Convenzionalmente, l'utente può selezionare la posizione del punto di inserimento (CP) facendo clic sulla metà finale del carattere "CP-1" o sulla metà principale del carattere "CP".</span><span class="sxs-lookup"><span data-stu-id="5bdb1-104">Conventionally, the user can select caret position (cp) by clicking either the trailing half of character "cp-1" or the leading half of character "cp".</span></span> <span data-ttu-id="5bdb1-105">Un'applicazione può implementare la conversione dell'offset x del mouse nella posizione del punto di inserimento, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5bdb1-105">An application can implement the translation of mouse hit x offset to caret position as follows:</span></span>


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



<span data-ttu-id="5bdb1-106">Per gli script che bloccano il punto di inserimento ai limiti del cluster, una chiamata a [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) restituisce con *fTrailing* impostato su 0 o la larghezza del cluster nei punti di codice.</span><span class="sxs-lookup"><span data-stu-id="5bdb1-106">For scripts that snap the caret to cluster boundaries, a call to [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) returns with *fTrailing* set to either 0 or the width of the cluster in code points.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bdb1-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5bdb1-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bdb1-108">Uso di Uniscribe</span><span class="sxs-lookup"><span data-stu-id="5bdb1-108">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




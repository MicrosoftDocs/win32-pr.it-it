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
# <a name="displaying-the-caret-in-bidirectional-strings"></a><span data-ttu-id="688be-103">Visualizzazione del cursore nelle stringhe bidirezionali</span><span class="sxs-lookup"><span data-stu-id="688be-103">Displaying the Caret in Bidirectional Strings</span></span>

<span data-ttu-id="688be-104">Nel testo unidirezionale, la posizione del punto di inserimento non ha ambiguità perché il bordo principale di un carattere si trova nella stessa posizione del bordo finale del carattere precedente.</span><span class="sxs-lookup"><span data-stu-id="688be-104">In unidirectional text, the caret position has no ambiguity because the leading edge of a character is at the same place as the trailing edge of the previous character.</span></span> <span data-ttu-id="688be-105">Tuttavia, nel testo bidirezionale, la posizione del punto di inserimento tra le esecuzioni della direzione opposta è ambigua.</span><span class="sxs-lookup"><span data-stu-id="688be-105">However, in bidirectional text, the caret position between runs of opposing direction is ambiguous.</span></span> <span data-ttu-id="688be-106">Nel paragrafo da sinistra a destra "hellosalaam", ad esempio, l'ultima lettera di "Hello" precede immediatamente la prima lettera di "Salaam".</span><span class="sxs-lookup"><span data-stu-id="688be-106">For example, in the left-to-right paragraph "hellosalaam", the last letter of "hello" immediately precedes the first letter of "salaam".</span></span> <span data-ttu-id="688be-107">La posizione migliore in cui visualizzare il punto di inserimento dipende dal fatto che venga considerata come segue "o" di "Hello" o che preceda "s" di "Salaam".</span><span class="sxs-lookup"><span data-stu-id="688be-107">The best position in which to display the caret depends on whether it is considered to follow the "o" of "hello" or to precede the "s" of "salaam".</span></span>

<span data-ttu-id="688be-108">Uniscribe usa le convenzioni di posizionamento del cursore indicate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="688be-108">Uniscribe uses the caret positioning conventions shown in the next table.</span></span>



| <span data-ttu-id="688be-109">Situazione</span><span class="sxs-lookup"><span data-stu-id="688be-109">Situation</span></span>       | <span data-ttu-id="688be-110">Posizionamento del cursore visivo</span><span class="sxs-lookup"><span data-stu-id="688be-110">Visual caret placement</span></span>                       |
|-----------------|----------------------------------------------|
| <span data-ttu-id="688be-111">Digitazione</span><span class="sxs-lookup"><span data-stu-id="688be-111">Typing</span></span>          | <span data-ttu-id="688be-112">Bordo finale dell'ultimo carattere digitato.</span><span class="sxs-lookup"><span data-stu-id="688be-112">Trailing edge of last character typed.</span></span>       |
| <span data-ttu-id="688be-113">Incollare</span><span class="sxs-lookup"><span data-stu-id="688be-113">Pasting</span></span>         | <span data-ttu-id="688be-114">Bordo finale dell'ultimo carattere incollato.</span><span class="sxs-lookup"><span data-stu-id="688be-114">Trailing edge of last character pasted.</span></span>      |
| <span data-ttu-id="688be-115">Avanzamento del cursore</span><span class="sxs-lookup"><span data-stu-id="688be-115">Caret advancing</span></span> | <span data-ttu-id="688be-116">Bordo finale dell'ultimo carattere passato.</span><span class="sxs-lookup"><span data-stu-id="688be-116">Trailing edge of last character passed over.</span></span> |
| <span data-ttu-id="688be-117">Ritiro del cursore</span><span class="sxs-lookup"><span data-stu-id="688be-117">Caret retiring</span></span>  | <span data-ttu-id="688be-118">Bordo principale dell'ultimo carattere passato.</span><span class="sxs-lookup"><span data-stu-id="688be-118">Leading edge of last character passed over.</span></span>  |
| <span data-ttu-id="688be-119">Home page</span><span class="sxs-lookup"><span data-stu-id="688be-119">Home</span></span>            | <span data-ttu-id="688be-120">Bordo principale della linea.</span><span class="sxs-lookup"><span data-stu-id="688be-120">Leading edge of line.</span></span>                        |
| <span data-ttu-id="688be-121">Fine</span><span class="sxs-lookup"><span data-stu-id="688be-121">End</span></span>             | <span data-ttu-id="688be-122">Bordo finale della linea.</span><span class="sxs-lookup"><span data-stu-id="688be-122">Trailing edge of line.</span></span>                       |



 

<span data-ttu-id="688be-123">Il punto di inserimento può essere posizionato come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="688be-123">The caret can be positioned as shown in the following example:</span></span>


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



<span data-ttu-id="688be-124">Il posizionamento del punto di inserimento può essere più semplice, come illustrato di seguito, dato un valore *fAdvancing* limitato a **true** o **false**:</span><span class="sxs-lookup"><span data-stu-id="688be-124">Positioning of the caret can be simpler, as shown below, given an *fAdvancing* value restricted to **TRUE** or **FALSE**:</span></span>


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



<span data-ttu-id="688be-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) gestisce logicamente le posizioni fuori intervallo.</span><span class="sxs-lookup"><span data-stu-id="688be-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) handles out-of-range positions logically.</span></span> <span data-ttu-id="688be-126">Restituisce il bordo principale dell'esecuzione per *iCharPos* <0 e il bordo finale dell'esecuzione per *iCharPos* >= length.</span><span class="sxs-lookup"><span data-stu-id="688be-126">It returns the leading edge of the run for *iCharPos* <0, and the trailing edge of the run for *iCharPos* >= length.</span></span> <span data-ttu-id="688be-127">Per ulteriori informazioni, vedere [gestione del posizionamento del cursore e hit testing](managing-caret-placement-and-hit-testing.md)</span><span class="sxs-lookup"><span data-stu-id="688be-127">For more information, see [Managing Caret Placement and Hit Testing](managing-caret-placement-and-hit-testing.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="688be-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="688be-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="688be-129">Uso di Uniscribe</span><span class="sxs-lookup"><span data-stu-id="688be-129">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




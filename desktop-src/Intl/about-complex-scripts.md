---
description: Uno script complesso è uno script per il quale il membro fComplex delle \_ proprietà dello script è impostato su true. In questo argomento vengono illustrate in dettaglio le proprietà che possono essere presenti in uno script complesso.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Informazioni sugli script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057817"
---
# <a name="about-complex-scripts"></a><span data-ttu-id="3da40-104">Informazioni sugli script complessi</span><span class="sxs-lookup"><span data-stu-id="3da40-104">About Complex Scripts</span></span>

<span data-ttu-id="3da40-105">Uno [script complesso](uniscribe-glossary.md) è uno script per il quale  il membro FComplex [**delle \_ proprietà dello script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="3da40-105">A [complex script](uniscribe-glossary.md) is a script for which the **fComplex** member of [**SCRIPT\_PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) is set to **TRUE**.</span></span> <span data-ttu-id="3da40-106">In questo argomento vengono illustrate in dettaglio le proprietà che possono essere presenti in uno script complesso.</span><span class="sxs-lookup"><span data-stu-id="3da40-106">This topic details the properties that a complex script might have.</span></span>

## <a name="bidirectional-rendering"></a><span data-ttu-id="3da40-107">Rendering bidirezionale</span><span class="sxs-lookup"><span data-stu-id="3da40-107">Bidirectional Rendering</span></span>

<span data-ttu-id="3da40-108">Il rendering bidirezionale sta gestendo il testo che legge sia da sinistra a destra che da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="3da40-108">Bidirectional rendering is handling of text that reads both left-to-right and right-to-left.</span></span> <span data-ttu-id="3da40-109">Nel rendering bidirezionale dell'arabo, ad esempio, la direzione di lettura predefinita per il testo è da destra a sinistra, ma è da sinistra a destra per alcuni numeri.</span><span class="sxs-lookup"><span data-stu-id="3da40-109">For example, in the bidirectional rendering of Arabic, the default reading direction for text is right-to-left, but it is left-to-right for some numbers.</span></span> <span data-ttu-id="3da40-110">L'elaborazione di uno script complesso deve tenere conto della differenza tra l'ordine logico (sequenza di tasti) e l'ordine visivo dei glifi.</span><span class="sxs-lookup"><span data-stu-id="3da40-110">Processing a complex script must account for the difference between the logical (keystroke) order and the visual order of the glyphs.</span></span> <span data-ttu-id="3da40-111">Inoltre, l'elaborazione deve gestire correttamente il movimento del cursore e l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="3da40-111">In addition, processing must properly deal with caret movement and hit testing.</span></span> <span data-ttu-id="3da40-112">Il mapping tra la posizione dello schermo e un indice dei caratteri richiede la comprensione degli algoritmi di layout per la visualizzazione specifica, ad esempio la selezione del testo o la visualizzazione del cursore.</span><span class="sxs-lookup"><span data-stu-id="3da40-112">The mapping between screen position and a character index requires an understanding of the layout algorithms for the particular display, for example, selection of text or caret display.</span></span>

## <a name="contextual-shaping"></a><span data-ttu-id="3da40-113">Definizione del contesto</span><span class="sxs-lookup"><span data-stu-id="3da40-113">Contextual Shaping</span></span>

<span data-ttu-id="3da40-114">In shaping contestuale, i caratteri script cambiano forma a seconda dei caratteri che li racchiudono.</span><span class="sxs-lookup"><span data-stu-id="3da40-114">In contextual shaping, script characters change shape depending on the characters that surround them.</span></span> <span data-ttu-id="3da40-115">Tale data shaping viene eseguita nella scrittura corsiva in lingua inglese quando una "l" minuscola cambia a seconda del carattere che la precede, ad esempio un "a" (si connette in basso a "l") o "o" (si connette in alto).</span><span class="sxs-lookup"><span data-stu-id="3da40-115">Such shaping occurs in English cursive writing when a lowercase "l" changes shape depending on the character that precedes it, such as an "a" (connects low to the "l") or an "o" (connects high).</span></span> <span data-ttu-id="3da40-116">Ad esempio, l'arabo è uno script che mostra il Shaping contestuale.</span><span class="sxs-lookup"><span data-stu-id="3da40-116">For example, Arabic is a script that exhibits contextual shaping.</span></span>

## <a name="combining-characters"></a><span data-ttu-id="3da40-117">Combinazione di caratteri</span><span class="sxs-lookup"><span data-stu-id="3da40-117">Combining Characters</span></span>

<span data-ttu-id="3da40-118">La combinazione di caratteri, detti anche "legature", sono caratteri che si uniscono a un carattere quando vengono posizionati insieme.</span><span class="sxs-lookup"><span data-stu-id="3da40-118">Combining characters, also called "ligatures," are characters that join into one character when placed together.</span></span> <span data-ttu-id="3da40-119">L'arabo è uno script con molti caratteri combinati.</span><span class="sxs-lookup"><span data-stu-id="3da40-119">Arabic is a script that has many combining characters.</span></span> <span data-ttu-id="3da40-120">Un esempio di utilizzo dei caratteri combinati è "a" seguito da "combinando grave", per il quale la rappresentazione di cui è stato eseguito il rendering è "à".</span><span class="sxs-lookup"><span data-stu-id="3da40-120">One example of the use of combining characters is the "a" followed by "combining grave", for which the rendered representation is "à".</span></span> <span data-ttu-id="3da40-121">Il flusso Unicode "U + 0061 U + 0300" richiede una certa elaborazione per assicurarsi che la "combinazione di tombe" sia posizionata correttamente sopra "a".</span><span class="sxs-lookup"><span data-stu-id="3da40-121">The Unicode stream "U+0061 U+0300" requires some processing to make sure the "combining grave" is correctly positioned above the "a".</span></span>

## <a name="specialized-word-break-and-justification"></a><span data-ttu-id="3da40-122">Pausa e giustificazione di parole specializzate</span><span class="sxs-lookup"><span data-stu-id="3da40-122">Specialized Word Break and Justification</span></span>

<span data-ttu-id="3da40-123">Alcuni script, ad esempio Thai, presentano regole complesse per dividere le parole tra le righe o giustificare il testo su una riga.</span><span class="sxs-lookup"><span data-stu-id="3da40-123">Some scripts, for example, Thai, have complex rules for dividing words between lines or justifying text on a line.</span></span>

## <a name="filtering-for-illegal-character-combinations"></a><span data-ttu-id="3da40-124">Filtro per combinazioni di caratteri non valide</span><span class="sxs-lookup"><span data-stu-id="3da40-124">Filtering for Illegal Character Combinations</span></span>

<span data-ttu-id="3da40-125">Uno script complesso, ad esempio tailandese, può filtrare le combinazioni di caratteri non valide quando un linguaggio non consente determinate combinazioni di caratteri.</span><span class="sxs-lookup"><span data-stu-id="3da40-125">A complex script, for example, Thai, can filter out illegal character combinations when a language does not allow certain character combinations.</span></span>

## <a name="font-fallback"></a><span data-ttu-id="3da40-126">Fallback del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="3da40-126">Font Fallback</span></span>

<span data-ttu-id="3da40-127">Il fallback del tipo di carattere è la selezione automatica di un tipo di carattere diverso dal tipo di carattere selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3da40-127">Font fallback is the automated selection of a font other than the font selected by the user.</span></span> <span data-ttu-id="3da40-128">In Uniscribe il fallback del tipo di carattere viene applicato dalla funzione [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) quando tutto o parte del testo è in uno script che non è supportato dal tipo di carattere selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3da40-128">In Uniscribe, font fallback is applied by the [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) function when all or part of the text is in a script that the user-selected font does not support.</span></span> <span data-ttu-id="3da40-129">Per ulteriori informazioni, vedere [utilizzo del fallback dei tipi di carattere](using-font-fallback.md).</span><span class="sxs-lookup"><span data-stu-id="3da40-129">For more information, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3da40-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3da40-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3da40-131">Informazioni su Uniscribe</span><span class="sxs-lookup"><span data-stu-id="3da40-131">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 




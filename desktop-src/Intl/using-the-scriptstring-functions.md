---
description: Per un'applicazione che si occupa di testo non formattato, Uniscribe fornisce le \* funzioni ScriptString.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Uso delle funzioni ScriptString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a2df5e7515bd605ad48cc7a246941e9b6f08f2
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047554"
---
# <a name="using-the-scriptstring-functions"></a><span data-ttu-id="a4b2d-103">Uso delle funzioni ScriptString</span><span class="sxs-lookup"><span data-stu-id="a4b2d-103">Using the ScriptString Functions</span></span>

<span data-ttu-id="a4b2d-104">Per un'applicazione che si occupa di testo non formattato, Uniscribe fornisce le funzioni **scriptString \*** .</span><span class="sxs-lookup"><span data-stu-id="a4b2d-104">For an application dealing with unformatted text, Uniscribe provides the **ScriptString\*** functions.</span></span> <span data-ttu-id="a4b2d-105">Queste funzioni sono simili a [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)e [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), ma forniscono un supporto completo per gli script, incluso il posizionamento del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-105">These functions are similar to [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext), and [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), but they provide full complex script support, including caret placement.</span></span> <span data-ttu-id="a4b2d-106">Queste funzioni sono simili alle altre funzioni Uniscribe, ma sono adattate ai requisiti più semplici di elaborazione del testo normale.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-106">These functions are similar to the other Uniscribe functions, but are tailored to the simpler requirements of plain text processing.</span></span>

<span data-ttu-id="a4b2d-107">La tabella seguente illustra in dettaglio le funzioni **scriptString \*** e tutte le controparti nelle altre funzioni Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-107">The following table details the **ScriptString\*** functions and any counterparts in the other Uniscribe functions.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a4b2d-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="a4b2d-108">Function</span></span></th>
<th><span data-ttu-id="a4b2d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4b2d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4b2d-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-111">Analizza il testo normale.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-111">Analyzes plain text.</span></span> <span data-ttu-id="a4b2d-112">Questa funzione corrisponde alle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4b2d-112">This function corresponds to the following functions:</span></span><br/> <dl><span data-ttu-id="a4b2d-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span></span><br /><span data-ttu-id="a4b2d-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span></span><br /><span data-ttu-id="a4b2d-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span></span><br /><span data-ttu-id="a4b2d-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span></span><br /><span data-ttu-id="a4b2d-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span></span><br /><span data-ttu-id="a4b2d-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span></span><br /><span data-ttu-id="a4b2d-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4b2d-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-121">Recupera la coordinata x per una posizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-121">Retrieves the x coordinate for a character position.</span></span> <span data-ttu-id="a4b2d-122">Questa funzione corrisponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-122">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4b2d-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-124">Libera una struttura <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a4b2d-124">Frees a <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4b2d-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-126">Converte le larghezze visive in larghezze logiche.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-126">Converts visual widths to logical widths.</span></span> <span data-ttu-id="a4b2d-127">Questa funzione corrisponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-127">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4b2d-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-129">Esegue il mapping delle posizioni del glifo di caratteri in modo analogo a <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, solo per uso legacy.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-129">Maps character glyph positions in a similar way to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, for legacy use only.</span></span> <span data-ttu-id="a4b2d-130">Questa funzione non funziona correttamente con gli script che generano più di un glifo per ogni punto di codice.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-130">This function does not work well with scripts that generate more than one glyph per code point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4b2d-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-132">Visualizza testo normale.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-132">Displays plain text.</span></span> <span data-ttu-id="a4b2d-133">Questa funzione corrisponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-133">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4b2d-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-135">Restituisce un puntatore alla lunghezza di una stringa di testo normale ritagliata.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-135">Returns a pointer to the length of a clipped plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4b2d-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-137">Restituisce un puntatore al buffer degli attributi logici per una stringa di testo normale analizzata.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-137">Returns a pointer to the logical attributes buffer for an analyzed plain text string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4b2d-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-139">Restituisce un puntatore alla dimensione (larghezza e altezza) per una stringa di testo normale analizzata.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-139">Returns a pointer to the size (width and height) for an analyzed plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4b2d-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-141">Identifica le sequenze di punti di codice non valide nello script specificato.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-141">Identifies code point sequences not valid in the given script.</span></span> <span data-ttu-id="a4b2d-142">Questa funzione è diversa da <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, che identifica i punti di codice non presenti in un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-142">This function is different from <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, which identifies code points not present in a font.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4b2d-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b2d-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span></span></td>
<td><span data-ttu-id="a4b2d-144">Converte una coordinata x in una posizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-144">Converts an x coordinate to a character position.</span></span> <span data-ttu-id="a4b2d-145">Questa funzione corrisponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-145">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4b2d-146">Per visualizzare solo testo normale senza modifiche, un'applicazione deve chiamare [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)e quindi [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span><span class="sxs-lookup"><span data-stu-id="a4b2d-146">To only display plain text without any modifications, an application should call [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), and then [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span></span> <span data-ttu-id="a4b2d-147">Le altre funzioni vengono usate per modificare il testo normale prima della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-147">The other functions are used to modify the plain text before display.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4b2d-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4b2d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4b2d-149">Uso di Uniscribe</span><span class="sxs-lookup"><span data-stu-id="a4b2d-149">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 

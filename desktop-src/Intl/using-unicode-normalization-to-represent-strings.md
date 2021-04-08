---
description: Le applicazioni possono utilizzare Unicode per rappresentare stringhe in più formati.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Uso della normalizzazione Unicode per rappresentare le stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885717"
---
# <a name="using-unicode-normalization-to-represent-strings"></a><span data-ttu-id="76131-103">Uso della normalizzazione Unicode per rappresentare le stringhe</span><span class="sxs-lookup"><span data-stu-id="76131-103">Using Unicode Normalization to Represent Strings</span></span>

<span data-ttu-id="76131-104">Le applicazioni possono utilizzare Unicode per rappresentare stringhe in più formati.</span><span class="sxs-lookup"><span data-stu-id="76131-104">Applications can use Unicode to represent strings in multiple forms.</span></span> <span data-ttu-id="76131-105">Poiché l'accettazione Unicode è cresciuta, in particolare tramite Internet, è stata creata la necessità di eliminare le differenze non essenziali nelle stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="76131-105">As Unicode acceptance has grown, especially via the Internet, the need has arisen to eliminate non-essential differences in Unicode strings.</span></span> <span data-ttu-id="76131-106">Più rappresentazioni per una combinazione di caratteri complicano il software, ad esempio quando un server Web risponde a una richiesta di pagina o un linker cerca un identificatore specifico in una libreria.</span><span class="sxs-lookup"><span data-stu-id="76131-106">Multiple representations for a combination of characters complicate software, for example, when a Web server responds to a page request or a linker seeks a particular identifier in a library.</span></span>

> [!Caution]  
> <span data-ttu-id="76131-107">Diverse stringhe Unicode possono sembrare visivamente identiche, aumentando i problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="76131-107">Different Unicode strings can appear to be visually identical, raising security concerns.</span></span> <span data-ttu-id="76131-108">Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="76131-108">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

<span data-ttu-id="76131-109">In risposta a questo requisito, il Consorzio Unicode ha definito un processo denominato "normalizzazione", che produce una rappresentazione binaria per le rappresentazioni binarie equivalenti di un carattere.</span><span class="sxs-lookup"><span data-stu-id="76131-109">In response to this requirement, the Unicode Consortium has defined a process called "normalization," which produces one binary representation for any of the equivalent binary representations of a character.</span></span> <span data-ttu-id="76131-110">Una volta normalizzate, due stringhe sono equivalenti se e solo se hanno rappresentazioni binarie identiche.</span><span class="sxs-lookup"><span data-stu-id="76131-110">Once normalized, two strings are equivalent if and only if they have identical binary representations.</span></span> <span data-ttu-id="76131-111">La normalizzazione Elimina alcune differenze, ma conserva le maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="76131-111">The normalization eliminates some differences but preserves case.</span></span>

<span data-ttu-id="76131-112">Per utilizzare la normalizzazione Unicode, un'applicazione può chiamare le funzioni [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) e [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) per la ridisposizione delle stringhe ACCCORDING a Unicode 4,0 TR \# 15.</span><span class="sxs-lookup"><span data-stu-id="76131-112">To use Unicode normalization, an application can call the [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) and [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) functions for rearrangement of strings acccording to Unicode 4.0 TR\#15.</span></span> <span data-ttu-id="76131-113">La normalizzazione può contribuire a migliorare la sicurezza riducendo le rappresentazioni di stringa alternative con lo stesso significato linguistico.</span><span class="sxs-lookup"><span data-stu-id="76131-113">Normalization can help improve security by reducing alternate string representations that have the same linguistic meaning.</span></span> <span data-ttu-id="76131-114">Tenere presente, tuttavia, che la normalizzazione non può eliminare completamente rappresentazioni alternative.</span><span class="sxs-lookup"><span data-stu-id="76131-114">Remember, however, that normalization cannot eliminate alternate representations entirely.</span></span>

<span data-ttu-id="76131-115">Per una descrizione dettagliata degli standard Unicode per la normalizzazione, vedere Unicode [Standard Annex \# 15: Unicode Normalizzation Forms](https://www.unicode.org/reports/tr15) (UAX \# 15).</span><span class="sxs-lookup"><span data-stu-id="76131-115">For a detailed description of the Unicode standards for normalization, refer to [Unicode Standard Annex \#15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \#15).</span></span>

> [!Caution]  
> <span data-ttu-id="76131-116">Poiché la normalizzazione può modificare il formato di una stringa, i meccanismi di sicurezza o gli algoritmi di convalida dei caratteri devono essere implementati in genere dopo la normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="76131-116">Because normalization can change the form of a string, security mechanisms or character validation algorithms should usually be implemented after normalization.</span></span> <span data-ttu-id="76131-117">Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="76131-117">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="provide-multiple-representations-of-the-same-string"></a><span data-ttu-id="76131-118">Fornire più rappresentazioni della stessa stringa</span><span class="sxs-lookup"><span data-stu-id="76131-118">Provide Multiple Representations of the Same String</span></span>

<span data-ttu-id="76131-119">In molti casi, Unicode consente più rappresentazioni di ciò che è linguisticamente la stessa stringa.</span><span class="sxs-lookup"><span data-stu-id="76131-119">In many cases, Unicode allows multiple representations of what is, linguistically, the same string.</span></span> <span data-ttu-id="76131-120">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="76131-120">For example:</span></span>

-   <span data-ttu-id="76131-121">La lettera maiuscola con dieresis (dieresi) può essere rappresentata come un singolo punto di codice Unicode "Ä" (U + 00C4) o con la combinazione di maiuscole e minuscole ("A" + "̈", ovvero U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="76131-121">Capital A with dieresis (umlaut) can be represented either as a single Unicode code point "Ä" (U+00C4) or the combination of Capital A and the combining Dieresis character ("A" + "¨", that is, U+0041 U+0308).</span></span> <span data-ttu-id="76131-122">Considerazioni simili sono valide per molti altri caratteri con segni diacritici.</span><span class="sxs-lookup"><span data-stu-id="76131-122">Similar considerations apply for many other characters with diacritic marks.</span></span>
-   <span data-ttu-id="76131-123">La lettera maiuscola a se stessa può essere rappresentata nel modo consueto (Latin capital letter A, U + 0041) o fullwidth Latin capital lettera A (U + FF21).</span><span class="sxs-lookup"><span data-stu-id="76131-123">Capital A itself can be represented either in the usual manner (Latin Capital Letter A, U+0041) or by Fullwidth Latin Capital Letter A (U+FF21).</span></span> <span data-ttu-id="76131-124">Considerazioni simili sono valide per le altre semplici lettere latine (sia maiuscole che minuscole) e per i caratteri katakana usati per la scrittura in giapponese.</span><span class="sxs-lookup"><span data-stu-id="76131-124">Similar considerations apply for the other simple Latin letters (both uppercase and lowercase) and for the katakana characters used in writing Japanese.</span></span>
-   <span data-ttu-id="76131-125">La stringa "Fi" può essere rappresentata dai caratteri "f" e "i" (U + 0066 U + 0069) o dalla legatura "Fi" (U + FB01).</span><span class="sxs-lookup"><span data-stu-id="76131-125">The string "fi" can be represented either by the characters "f" and "i" (U+0066 U+0069) or by the ligature "ﬁ" (U+FB01).</span></span> <span data-ttu-id="76131-126">Considerazioni simili si applicano a molte altre combinazioni di caratteri per le quali Unicode definisce legature.</span><span class="sxs-lookup"><span data-stu-id="76131-126">Similar considerations apply for many other combinations of characters for which Unicode defines ligatures.</span></span>

## <a name="use-the-four-defined-normalization-forms"></a><span data-ttu-id="76131-127">Usare i quattro formati di normalizzazione definiti</span><span class="sxs-lookup"><span data-stu-id="76131-127">Use the Four Defined Normalization Forms</span></span>

<span data-ttu-id="76131-128">Le applicazioni possono eseguire la normalizzazione Unicode usando diversi algoritmi, detti "forme di normalizzazione", che rispettano diverse regole.</span><span class="sxs-lookup"><span data-stu-id="76131-128">Your applications can perform Unicode normalization using several algorithms, called "normalization forms," that obey different rules.</span></span> <span data-ttu-id="76131-129">Unicode Consortium ha definito quattro forme di normalizzazione: NFC (form C), NFD (form D), NFKC (form KC) e NFKD (form KD).</span><span class="sxs-lookup"><span data-stu-id="76131-129">The Unicode Consortium has defined four normalization forms: NFC (form C), NFD (form D), NFKC (form KC), and NFKD (form KD).</span></span> <span data-ttu-id="76131-130">Ogni modulo Elimina alcune differenze, ma conserva i casi.</span><span class="sxs-lookup"><span data-stu-id="76131-130">Each form eliminates some differences but preserves case.</span></span> <span data-ttu-id="76131-131">Win32 e il .NET Framework supportano tutti e quattro i form di normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="76131-131">Win32 and the .NET Framework support all four normalization forms.</span></span>

<span data-ttu-id="76131-132">Il [**\_ modulo**](/windows/desktop/api/Winnls/ne-winnls-norm_form) NLS Enumeration Type Norm supporta i quattro formati standard di normalizzazione Unicode.</span><span class="sxs-lookup"><span data-stu-id="76131-132">The NLS enumeration type [**NORM\_FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) supports the four standard Unicode normalization forms.</span></span> <span data-ttu-id="76131-133">I form C e D forniscono forme canoniche per le stringhe.</span><span class="sxs-lookup"><span data-stu-id="76131-133">Forms C and D provide canonical forms for strings.</span></span> <span data-ttu-id="76131-134">Le forme non canoniche KC e KD forniscono una maggiore compatibilità e possono rivelare determinate equivalenze semantiche che non sono evidenti nei moduli C e D. Tuttavia, lo fanno a scapito di una certa perdita di informazioni e in genere non devono essere usate come metodo canonico per archiviare le stringhe.</span><span class="sxs-lookup"><span data-stu-id="76131-134">Non-canonical forms KC and KD provide further compatibility, and can reveal certain semantic equivalences that are not apparent in forms C and D. However, they do so at the expense of a certain loss of information, and generally should not be used as a canonical way to store strings.</span></span>

<span data-ttu-id="76131-135">Tra le due forme canoniche, il form C è un formato "composto" e il form D è un formato "decomposto".</span><span class="sxs-lookup"><span data-stu-id="76131-135">Of the two canonical forms, form C is a "composed" form and form D is a "decomposed" form.</span></span> <span data-ttu-id="76131-136">Ad esempio, il form C usa il singolo punto di codice Unicode "Ä" (U + 00C4), mentre il form D USA ("A" + "̈", ovvero U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="76131-136">For example, form C uses the single Unicode code point "Ä" (U+00C4), while form D uses ("A" + "¨", that is U+0041 U+0308).</span></span> <span data-ttu-id="76131-137">Questi rendering sono identici, perché "̈" (U + 0308) è un carattere di combinazione.</span><span class="sxs-lookup"><span data-stu-id="76131-137">These render identically, because "¨" (U+0308) is a combining character.</span></span> <span data-ttu-id="76131-138">Il form D può utilizzare un numero qualsiasi di punti di codice per rappresentare un singolo punto di codice utilizzato dal form C.</span><span class="sxs-lookup"><span data-stu-id="76131-138">Form D can use any number of code points to represent a single code point used by form C.</span></span>

<span data-ttu-id="76131-139">Se due stringhe sono identiche in entrambi i form C o form D, sono identiche nell'altro form.</span><span class="sxs-lookup"><span data-stu-id="76131-139">If two strings are identical in either form C or form D, they are identical in the other form.</span></span> <span data-ttu-id="76131-140">Inoltre, quando il rendering viene eseguito correttamente, vengono visualizzati in modo indistinguibile l'uno dall'altro e dalla stringa originale non normalizzata.</span><span class="sxs-lookup"><span data-stu-id="76131-140">Furthermore, when correctly rendered, they display indistinguishably from one another and from the original non-normalized string.</span></span>

<span data-ttu-id="76131-141">Una volta normalizzate, le stringhe non possono essere restituite in modo coerente alla relativa rappresentazione originale.</span><span class="sxs-lookup"><span data-stu-id="76131-141">Once normalized, strings cannot be consistently returned to their original representation.</span></span> <span data-ttu-id="76131-142">Se, ad esempio, una stringa con una combinazione di rappresentazioni di caratteri composti e scomposti viene convertita in un formato normalizzato, non è possibile denormalizzarla nella stringa mista originale.</span><span class="sxs-lookup"><span data-stu-id="76131-142">For example, if a string with a mixture of composed and decomposed character representations is converted to a normalized form, there is no way to un-normalize it to the original mixed string.</span></span> <span data-ttu-id="76131-143">Pertanto, se un'applicazione richiede la rappresentazione originale della stringa, deve archiviare in modo esplicito tale rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="76131-143">Therefore, if an application requires the original representation of the string, it must store that representation explicitly.</span></span> <span data-ttu-id="76131-144">Tuttavia, la conversione tra le due forme canoniche è reversibile.</span><span class="sxs-lookup"><span data-stu-id="76131-144">However, converting between the two canonical forms is reversible.</span></span> <span data-ttu-id="76131-145">Una stringa nel formato C può essere convertita in forma D, quindi di nuovo nel form C e il risultato è identico alla stringa C del formato originale.</span><span class="sxs-lookup"><span data-stu-id="76131-145">A string in form C can be converted to form D and then back to form C, and the result is identical to the original form C string.</span></span>

<span data-ttu-id="76131-146">I moduli KC e KD sono simili rispettivamente ai form C e D, ma questi "moduli di compatibilità" hanno mapping aggiuntivi di caratteri compatibili alla forma di base di ogni carattere.</span><span class="sxs-lookup"><span data-stu-id="76131-146">Forms KC and KD are similar to forms C and D, respectively, but these "compatibility forms" have additional mappings of compatible characters to the basic form of each character.</span></span> <span data-ttu-id="76131-147">Tali mapping possono causare la perdita delle variazioni dei caratteri secondari.</span><span class="sxs-lookup"><span data-stu-id="76131-147">Such mappings can cause minor character variations to be lost.</span></span> <span data-ttu-id="76131-148">Combinano alcuni caratteri visivamente distinti.</span><span class="sxs-lookup"><span data-stu-id="76131-148">They combine certain characters that are visually distinct.</span></span> <span data-ttu-id="76131-149">Ad esempio, combinano caratteri a larghezza intera e a metà larghezza con lo stesso significato semantico, o forme diverse della stessa lettera araba, o la legatura "Fi" (U + FB01) e la coppia di caratteri "Fi" (U + 0066 U + 0069).</span><span class="sxs-lookup"><span data-stu-id="76131-149">For example, they combine full-width and half-width characters with the same semantic meaning, or different forms of the same Arabic letter, or the ligature "ﬁ" (U+FB01) and the character pair "fi" (U+0066 U+0069).</span></span> <span data-ttu-id="76131-150">Combinano anche alcuni caratteri che talvolta possono avere un significato semantico diverso, ad esempio una cifra scritta come apice, come indice o racchiuso in un cerchio.</span><span class="sxs-lookup"><span data-stu-id="76131-150">They also combine some characters that might sometimes have a different semantic meaning, such as a digit written as a superscript, as a subscript, or enclosed in a circle.</span></span> <span data-ttu-id="76131-151">A causa di questa perdita di informazioni, i moduli KC e KD in genere non devono essere usati come forme canoniche di stringhe, ma sono utili per alcune applicazioni.</span><span class="sxs-lookup"><span data-stu-id="76131-151">Because of this information loss, forms KC and KD generally should not be used as canonical forms of strings, but they are useful for certain applications.</span></span>

<span data-ttu-id="76131-152">Il formato KC è un formato composto e il formato KD è un formato decomposto.</span><span class="sxs-lookup"><span data-stu-id="76131-152">Form KC is a composed form and form KD is a decomposed form.</span></span> <span data-ttu-id="76131-153">L'applicazione può andare avanti e indietro tra i form KC e KD, ma non esiste un modo coerente per passare dal formato KC o KD alla stringa originale, anche se la stringa originale è nel formato C o D.</span><span class="sxs-lookup"><span data-stu-id="76131-153">The application can go back and forth between forms KC and KD, but there is no consistent way to go from form KC or KD back to the original string, even if the original string is in form C or D.</span></span>

<span data-ttu-id="76131-154">Windows, le applicazioni Microsoft e i .NET Framework in genere generano caratteri nel form C utilizzando i normali metodi di input.</span><span class="sxs-lookup"><span data-stu-id="76131-154">Windows, Microsoft applications, and the .NET Framework generally generate characters in form C using normal input methods.</span></span> <span data-ttu-id="76131-155">Per la maggior parte degli scopi di Windows, form C è il formato preferito.</span><span class="sxs-lookup"><span data-stu-id="76131-155">For most purposes on Windows, form C is the preferred form.</span></span> <span data-ttu-id="76131-156">Ad esempio, i caratteri nel formato C sono prodotti da input da tastiera di Windows.</span><span class="sxs-lookup"><span data-stu-id="76131-156">For example, characters in form C are produced by Windows keyboard input.</span></span> <span data-ttu-id="76131-157">Tuttavia, i caratteri importati dal Web e da altre piattaforme possono introdurre altri moduli di normalizzazione nel flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="76131-157">However, characters imported from the Web and other platforms can introduce other normalization forms into the data stream.</span></span>

<span data-ttu-id="76131-158">Gli esempi seguenti sono tratti da UAX \# 15 e illustrano le differenze tra i quattro moduli di normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="76131-158">The following examples are drawn from UAX \#15, and illustrate the differences among the four normalization forms.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="76131-159">Originale</span><span class="sxs-lookup"><span data-stu-id="76131-159">Original</span></span></th>
<th><span data-ttu-id="76131-160">Form D</span><span class="sxs-lookup"><span data-stu-id="76131-160">Form D</span></span></th>
<th><span data-ttu-id="76131-161">Form C</span><span class="sxs-lookup"><span data-stu-id="76131-161">Form C</span></span></th>
<th><span data-ttu-id="76131-162">Note</span><span class="sxs-lookup"><span data-stu-id="76131-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76131-163">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-163">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="76131-164">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-164">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="76131-165">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-165">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="76131-166">Il ffi_ligature (U + FB03) non è scomposto, perché include un mapping di compatibilità, non un mapping canonico. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="76131-166">The ffi_ligature (U+FB03) is not decomposed, because it has a compatibility mapping, not a canonical mapping.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="76131-167">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-167">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="76131-168">&quot;A\u0308\uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-168">&quot;A\u0308\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="76131-169">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-169">&quot;Ä\uFB03n&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="76131-170">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-170">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="76131-171">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-171">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="76131-172">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-172">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="76131-173">Il numero romano IV (U + 2163) non è scomposto. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="76131-173">The ROMAN NUMERAL IV (U+2163) is not decomposed.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="76131-174">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-174">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="76131-175">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-175">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="76131-176">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-176">&quot;Henry \u2163&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="76131-177">ga</span><span class="sxs-lookup"><span data-stu-id="76131-177">ga</span></span></td>
<td><span data-ttu-id="76131-178">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-178">ka +ten</span></span></td>
<td><span data-ttu-id="76131-179">ga</span><span class="sxs-lookup"><span data-stu-id="76131-179">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="76131-180">Diversi equivalenti di compatibilità di un singolo carattere giapponese non comportano la stessa stringa nel formato C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="76131-180">Different compatibility equivalents of a single Japanese character do not result in the same string in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="76131-181">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-181">ka +ten</span></span></td>
<td><span data-ttu-id="76131-182">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-182">ka +ten</span></span></td>
<td><span data-ttu-id="76131-183">ga</span><span class="sxs-lookup"><span data-stu-id="76131-183">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="76131-184">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="76131-184">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="76131-185">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="76131-185">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="76131-186">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="76131-186">hw_ka +hw_ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="76131-187">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="76131-187">ka +hw_ten</span></span></td>
<td><span data-ttu-id="76131-188">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="76131-188">ka +hw_ten</span></span></td>
<td><span data-ttu-id="76131-189">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="76131-189">ka +hw_ten</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="76131-190">hw_ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-190">hw_ka +ten</span></span></td>
<td><span data-ttu-id="76131-191">hw_ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-191">hw_ka +ten</span></span></td>
<td><span data-ttu-id="76131-192">hw_ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-192">hw_ka +ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="76131-193">Mario</span><span class="sxs-lookup"><span data-stu-id="76131-193">kaks</span></span></td>
<td><span data-ttu-id="76131-194">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="76131-194">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="76131-195">Mario</span><span class="sxs-lookup"><span data-stu-id="76131-195">kaks</span></span></td>
<td><span data-ttu-id="76131-196">Le sillabe hangul vengono mantenute in normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="76131-196">Hangul syllables are maintained under normalization.</span></span><br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="76131-197">Originale</span><span class="sxs-lookup"><span data-stu-id="76131-197">Original</span></span></th>
<th><span data-ttu-id="76131-198">Modulo KD</span><span class="sxs-lookup"><span data-stu-id="76131-198">Form KD</span></span></th>
<th><span data-ttu-id="76131-199">Formato KC</span><span class="sxs-lookup"><span data-stu-id="76131-199">Form KC</span></span></th>
<th><span data-ttu-id="76131-200">Note</span><span class="sxs-lookup"><span data-stu-id="76131-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76131-201">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-201">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="76131-202">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-202">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="76131-203">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-203">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="76131-204">Il ffi_ligature (U + FB03) viene scomposto nel formato KC, ma non nel formato C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="76131-204">The ffi_ligature (U+FB03) is decomposed in form KC, but not in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="76131-205">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-205">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="76131-206">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-206">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="76131-207">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-207">&quot;Äffin&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="76131-208">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-208">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="76131-209">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-209">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="76131-210">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-210">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="76131-211">Le stringhe risultanti sono identiche nel formato KC. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="76131-211">The resulting strings here are identical in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="76131-212">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-212">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="76131-213">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-213">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="76131-214">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="76131-214">&quot;Henry IV&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="76131-215">ga</span><span class="sxs-lookup"><span data-stu-id="76131-215">ga</span></span></td>
<td><span data-ttu-id="76131-216">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-216">ka +ten</span></span></td>
<td><span data-ttu-id="76131-217">ga</span><span class="sxs-lookup"><span data-stu-id="76131-217">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="76131-218">Diversi equivalenti di compatibilità di un singolo carattere giapponese risultano nella stessa stringa nel formato KC. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="76131-218">Different compatibility equivalents of a single Japanese character result in the same string in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="76131-219">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-219">ka +ten</span></span></td>
<td><span data-ttu-id="76131-220">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-220">ka +ten</span></span></td>
<td><span data-ttu-id="76131-221">ga</span><span class="sxs-lookup"><span data-stu-id="76131-221">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="76131-222">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="76131-222">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="76131-223">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-223">ka +ten</span></span></td>
<td><span data-ttu-id="76131-224">ga</span><span class="sxs-lookup"><span data-stu-id="76131-224">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="76131-225">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="76131-225">ka +hw_ten</span></span></td>
<td><span data-ttu-id="76131-226">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-226">ka +ten</span></span></td>
<td><span data-ttu-id="76131-227">ga</span><span class="sxs-lookup"><span data-stu-id="76131-227">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="76131-228">hw_ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-228">hw_ka +ten</span></span></td>
<td><span data-ttu-id="76131-229">Ka + dieci</span><span class="sxs-lookup"><span data-stu-id="76131-229">ka +ten</span></span></td>
<td><span data-ttu-id="76131-230">ga</span><span class="sxs-lookup"><span data-stu-id="76131-230">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="76131-231">Mario</span><span class="sxs-lookup"><span data-stu-id="76131-231">kaks</span></span></td>
<td><span data-ttu-id="76131-232">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="76131-232">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="76131-233">Mario</span><span class="sxs-lookup"><span data-stu-id="76131-233">kaks</span></span></td>
<td><span data-ttu-id="76131-234">Le sillabe hangul vengono mantenute in normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="76131-234">Hangul syllables are maintained under normalization.</span></span> <span data-ttu-id="76131-235">Nelle versioni Unicode precedenti, i caratteri Jamo come KS <sub>f</sub> avevano mapping di compatibilità a k <sub>f</sub> + s <sub>f</sub>.</span><span class="sxs-lookup"><span data-stu-id="76131-235">In earlier Unicode versions, jamo characters like ks <sub>f</sub> had compatibility mappings to k <sub>f</sub> + s <sub>f</sub>.</span></span> <span data-ttu-id="76131-236">Questi mapping sono stati rimossi in 2.1.9 Unicode per garantire la conservazione delle sillabe hangul.</span><span class="sxs-lookup"><span data-stu-id="76131-236">These mappings were removed in Unicode 2.1.9 to ensure that Hangul syllables are maintained.</span></span><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="76131-237">Le due tabelle precedenti hanno un copyright di © 1998-2006 Unicode, Inc. Tutti i diritti riservati.</span><span class="sxs-lookup"><span data-stu-id="76131-237">The two tables above have a copyright of © 1998-2006 Unicode, Inc. All Rights Reserved.</span></span>

 

## <a name="use-composed-forms-for-single-glyphs"></a><span data-ttu-id="76131-238">Usare i moduli composti per i singoli glifi</span><span class="sxs-lookup"><span data-stu-id="76131-238">Use Composed Forms for Single Glyphs</span></span>

<span data-ttu-id="76131-239">Molte sequenze di caratteri che corrispondono a un singolo glifo non hanno forme composte.</span><span class="sxs-lookup"><span data-stu-id="76131-239">Many character sequences that correspond to a single glyph do not have composed forms.</span></span> <span data-ttu-id="76131-240">Anche se normalizzato in base al form C, un singolo glifo visivo o elemento di testo logico può essere composto da più punti di codice Unicode.</span><span class="sxs-lookup"><span data-stu-id="76131-240">Even when normalized by form C, a single visual glyph or logical text element can be composed of multiple Unicode code points.</span></span> <span data-ttu-id="76131-241">Ad esempio, diversi caratteri utilizzati per la scrittura in lituano hanno segni diacritici doppi, perché hanno solo moduli decomposti.</span><span class="sxs-lookup"><span data-stu-id="76131-241">For example, several characters used in writing Lithuanian have double diacritics, as they have only decomposed forms.</span></span> <span data-ttu-id="76131-242">Un esempio è U minuscolo con Macron e tilde ("ū̃", U + 016B U + 0303, dove il primo punto di codice è un U minuscolo con Macron e il secondo è un accento acuto combinato).</span><span class="sxs-lookup"><span data-stu-id="76131-242">An example is lowercase U with macron and tilde ("ū̃", U+016b U+0303, where the first code point is a lowercase U with macron and the second is a combining acute accent).</span></span>

## <a name="example"></a><span data-ttu-id="76131-243">Esempio</span><span class="sxs-lookup"><span data-stu-id="76131-243">Example</span></span>

<span data-ttu-id="76131-244">Un esempio pertinente è disponibile nell' [esempio di normalizzazione NLS: Unicode](nls--unicode-normalization-sample.md).</span><span class="sxs-lookup"><span data-stu-id="76131-244">A relevant example can be found in [NLS: Unicode Normalization Sample](nls--unicode-normalization-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76131-245">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76131-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76131-246">Uso del supporto per le lingue nazionali</span><span class="sxs-lookup"><span data-stu-id="76131-246">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="76131-247">Considerazioni sulla sicurezza: funzionalità internazionali</span><span class="sxs-lookup"><span data-stu-id="76131-247">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> <dt>

[<span data-ttu-id="76131-248">**IsNormalizedString**</span><span class="sxs-lookup"><span data-stu-id="76131-248">**IsNormalizedString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[<span data-ttu-id="76131-249">**NormalizeString**</span><span class="sxs-lookup"><span data-stu-id="76131-249">**NormalizeString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 





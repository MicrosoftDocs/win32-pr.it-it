---
title: Comportamento del fallback del tipo di carattere HTML
description: Comportamento del fallback del tipo di carattere HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300606"
---
# <a name="html-font-fallback-behavior"></a><span data-ttu-id="a854f-103">Comportamento del fallback del tipo di carattere HTML</span><span class="sxs-lookup"><span data-stu-id="a854f-103">HTML font fallback behavior</span></span>

## <a name="platform"></a><span data-ttu-id="a854f-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="a854f-104">Platform</span></span>

<span data-ttu-id="a854f-105">Client-\* \* Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a854f-105">Clients -\*\* Windows 8.1</span></span>  
<span data-ttu-id="a854f-106">**Server-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a854f-106">**Servers -** Windows Server 2012 R2</span></span>  


## <a name="description"></a><span data-ttu-id="a854f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a854f-107">Description</span></span>

<span data-ttu-id="a854f-108">Microsoft sta aggiornando la logica per i tipi di carattere dell'interfaccia utente per diverse lingue nelle app di Windows Store tramite HTML.</span><span class="sxs-lookup"><span data-stu-id="a854f-108">Microsoft is updating the logic for UI fonts for several languages in Windows Store apps using HTML.</span></span> <span data-ttu-id="a854f-109">Invece di usare un solo tipo di carattere per tutte le lingue, il tipo di carattere dell'interfaccia utente ora verrà determinato in base al linguaggio.</span><span class="sxs-lookup"><span data-stu-id="a854f-109">Rather than using a single font for all languages, the UI font will now be determined on a per language basis.</span></span> <span data-ttu-id="a854f-110">Ad esempio, i tipi di carattere dell'interfaccia utente per il giapponese saranno ora Meiryo interfaccia utente nelle app che usano HTML.</span><span class="sxs-lookup"><span data-stu-id="a854f-110">For example, UI fonts for Japanese will now be Meiryo UI in apps that use HTML.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a854f-111">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="a854f-111">Manifestation</span></span>

<span data-ttu-id="a854f-112">Le app che dipendono da un tipo di carattere precedente potrebbero essere diverse; anche se l'aspetto dell'app viene migliorato in generale grazie a tipi di carattere più leggibili, è possibile che si verifichi un problema con i layout che dipendono dalle dimensioni del contenuto in pixel perfetti.</span><span class="sxs-lookup"><span data-stu-id="a854f-112">Apps that depended on an old font may look different; while your app appearance will be improved overall thanks to more readable fonts, there could be an issue with layouts that depend on pixel-perfect content sizes.</span></span> <span data-ttu-id="a854f-113">Ad esempio, alcune righe di contenuto possono essere più grandi di quelle precedentemente, causando interruzioni di riga e/o il ridimensionamento di elementi contenitore imprevisti.</span><span class="sxs-lookup"><span data-stu-id="a854f-113">For example, some lines of content may be bigger than they were previously, causing unexpected line breaks and/or resizing of container elements.</span></span> <span data-ttu-id="a854f-114">In pratica, tuttavia, non sono stati riscontrati problemi con le app esistenti.</span><span class="sxs-lookup"><span data-stu-id="a854f-114">However, in practice we haven’t noticed any issues with any existing apps.</span></span>

## <a name="solution"></a><span data-ttu-id="a854f-115">Soluzione</span><span class="sxs-lookup"><span data-stu-id="a854f-115">Solution</span></span>

<span data-ttu-id="a854f-116">Le app interessate possono attenuare questo comportamento specificando un tipo di carattere specifico tramite CSS (ad esempio, "font-family: Meiryo UI") invece di basarsi sui tipi di carattere predefiniti precedenti.</span><span class="sxs-lookup"><span data-stu-id="a854f-116">Affected apps can mitigate this behavior by specifying a given font via CSS (for example, “font-family: Meiryo UI”) instead of relying on the old default fonts.</span></span> <span data-ttu-id="a854f-117">La tabella seguente fornisce il tipo di carattere dell'interfaccia utente per ogni nome di script.</span><span class="sxs-lookup"><span data-stu-id="a854f-117">The following table provides the UI font for each of the script names.</span></span>



| <span data-ttu-id="a854f-118">Nome script</span><span class="sxs-lookup"><span data-stu-id="a854f-118">Script Name</span></span>        | <span data-ttu-id="a854f-119">Tipo di carattere dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a854f-119">UI Font</span></span>               |
|--------------------|-----------------------|
| <span data-ttu-id="a854f-120">Arabo</span><span class="sxs-lookup"><span data-stu-id="a854f-120">Arabic</span></span>             | <span data-ttu-id="a854f-121">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="a854f-121">Segoe UI</span></span>              |
| <span data-ttu-id="a854f-122">Armeno</span><span class="sxs-lookup"><span data-stu-id="a854f-122">Armenian</span></span>           | <span data-ttu-id="a854f-123">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="a854f-123">Segoe UI</span></span>              |
| <span data-ttu-id="a854f-124">Bengalese</span><span class="sxs-lookup"><span data-stu-id="a854f-124">Bengali</span></span>            | <span data-ttu-id="a854f-125">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-125">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-126">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="a854f-126">Bopomofo</span></span>           | <span data-ttu-id="a854f-127">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="a854f-127">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="a854f-128">Braille</span><span class="sxs-lookup"><span data-stu-id="a854f-128">Braille</span></span>            | <span data-ttu-id="a854f-129">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-129">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-130">Buginese</span><span class="sxs-lookup"><span data-stu-id="a854f-130">Buginese</span></span>           | <span data-ttu-id="a854f-131">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="a854f-131">Leelawadee UI</span></span>         |
| <span data-ttu-id="a854f-132">Sillabico canadese</span><span class="sxs-lookup"><span data-stu-id="a854f-132">Canadian Syllabics</span></span> | <span data-ttu-id="a854f-133">Gadugi</span><span class="sxs-lookup"><span data-stu-id="a854f-133">Gadugi</span></span>                |
| <span data-ttu-id="a854f-134">Cherokee</span><span class="sxs-lookup"><span data-stu-id="a854f-134">Cherokee</span></span>           | <span data-ttu-id="a854f-135">Gadugi</span><span class="sxs-lookup"><span data-stu-id="a854f-135">Gadugi</span></span>                |
| <span data-ttu-id="a854f-136">Copto</span><span class="sxs-lookup"><span data-stu-id="a854f-136">Coptic</span></span>             | <span data-ttu-id="a854f-137">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-137">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-138">Han (semplificato)</span><span class="sxs-lookup"><span data-stu-id="a854f-138">Han (Simplified)</span></span>   | <span data-ttu-id="a854f-139">Microsoft YaHei UI</span><span class="sxs-lookup"><span data-stu-id="a854f-139">Microsoft YaHei UI</span></span>    |
| <span data-ttu-id="a854f-140">Han (tradizionale)</span><span class="sxs-lookup"><span data-stu-id="a854f-140">Han (Traditional)</span></span>  | <span data-ttu-id="a854f-141">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="a854f-141">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="a854f-142">Cirillico</span><span class="sxs-lookup"><span data-stu-id="a854f-142">Cyrillic</span></span>           | <span data-ttu-id="a854f-143">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="a854f-143">Segoe UI</span></span>              |
| <span data-ttu-id="a854f-144">Devanagari</span><span class="sxs-lookup"><span data-stu-id="a854f-144">Devanagari</span></span>         | <span data-ttu-id="a854f-145">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-145">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-146">Deseret</span><span class="sxs-lookup"><span data-stu-id="a854f-146">Deseret</span></span>            | <span data-ttu-id="a854f-147">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-147">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-148">Etiope</span><span class="sxs-lookup"><span data-stu-id="a854f-148">Ethiopic</span></span>           | <span data-ttu-id="a854f-149">Ebrima</span><span class="sxs-lookup"><span data-stu-id="a854f-149">Ebrima</span></span>                |
| <span data-ttu-id="a854f-150">Georgiano</span><span class="sxs-lookup"><span data-stu-id="a854f-150">Georgian</span></span>           | <span data-ttu-id="a854f-151">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="a854f-151">Segoe UI</span></span>              |
| <span data-ttu-id="a854f-152">Glagolitico</span><span class="sxs-lookup"><span data-stu-id="a854f-152">Glagolitic</span></span>         | <span data-ttu-id="a854f-153">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-153">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-154">Gothic</span><span class="sxs-lookup"><span data-stu-id="a854f-154">Gothic</span></span>             | <span data-ttu-id="a854f-155">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-155">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-156">Greco</span><span class="sxs-lookup"><span data-stu-id="a854f-156">Greek</span></span>              | <span data-ttu-id="a854f-157">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="a854f-157">Segoe UI</span></span>              |
| <span data-ttu-id="a854f-158">Gujarati</span><span class="sxs-lookup"><span data-stu-id="a854f-158">Gujarati</span></span>           | <span data-ttu-id="a854f-159">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-159">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-160">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="a854f-160">Gurmukhi</span></span>           | <span data-ttu-id="a854f-161">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-161">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-162">Ebraico</span><span class="sxs-lookup"><span data-stu-id="a854f-162">Hebrew</span></span>             | <span data-ttu-id="a854f-163">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="a854f-163">Segoe UI</span></span>              |
| <span data-ttu-id="a854f-164">Corsivo precedente</span><span class="sxs-lookup"><span data-stu-id="a854f-164">Old Italic</span></span>         | <span data-ttu-id="a854f-165">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-165">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-166">Giavanese</span><span class="sxs-lookup"><span data-stu-id="a854f-166">Javanese</span></span>           | <span data-ttu-id="a854f-167">Testo giavanese</span><span class="sxs-lookup"><span data-stu-id="a854f-167">Javanese Text</span></span>         |
| <span data-ttu-id="a854f-168">Giapponese</span><span class="sxs-lookup"><span data-stu-id="a854f-168">Japanese</span></span>           | <span data-ttu-id="a854f-169">Interfaccia utente di Meiryo</span><span class="sxs-lookup"><span data-stu-id="a854f-169">Meiryo UI</span></span>             |
| <span data-ttu-id="a854f-170">Kannada</span><span class="sxs-lookup"><span data-stu-id="a854f-170">Kannada</span></span>            | <span data-ttu-id="a854f-171">Interfaccia utente di Mirmala</span><span class="sxs-lookup"><span data-stu-id="a854f-171">Mirmala UI</span></span>            |
| <span data-ttu-id="a854f-172">Khmer</span><span class="sxs-lookup"><span data-stu-id="a854f-172">Khmer</span></span>              | <span data-ttu-id="a854f-173">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="a854f-173">Leelawadee UI</span></span>         |
| <span data-ttu-id="a854f-174">Coreano</span><span class="sxs-lookup"><span data-stu-id="a854f-174">Korean</span></span>             | <span data-ttu-id="a854f-175">Malgun Gothic</span><span class="sxs-lookup"><span data-stu-id="a854f-175">Malgun Gothic</span></span>         |
| <span data-ttu-id="a854f-176">Lao</span><span class="sxs-lookup"><span data-stu-id="a854f-176">Lao</span></span>                | <span data-ttu-id="a854f-177">Leelawadee</span><span class="sxs-lookup"><span data-stu-id="a854f-177">Leelawadee</span></span>            |
| <span data-ttu-id="a854f-178">Latino</span><span class="sxs-lookup"><span data-stu-id="a854f-178">Latin</span></span>              | <span data-ttu-id="a854f-179">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="a854f-179">Segoe UI</span></span>              |
| <span data-ttu-id="a854f-180">Malayalam</span><span class="sxs-lookup"><span data-stu-id="a854f-180">Malayalam</span></span>          | <span data-ttu-id="a854f-181">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-181">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-182">Mongolo</span><span class="sxs-lookup"><span data-stu-id="a854f-182">Mongolian</span></span>          | <span data-ttu-id="a854f-183">Mongolian Baiti</span><span class="sxs-lookup"><span data-stu-id="a854f-183">Mongolian Baiti</span></span>       |
| <span data-ttu-id="a854f-184">Myanmar</span><span class="sxs-lookup"><span data-stu-id="a854f-184">Myanmar</span></span>            | <span data-ttu-id="a854f-185">Myanmar Text</span><span class="sxs-lookup"><span data-stu-id="a854f-185">Myanmar Text</span></span>          |
| <span data-ttu-id="a854f-186">Modellazione N'Ko</span><span class="sxs-lookup"><span data-stu-id="a854f-186">N'Ko</span></span>               | <span data-ttu-id="a854f-187">Ebrima</span><span class="sxs-lookup"><span data-stu-id="a854f-187">Ebrima</span></span>                |
| <span data-ttu-id="a854f-188">Ogamico</span><span class="sxs-lookup"><span data-stu-id="a854f-188">Ogham</span></span>              | <span data-ttu-id="a854f-189">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-189">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-190">Chiki OL</span><span class="sxs-lookup"><span data-stu-id="a854f-190">Ol Chiki</span></span>           | <span data-ttu-id="a854f-191">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-191">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-192">Vecchio turco</span><span class="sxs-lookup"><span data-stu-id="a854f-192">Old Turkic</span></span>         | <span data-ttu-id="a854f-193">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-193">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-194">Oriya</span><span class="sxs-lookup"><span data-stu-id="a854f-194">Oriya</span></span>              | <span data-ttu-id="a854f-195">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-195">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-196">Osmanya</span><span class="sxs-lookup"><span data-stu-id="a854f-196">Osmanya</span></span>            | <span data-ttu-id="a854f-197">Ebrima</span><span class="sxs-lookup"><span data-stu-id="a854f-197">Ebrima</span></span>                |
| <span data-ttu-id="a854f-198">Carattere phags-pa</span><span class="sxs-lookup"><span data-stu-id="a854f-198">Phags-pa</span></span>           | <span data-ttu-id="a854f-199">Microsoft PhagsPa</span><span class="sxs-lookup"><span data-stu-id="a854f-199">Microsoft PhagsPa</span></span>     |
| <span data-ttu-id="a854f-200">Runico</span><span class="sxs-lookup"><span data-stu-id="a854f-200">Runic</span></span>              | <span data-ttu-id="a854f-201">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="a854f-201">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="a854f-202">Sora Sompeng</span><span class="sxs-lookup"><span data-stu-id="a854f-202">Sora Sompeng</span></span>       | <span data-ttu-id="a854f-203">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-203">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-204">Singalese</span><span class="sxs-lookup"><span data-stu-id="a854f-204">Sinhala</span></span>            | <span data-ttu-id="a854f-205">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-205">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-206">Siriaco</span><span class="sxs-lookup"><span data-stu-id="a854f-206">Syriac</span></span>             | <span data-ttu-id="a854f-207">Estrangelo Edessa</span><span class="sxs-lookup"><span data-stu-id="a854f-207">Estrangelo Edessa</span></span>     |
| <span data-ttu-id="a854f-208">Tai le</span><span class="sxs-lookup"><span data-stu-id="a854f-208">Tai Le</span></span>             | <span data-ttu-id="a854f-209">Microsoft Tai Le</span><span class="sxs-lookup"><span data-stu-id="a854f-209">Microsoft Tai Le</span></span>      |
| <span data-ttu-id="a854f-210">Nuovo tai lue</span><span class="sxs-lookup"><span data-stu-id="a854f-210">New Tai Lue</span></span>        | <span data-ttu-id="a854f-211">Microsoft New Tai Lue</span><span class="sxs-lookup"><span data-stu-id="a854f-211">Microsoft New Tai Lue</span></span> |
| <span data-ttu-id="a854f-212">Tamil</span><span class="sxs-lookup"><span data-stu-id="a854f-212">Tamil</span></span>              | <span data-ttu-id="a854f-213">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-213">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-214">Telugu</span><span class="sxs-lookup"><span data-stu-id="a854f-214">Telugu</span></span>             | <span data-ttu-id="a854f-215">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="a854f-215">Nirmala UI</span></span>            |
| <span data-ttu-id="a854f-216">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="a854f-216">Tifinagh</span></span>           | <span data-ttu-id="a854f-217">Ebrima</span><span class="sxs-lookup"><span data-stu-id="a854f-217">Ebrima</span></span>                |
| <span data-ttu-id="a854f-218">Thaana</span><span class="sxs-lookup"><span data-stu-id="a854f-218">Thaana</span></span>             | <span data-ttu-id="a854f-219">MV Boli</span><span class="sxs-lookup"><span data-stu-id="a854f-219">MV Boli</span></span>               |
| <span data-ttu-id="a854f-220">Thai</span><span class="sxs-lookup"><span data-stu-id="a854f-220">Thai</span></span>               | <span data-ttu-id="a854f-221">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="a854f-221">Leelawadee UI</span></span>         |
| <span data-ttu-id="a854f-222">Tibetano</span><span class="sxs-lookup"><span data-stu-id="a854f-222">Tibetan</span></span>            | <span data-ttu-id="a854f-223">Microsoft Himalaya</span><span class="sxs-lookup"><span data-stu-id="a854f-223">Microsoft Himalaya</span></span>    |
| <span data-ttu-id="a854f-224">Vai</span><span class="sxs-lookup"><span data-stu-id="a854f-224">Vai</span></span>                | <span data-ttu-id="a854f-225">Ebrima</span><span class="sxs-lookup"><span data-stu-id="a854f-225">Ebrima</span></span>                |
| <span data-ttu-id="a854f-226">Yi</span><span class="sxs-lookup"><span data-stu-id="a854f-226">Yi</span></span>                 | <span data-ttu-id="a854f-227">Microsoft Yi Baiti</span><span class="sxs-lookup"><span data-stu-id="a854f-227">Microsoft Yi Baiti</span></span>    |



 

 

 





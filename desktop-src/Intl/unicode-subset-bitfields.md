---
description: Il subset Unicode campi (USBs) viene utilizzato nelle strutture FONTSIGNATURE e LOCALESIGNATURE.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Campi subset Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314800"
---
# <a name="unicode-subset-bitfields"></a><span data-ttu-id="75ef3-103">Campi subset Unicode</span><span class="sxs-lookup"><span data-stu-id="75ef3-103">Unicode Subset Bitfields</span></span>

<span data-ttu-id="75ef3-104">Il subset Unicode campi (USBs) viene utilizzato nelle strutture [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) e [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .</span><span class="sxs-lookup"><span data-stu-id="75ef3-104">The Unicode subset bitfields (USBs) are used in the [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) and [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) structures.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="75ef3-105">bit</span><span class="sxs-lookup"><span data-stu-id="75ef3-105">Bit</span></span></th>
<th><span data-ttu-id="75ef3-106">Intervallo secondario Unicode</span><span class="sxs-lookup"><span data-stu-id="75ef3-106">Unicode subrange</span></span></th>
<th><span data-ttu-id="75ef3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75ef3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75ef3-108">0</span><span class="sxs-lookup"><span data-stu-id="75ef3-108">0</span></span></td>
<td><span data-ttu-id="75ef3-109">0000 - 007F</span><span class="sxs-lookup"><span data-stu-id="75ef3-109">0000 - 007F</span></span></td>
<td><span data-ttu-id="75ef3-110">Latino di base</span><span class="sxs-lookup"><span data-stu-id="75ef3-110">Basic Latin</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-111">1</span><span class="sxs-lookup"><span data-stu-id="75ef3-111">1</span></span></td>
<td><span data-ttu-id="75ef3-112">0080 - 00FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-112">0080 - 00FF</span></span></td>
<td><span data-ttu-id="75ef3-113">Supplemento Latin 1</span><span class="sxs-lookup"><span data-stu-id="75ef3-113">Latin-1 Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-114">2</span><span class="sxs-lookup"><span data-stu-id="75ef3-114">2</span></span></td>
<td><span data-ttu-id="75ef3-115">0100 - 017F</span><span class="sxs-lookup"><span data-stu-id="75ef3-115">0100 - 017F</span></span></td>
<td><span data-ttu-id="75ef3-116">Latino esteso-A</span><span class="sxs-lookup"><span data-stu-id="75ef3-116">Latin Extended-A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-117">3</span><span class="sxs-lookup"><span data-stu-id="75ef3-117">3</span></span></td>
<td><span data-ttu-id="75ef3-118">0180 - 024F</span><span class="sxs-lookup"><span data-stu-id="75ef3-118">0180 - 024F</span></span></td>
<td><span data-ttu-id="75ef3-119">Latino esteso-B</span><span class="sxs-lookup"><span data-stu-id="75ef3-119">Latin Extended-B</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="75ef3-120">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-120">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-121">0250 - 02AF</span><span class="sxs-lookup"><span data-stu-id="75ef3-121">0250 - 02AF</span></span></td>
<td><span data-ttu-id="75ef3-122">Estensioni IPA</span><span class="sxs-lookup"><span data-stu-id="75ef3-122">IPA Extensions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-123">1D00 - 1D7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-123">1D00 - 1D7F</span></span></td>
<td><span data-ttu-id="75ef3-124">Estensioni fonetiche</span><span class="sxs-lookup"><span data-stu-id="75ef3-124">Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-125">1D80 - 1DBF</span><span class="sxs-lookup"><span data-stu-id="75ef3-125">1D80 - 1DBF</span></span></td>
<td><span data-ttu-id="75ef3-126">Supplemento per le estensioni fonetiche</span><span class="sxs-lookup"><span data-stu-id="75ef3-126">Phonetic Extensions Supplement</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="75ef3-127">5 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-127">5${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-128">02B0 - 02FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-128">02B0 - 02FF</span></span></td>
<td><span data-ttu-id="75ef3-129">Caratteri di modifica spaziatura</span><span class="sxs-lookup"><span data-stu-id="75ef3-129">Spacing Modifier Letters</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-130">A700-A71F</span><span class="sxs-lookup"><span data-stu-id="75ef3-130">A700 - A71F</span></span></td>
<td><span data-ttu-id="75ef3-131">Modifica lettere tono</span><span class="sxs-lookup"><span data-stu-id="75ef3-131">Modifier Tone Letters</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="75ef3-132">6 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-132">6${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-133">0300 - 036F</span><span class="sxs-lookup"><span data-stu-id="75ef3-133">0300 - 036F</span></span></td>
<td><span data-ttu-id="75ef3-134">Combinazione di segni diacritici</span><span class="sxs-lookup"><span data-stu-id="75ef3-134">Combining Diacritical Marks</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-135">1DC0 - 1DFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-135">1DC0 - 1DFF</span></span></td>
<td><span data-ttu-id="75ef3-136">Supplemento segni diacritici combinati</span><span class="sxs-lookup"><span data-stu-id="75ef3-136">Combining Diacritical Marks Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-137">7</span><span class="sxs-lookup"><span data-stu-id="75ef3-137">7</span></span></td>
<td><span data-ttu-id="75ef3-138">0370 - 03FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-138">0370 - 03FF</span></span></td>
<td><span data-ttu-id="75ef3-139">Greco e copto</span><span class="sxs-lookup"><span data-stu-id="75ef3-139">Greek and Coptic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-140">8</span><span class="sxs-lookup"><span data-stu-id="75ef3-140">8</span></span></td>
<td><span data-ttu-id="75ef3-141">2C80 - 2CFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-141">2C80 - 2CFF</span></span></td>
<td><span data-ttu-id="75ef3-142">Copto</span><span class="sxs-lookup"><span data-stu-id="75ef3-142">Coptic</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="75ef3-143">9 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-143">9${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-144">0400 - 04FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-144">0400 - 04FF</span></span></td>
<td><span data-ttu-id="75ef3-145">Cirillico</span><span class="sxs-lookup"><span data-stu-id="75ef3-145">Cyrillic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-146">0500 - 052F</span><span class="sxs-lookup"><span data-stu-id="75ef3-146">0500 - 052F</span></span></td>
<td><span data-ttu-id="75ef3-147">Supplemento cirillico</span><span class="sxs-lookup"><span data-stu-id="75ef3-147">Cyrillic Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-148">2DE0 - 2DFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-148">2DE0 - 2DFF</span></span></td>
<td><span data-ttu-id="75ef3-149">Cirillico esteso-A</span><span class="sxs-lookup"><span data-stu-id="75ef3-149">Cyrillic Extended-A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-150">A640-A69F</span><span class="sxs-lookup"><span data-stu-id="75ef3-150">A640 - A69F</span></span></td>
<td><span data-ttu-id="75ef3-151">Cirillico esteso-B</span><span class="sxs-lookup"><span data-stu-id="75ef3-151">Cyrillic Extended-B</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-152">10</span><span class="sxs-lookup"><span data-stu-id="75ef3-152">10</span></span></td>
<td><span data-ttu-id="75ef3-153">0530 - 058F</span><span class="sxs-lookup"><span data-stu-id="75ef3-153">0530 - 058F</span></span></td>
<td><span data-ttu-id="75ef3-154">Armeno</span><span class="sxs-lookup"><span data-stu-id="75ef3-154">Armenian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-155">11</span><span class="sxs-lookup"><span data-stu-id="75ef3-155">11</span></span></td>
<td><span data-ttu-id="75ef3-156">0590 - 05FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-156">0590 - 05FF</span></span></td>
<td><span data-ttu-id="75ef3-157">Ebraico</span><span class="sxs-lookup"><span data-stu-id="75ef3-157">Hebrew</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-158">12</span><span class="sxs-lookup"><span data-stu-id="75ef3-158">12</span></span></td>
<td><span data-ttu-id="75ef3-159">A500-A63F</span><span class="sxs-lookup"><span data-stu-id="75ef3-159">A500 - A63F</span></span></td>
<td><span data-ttu-id="75ef3-160">Vai</span><span class="sxs-lookup"><span data-stu-id="75ef3-160">Vai</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="75ef3-161">13 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-161">13${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-162">0600 - 06FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-162">0600 - 06FF</span></span></td>
<td><span data-ttu-id="75ef3-163">Arabo</span><span class="sxs-lookup"><span data-stu-id="75ef3-163">Arabic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-164">0750-077F</span><span class="sxs-lookup"><span data-stu-id="75ef3-164">0750 - 077F</span></span></td>
<td><span data-ttu-id="75ef3-165">Supplemento arabo</span><span class="sxs-lookup"><span data-stu-id="75ef3-165">Arabic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-166">14</span><span class="sxs-lookup"><span data-stu-id="75ef3-166">14</span></span></td>
<td><span data-ttu-id="75ef3-167">07C0 - 07FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-167">07C0 - 07FF</span></span></td>
<td><span data-ttu-id="75ef3-168">NKo</span><span class="sxs-lookup"><span data-stu-id="75ef3-168">NKo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-169">15</span><span class="sxs-lookup"><span data-stu-id="75ef3-169">15</span></span></td>
<td><span data-ttu-id="75ef3-170">0900 - 097F</span><span class="sxs-lookup"><span data-stu-id="75ef3-170">0900 - 097F</span></span></td>
<td><span data-ttu-id="75ef3-171">Devanagari</span><span class="sxs-lookup"><span data-stu-id="75ef3-171">Devanagari</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-172">16</span><span class="sxs-lookup"><span data-stu-id="75ef3-172">16</span></span></td>
<td><span data-ttu-id="75ef3-173">0980 - 09FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-173">0980 - 09FF</span></span></td>
<td><span data-ttu-id="75ef3-174">Bengalese</span><span class="sxs-lookup"><span data-stu-id="75ef3-174">Bangla</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-175">17</span><span class="sxs-lookup"><span data-stu-id="75ef3-175">17</span></span></td>
<td><span data-ttu-id="75ef3-176">0A00 - 0A7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-176">0A00 - 0A7F</span></span></td>
<td><span data-ttu-id="75ef3-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="75ef3-177">Gurmukhi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-178">18</span><span class="sxs-lookup"><span data-stu-id="75ef3-178">18</span></span></td>
<td><span data-ttu-id="75ef3-179">0A80 - 0AFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-179">0A80 - 0AFF</span></span></td>
<td><span data-ttu-id="75ef3-180">Gujarati</span><span class="sxs-lookup"><span data-stu-id="75ef3-180">Gujarati</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-181">19</span><span class="sxs-lookup"><span data-stu-id="75ef3-181">19</span></span></td>
<td><span data-ttu-id="75ef3-182">0B00 - 0B7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-182">0B00 - 0B7F</span></span></td>
<td><span data-ttu-id="75ef3-183">Odia</span><span class="sxs-lookup"><span data-stu-id="75ef3-183">Odia</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-184">20</span><span class="sxs-lookup"><span data-stu-id="75ef3-184">20</span></span></td>
<td><span data-ttu-id="75ef3-185">0B80 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-185">0B80 - 0BFF</span></span></td>
<td><span data-ttu-id="75ef3-186">Tamil</span><span class="sxs-lookup"><span data-stu-id="75ef3-186">Tamil</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-187">21</span><span class="sxs-lookup"><span data-stu-id="75ef3-187">21</span></span></td>
<td><span data-ttu-id="75ef3-188">0C00 - 0C7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-188">0C00 - 0C7F</span></span></td>
<td><span data-ttu-id="75ef3-189">Telugu</span><span class="sxs-lookup"><span data-stu-id="75ef3-189">Telugu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-190">22</span><span class="sxs-lookup"><span data-stu-id="75ef3-190">22</span></span></td>
<td><span data-ttu-id="75ef3-191">0C80 - 0CFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-191">0C80 - 0CFF</span></span></td>
<td><span data-ttu-id="75ef3-192">Kannada</span><span class="sxs-lookup"><span data-stu-id="75ef3-192">Kannada</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-193">23</span><span class="sxs-lookup"><span data-stu-id="75ef3-193">23</span></span></td>
<td><span data-ttu-id="75ef3-194">0D00 - 0D7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-194">0D00 - 0D7F</span></span></td>
<td><span data-ttu-id="75ef3-195">Malayalam</span><span class="sxs-lookup"><span data-stu-id="75ef3-195">Malayalam</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-196">24</span><span class="sxs-lookup"><span data-stu-id="75ef3-196">24</span></span></td>
<td><span data-ttu-id="75ef3-197">0E00 - 0E7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-197">0E00 - 0E7F</span></span></td>
<td><span data-ttu-id="75ef3-198">Thai</span><span class="sxs-lookup"><span data-stu-id="75ef3-198">Thai</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-199">25</span><span class="sxs-lookup"><span data-stu-id="75ef3-199">25</span></span></td>
<td><span data-ttu-id="75ef3-200">0E80 - 0EFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-200">0E80 - 0EFF</span></span></td>
<td><span data-ttu-id="75ef3-201">Lao</span><span class="sxs-lookup"><span data-stu-id="75ef3-201">Lao</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="75ef3-202">26 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-202">26${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-203">10A0 - 10FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-203">10A0 - 10FF</span></span></td>
<td><span data-ttu-id="75ef3-204">Georgiano</span><span class="sxs-lookup"><span data-stu-id="75ef3-204">Georgian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-205">2D00 - 2D2F</span><span class="sxs-lookup"><span data-stu-id="75ef3-205">2D00 - 2D2F</span></span></td>
<td><span data-ttu-id="75ef3-206">Supplemento georgiano</span><span class="sxs-lookup"><span data-stu-id="75ef3-206">Georgian Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-207">27</span><span class="sxs-lookup"><span data-stu-id="75ef3-207">27</span></span></td>
<td><span data-ttu-id="75ef3-208">1B00 - 1B7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-208">1B00 - 1B7F</span></span></td>
<td><span data-ttu-id="75ef3-209">Balinese</span><span class="sxs-lookup"><span data-stu-id="75ef3-209">Balinese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-210">28</span><span class="sxs-lookup"><span data-stu-id="75ef3-210">28</span></span></td>
<td><span data-ttu-id="75ef3-211">1100 - 11FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-211">1100 - 11FF</span></span></td>
<td><span data-ttu-id="75ef3-212">Jamo hangul</span><span class="sxs-lookup"><span data-stu-id="75ef3-212">Hangul Jamo</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="75ef3-213">29 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-213">29${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-214">1E00 - 1EFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-214">1E00 - 1EFF</span></span></td>
<td><span data-ttu-id="75ef3-215">Informazioni aggiuntive sull'estensione Latin</span><span class="sxs-lookup"><span data-stu-id="75ef3-215">Latin Extended Additional</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-216">2C60 - 2C7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-216">2C60 - 2C7F</span></span></td>
<td><span data-ttu-id="75ef3-217">Latino esteso-C</span><span class="sxs-lookup"><span data-stu-id="75ef3-217">Latin Extended-C</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-218">A720-A7FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-218">A720 - A7FF</span></span></td>
<td><span data-ttu-id="75ef3-219">Latino esteso D</span><span class="sxs-lookup"><span data-stu-id="75ef3-219">Latin Extended-D</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-220">30</span><span class="sxs-lookup"><span data-stu-id="75ef3-220">30</span></span></td>
<td><span data-ttu-id="75ef3-221">1F00 - 1FFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-221">1F00 - 1FFF</span></span></td>
<td><span data-ttu-id="75ef3-222">Greco esteso</span><span class="sxs-lookup"><span data-stu-id="75ef3-222">Greek Extended</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="75ef3-223">31 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-223">31${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-224">2000 - 206F</span><span class="sxs-lookup"><span data-stu-id="75ef3-224">2000 - 206F</span></span></td>
<td><span data-ttu-id="75ef3-225">Punteggiatura generale</span><span class="sxs-lookup"><span data-stu-id="75ef3-225">General Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-226">2E00 - 2E7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-226">2E00 - 2E7F</span></span></td>
<td><span data-ttu-id="75ef3-227">Punteggiatura supplementare</span><span class="sxs-lookup"><span data-stu-id="75ef3-227">Supplemental Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-228">32</span><span class="sxs-lookup"><span data-stu-id="75ef3-228">32</span></span></td>
<td><span data-ttu-id="75ef3-229">2070 - 209F</span><span class="sxs-lookup"><span data-stu-id="75ef3-229">2070 - 209F</span></span></td>
<td><span data-ttu-id="75ef3-230">Apici e pedici</span><span class="sxs-lookup"><span data-stu-id="75ef3-230">Superscripts And Subscripts</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-231">33</span><span class="sxs-lookup"><span data-stu-id="75ef3-231">33</span></span></td>
<td><span data-ttu-id="75ef3-232">20A0 - 20CF</span><span class="sxs-lookup"><span data-stu-id="75ef3-232">20A0 - 20CF</span></span></td>
<td><span data-ttu-id="75ef3-233">Simboli di valuta</span><span class="sxs-lookup"><span data-stu-id="75ef3-233">Currency Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-234">34</span><span class="sxs-lookup"><span data-stu-id="75ef3-234">34</span></span></td>
<td><span data-ttu-id="75ef3-235">20D0 - 20FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-235">20D0 - 20FF</span></span></td>
<td><span data-ttu-id="75ef3-236">Combinazione di segni diacritici per i simboli</span><span class="sxs-lookup"><span data-stu-id="75ef3-236">Combining Diacritical Marks For Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-237">35</span><span class="sxs-lookup"><span data-stu-id="75ef3-237">35</span></span></td>
<td><span data-ttu-id="75ef3-238">2100 - 214F</span><span class="sxs-lookup"><span data-stu-id="75ef3-238">2100 - 214F</span></span></td>
<td><span data-ttu-id="75ef3-239">Simboli alfabetici</span><span class="sxs-lookup"><span data-stu-id="75ef3-239">Letterlike Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-240">36</span><span class="sxs-lookup"><span data-stu-id="75ef3-240">36</span></span></td>
<td><span data-ttu-id="75ef3-241">2150 - 218F</span><span class="sxs-lookup"><span data-stu-id="75ef3-241">2150 - 218F</span></span></td>
<td><span data-ttu-id="75ef3-242">Formati numerici</span><span class="sxs-lookup"><span data-stu-id="75ef3-242">Number Forms</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="75ef3-243">37 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-243">37${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-244">2190 - 21FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-244">2190 - 21FF</span></span></td>
<td><span data-ttu-id="75ef3-245">Frecce</span><span class="sxs-lookup"><span data-stu-id="75ef3-245">Arrows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-246">27F0 - 27FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-246">27F0 - 27FF</span></span></td>
<td><span data-ttu-id="75ef3-247">Frecce aggiuntive-A</span><span class="sxs-lookup"><span data-stu-id="75ef3-247">Supplemental Arrows-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-248">2900 - 297F</span><span class="sxs-lookup"><span data-stu-id="75ef3-248">2900 - 297F</span></span></td>
<td><span data-ttu-id="75ef3-249">Frecce aggiuntive-B</span><span class="sxs-lookup"><span data-stu-id="75ef3-249">Supplemental Arrows-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-250">2B00 - 2BFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-250">2B00 - 2BFF</span></span></td>
<td><span data-ttu-id="75ef3-251">Simboli e frecce varie</span><span class="sxs-lookup"><span data-stu-id="75ef3-251">Miscellaneous Symbols and Arrows</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="75ef3-252">38 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-252">38${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-253">2200 - 22FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-253">2200 - 22FF</span></span></td>
<td><span data-ttu-id="75ef3-254">Operatori matematici</span><span class="sxs-lookup"><span data-stu-id="75ef3-254">Mathematical Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-255">27C0 - 27EF</span><span class="sxs-lookup"><span data-stu-id="75ef3-255">27C0 - 27EF</span></span></td>
<td><span data-ttu-id="75ef3-256">Simboli matematici vari-A</span><span class="sxs-lookup"><span data-stu-id="75ef3-256">Miscellaneous Mathematical Symbols-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-257">2980 - 29FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-257">2980 - 29FF</span></span></td>
<td><span data-ttu-id="75ef3-258">Simboli matematici vari-B</span><span class="sxs-lookup"><span data-stu-id="75ef3-258">Miscellaneous Mathematical Symbols-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-259">2A00 - 2AFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-259">2A00 - 2AFF</span></span></td>
<td><span data-ttu-id="75ef3-260">Operatori matematici supplementari</span><span class="sxs-lookup"><span data-stu-id="75ef3-260">Supplemental Mathematical Operators</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-261">39</span><span class="sxs-lookup"><span data-stu-id="75ef3-261">39</span></span></td>
<td><span data-ttu-id="75ef3-262">2300 - 23FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-262">2300 - 23FF</span></span></td>
<td><span data-ttu-id="75ef3-263">Varie tecniche</span><span class="sxs-lookup"><span data-stu-id="75ef3-263">Miscellaneous Technical</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-264">40</span><span class="sxs-lookup"><span data-stu-id="75ef3-264">40</span></span></td>
<td><span data-ttu-id="75ef3-265">2400 - 243F</span><span class="sxs-lookup"><span data-stu-id="75ef3-265">2400 - 243F</span></span></td>
<td><span data-ttu-id="75ef3-266">Controllare le immagini</span><span class="sxs-lookup"><span data-stu-id="75ef3-266">Control Pictures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-267">41</span><span class="sxs-lookup"><span data-stu-id="75ef3-267">41</span></span></td>
<td><span data-ttu-id="75ef3-268">2440 - 245F</span><span class="sxs-lookup"><span data-stu-id="75ef3-268">2440 - 245F</span></span></td>
<td><span data-ttu-id="75ef3-269">Riconoscimento ottico di caratteri</span><span class="sxs-lookup"><span data-stu-id="75ef3-269">Optical Character Recognition</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-270">42</span><span class="sxs-lookup"><span data-stu-id="75ef3-270">42</span></span></td>
<td><span data-ttu-id="75ef3-271">2460 - 24FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-271">2460 - 24FF</span></span></td>
<td><span data-ttu-id="75ef3-272">Caratteri alfanumerici racchiusi</span><span class="sxs-lookup"><span data-stu-id="75ef3-272">Enclosed Alphanumerics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-273">43</span><span class="sxs-lookup"><span data-stu-id="75ef3-273">43</span></span></td>
<td><span data-ttu-id="75ef3-274">2500 - 257F</span><span class="sxs-lookup"><span data-stu-id="75ef3-274">2500 - 257F</span></span></td>
<td><span data-ttu-id="75ef3-275">Disegno box</span><span class="sxs-lookup"><span data-stu-id="75ef3-275">Box Drawing</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-276">44</span><span class="sxs-lookup"><span data-stu-id="75ef3-276">44</span></span></td>
<td><span data-ttu-id="75ef3-277">2580 - 259F</span><span class="sxs-lookup"><span data-stu-id="75ef3-277">2580 - 259F</span></span></td>
<td><span data-ttu-id="75ef3-278">Elementi Block</span><span class="sxs-lookup"><span data-stu-id="75ef3-278">Block Elements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-279">45</span><span class="sxs-lookup"><span data-stu-id="75ef3-279">45</span></span></td>
<td><span data-ttu-id="75ef3-280">25A0 - 25FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-280">25A0 - 25FF</span></span></td>
<td><span data-ttu-id="75ef3-281">Forme geometriche</span><span class="sxs-lookup"><span data-stu-id="75ef3-281">Geometric Shapes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-282">46</span><span class="sxs-lookup"><span data-stu-id="75ef3-282">46</span></span></td>
<td><span data-ttu-id="75ef3-283">2600 - 26FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-283">2600 - 26FF</span></span></td>
<td><span data-ttu-id="75ef3-284">Simboli vari</span><span class="sxs-lookup"><span data-stu-id="75ef3-284">Miscellaneous Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-285">47</span><span class="sxs-lookup"><span data-stu-id="75ef3-285">47</span></span></td>
<td><span data-ttu-id="75ef3-286">2700 - 27BF</span><span class="sxs-lookup"><span data-stu-id="75ef3-286">2700 - 27BF</span></span></td>
<td><span data-ttu-id="75ef3-287">Dingbat</span><span class="sxs-lookup"><span data-stu-id="75ef3-287">Dingbats</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-288">48</span><span class="sxs-lookup"><span data-stu-id="75ef3-288">48</span></span></td>
<td><span data-ttu-id="75ef3-289">3000 - 303F</span><span class="sxs-lookup"><span data-stu-id="75ef3-289">3000 - 303F</span></span></td>
<td><span data-ttu-id="75ef3-290">Simboli e punteggiatura CJK</span><span class="sxs-lookup"><span data-stu-id="75ef3-290">CJK Symbols And Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-291">49</span><span class="sxs-lookup"><span data-stu-id="75ef3-291">49</span></span></td>
<td><span data-ttu-id="75ef3-292">3040 - 309F</span><span class="sxs-lookup"><span data-stu-id="75ef3-292">3040 - 309F</span></span></td>
<td><span data-ttu-id="75ef3-293">Hiragana</span><span class="sxs-lookup"><span data-stu-id="75ef3-293">Hiragana</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="75ef3-294">50 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-294">50${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-295">30A0 - 30FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-295">30A0 - 30FF</span></span></td>
<td><span data-ttu-id="75ef3-296">Katakana</span><span class="sxs-lookup"><span data-stu-id="75ef3-296">Katakana</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-297">31F0 - 31FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-297">31F0 - 31FF</span></span></td>
<td><span data-ttu-id="75ef3-298">Estensioni fonetiche katakana</span><span class="sxs-lookup"><span data-stu-id="75ef3-298">Katakana Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="75ef3-299">51 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-299">51${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-300">3100 - 312F</span><span class="sxs-lookup"><span data-stu-id="75ef3-300">3100 - 312F</span></span></td>
<td><span data-ttu-id="75ef3-301">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="75ef3-301">Bopomofo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-302">31A0 - 31BF</span><span class="sxs-lookup"><span data-stu-id="75ef3-302">31A0 - 31BF</span></span></td>
<td><span data-ttu-id="75ef3-303">Bopomofo esteso</span><span class="sxs-lookup"><span data-stu-id="75ef3-303">Bopomofo Extended</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-304">52</span><span class="sxs-lookup"><span data-stu-id="75ef3-304">52</span></span></td>
<td><span data-ttu-id="75ef3-305">3130 - 318F</span><span class="sxs-lookup"><span data-stu-id="75ef3-305">3130 - 318F</span></span></td>
<td><span data-ttu-id="75ef3-306">Compatibilità Hangul Jamo</span><span class="sxs-lookup"><span data-stu-id="75ef3-306">Hangul Compatibility Jamo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-307">53</span><span class="sxs-lookup"><span data-stu-id="75ef3-307">53</span></span></td>
<td><span data-ttu-id="75ef3-308">A840 - A87F</span><span class="sxs-lookup"><span data-stu-id="75ef3-308">A840 - A87F</span></span></td>
<td><span data-ttu-id="75ef3-309">Carattere phags-pa</span><span class="sxs-lookup"><span data-stu-id="75ef3-309">Phags-pa</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-310">54</span><span class="sxs-lookup"><span data-stu-id="75ef3-310">54</span></span></td>
<td><span data-ttu-id="75ef3-311">3200 - 32FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-311">3200 - 32FF</span></span></td>
<td><span data-ttu-id="75ef3-312">Lettere e mesi CJK racchiusi</span><span class="sxs-lookup"><span data-stu-id="75ef3-312">Enclosed CJK Letters And Months</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-313">55</span><span class="sxs-lookup"><span data-stu-id="75ef3-313">55</span></span></td>
<td><span data-ttu-id="75ef3-314">3300 - 33FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-314">3300 - 33FF</span></span></td>
<td><span data-ttu-id="75ef3-315">Compatibilità con CJK</span><span class="sxs-lookup"><span data-stu-id="75ef3-315">CJK Compatibility</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-316">56</span><span class="sxs-lookup"><span data-stu-id="75ef3-316">56</span></span></td>
<td><span data-ttu-id="75ef3-317">AC00 - D7AF</span><span class="sxs-lookup"><span data-stu-id="75ef3-317">AC00 - D7AF</span></span></td>
<td><span data-ttu-id="75ef3-318">Sillabe hangul</span><span class="sxs-lookup"><span data-stu-id="75ef3-318">Hangul Syllables</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-319">57</span><span class="sxs-lookup"><span data-stu-id="75ef3-319">57</span></span></td>
<td><span data-ttu-id="75ef3-320">D800-DFFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-320">D800 - DFFF</span></span></td>
<td><span data-ttu-id="75ef3-321">Non piano 0.</span><span class="sxs-lookup"><span data-stu-id="75ef3-321">Non-Plane 0.</span></span> <span data-ttu-id="75ef3-322">Si noti che l'impostazione di questo bit implica che esiste almeno un punto di codice supplementare oltre il piano multilingue di base (BMP) supportato da questo tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="75ef3-322">Note that setting this bit implies that there is at least one supplementary code point beyond the Basic Multilingual Plane (BMP) that is supported by this font.</span></span> <span data-ttu-id="75ef3-323">Vedere <a href="surrogates-and-supplementary-characters.md">surrogati e caratteri supplementari</a>.</span><span class="sxs-lookup"><span data-stu-id="75ef3-323">See <a href="surrogates-and-supplementary-characters.md">Surrogates and Supplementary Characters</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-324">58</span><span class="sxs-lookup"><span data-stu-id="75ef3-324">58</span></span></td>
<td><span data-ttu-id="75ef3-325">10900-1091F</span><span class="sxs-lookup"><span data-stu-id="75ef3-325">10900 - 1091F</span></span></td>
<td><span data-ttu-id="75ef3-326">Fenicio</span><span class="sxs-lookup"><span data-stu-id="75ef3-326">Phoenician</span></span></td>
</tr>
<tr class="even">
<td rowspan="7"><span data-ttu-id="75ef3-327">59 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-327">59${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-328">2E80 - 2EFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-328">2E80 - 2EFF</span></span></td>
<td><span data-ttu-id="75ef3-329">Complemento ai radicali CJK</span><span class="sxs-lookup"><span data-stu-id="75ef3-329">CJK Radicals Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-330">2F00 - 2FDF</span><span class="sxs-lookup"><span data-stu-id="75ef3-330">2F00 - 2FDF</span></span></td>
<td><span data-ttu-id="75ef3-331">Radicali Kangxi</span><span class="sxs-lookup"><span data-stu-id="75ef3-331">Kangxi Radicals</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-332">2FF0 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-332">2FF0 - 2FFF</span></span></td>
<td><span data-ttu-id="75ef3-333">Caratteri di descrizione ideogrammi</span><span class="sxs-lookup"><span data-stu-id="75ef3-333">Ideographic Description Characters</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-334">3190 - 319F</span><span class="sxs-lookup"><span data-stu-id="75ef3-334">3190 - 319F</span></span></td>
<td><span data-ttu-id="75ef3-335">Kanbun</span><span class="sxs-lookup"><span data-stu-id="75ef3-335">Kanbun</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-336">3400 - 4DBF</span><span class="sxs-lookup"><span data-stu-id="75ef3-336">3400 - 4DBF</span></span></td>
<td><span data-ttu-id="75ef3-337">Ideogrammi Unificati CJK estensione A</span><span class="sxs-lookup"><span data-stu-id="75ef3-337">CJK Unified Ideographs Extension A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-338">4E00 - 9FFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-338">4E00 - 9FFF</span></span></td>
<td><span data-ttu-id="75ef3-339">Ideogrammi Unificati CJK</span><span class="sxs-lookup"><span data-stu-id="75ef3-339">CJK Unified Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-340">20000-2A6DF</span><span class="sxs-lookup"><span data-stu-id="75ef3-340">20000 - 2A6DF</span></span></td>
<td><span data-ttu-id="75ef3-341">CJK Unified ideogrammi Extension B</span><span class="sxs-lookup"><span data-stu-id="75ef3-341">CJK Unified Ideographs Extension B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-342">60</span><span class="sxs-lookup"><span data-stu-id="75ef3-342">60</span></span></td>
<td><span data-ttu-id="75ef3-343">E000 - F8FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-343">E000 - F8FF</span></span></td>
<td><span data-ttu-id="75ef3-344">Area uso privato</span><span class="sxs-lookup"><span data-stu-id="75ef3-344">Private Use Area</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="75ef3-345">61 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-345">61${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-346">31C0 - 31EF</span><span class="sxs-lookup"><span data-stu-id="75ef3-346">31C0 - 31EF</span></span></td>
<td><span data-ttu-id="75ef3-347">Tratti CJK</span><span class="sxs-lookup"><span data-stu-id="75ef3-347">CJK Strokes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-348">F900 - FAFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-348">F900 - FAFF</span></span></td>
<td><span data-ttu-id="75ef3-349">Ideogrammi di compatibilità CJK</span><span class="sxs-lookup"><span data-stu-id="75ef3-349">CJK Compatibility Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-350">2F800 - 2FA1F</span><span class="sxs-lookup"><span data-stu-id="75ef3-350">2F800 - 2FA1F</span></span></td>
<td><span data-ttu-id="75ef3-351">Complemento ideogrammi compatibilità CJK</span><span class="sxs-lookup"><span data-stu-id="75ef3-351">CJK Compatibility Ideographs Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-352">62</span><span class="sxs-lookup"><span data-stu-id="75ef3-352">62</span></span></td>
<td><span data-ttu-id="75ef3-353">FB00 - FB4F</span><span class="sxs-lookup"><span data-stu-id="75ef3-353">FB00 - FB4F</span></span></td>
<td><span data-ttu-id="75ef3-354">Moduli di presentazione alfabetica</span><span class="sxs-lookup"><span data-stu-id="75ef3-354">Alphabetic Presentation Forms</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-355">63</span><span class="sxs-lookup"><span data-stu-id="75ef3-355">63</span></span></td>
<td><span data-ttu-id="75ef3-356">FB50 - FDFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-356">FB50 - FDFF</span></span></td>
<td><span data-ttu-id="75ef3-357">Moduli di presentazione araba-A</span><span class="sxs-lookup"><span data-stu-id="75ef3-357">Arabic Presentation Forms-A</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-358">64</span><span class="sxs-lookup"><span data-stu-id="75ef3-358">64</span></span></td>
<td><span data-ttu-id="75ef3-359">FE20 - FE2F</span><span class="sxs-lookup"><span data-stu-id="75ef3-359">FE20 - FE2F</span></span></td>
<td><span data-ttu-id="75ef3-360">Combinazione di metà segni</span><span class="sxs-lookup"><span data-stu-id="75ef3-360">Combining Half Marks</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="75ef3-361">65 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-361">65${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-362">FE10 - FE1F</span><span class="sxs-lookup"><span data-stu-id="75ef3-362">FE10 - FE1F</span></span></td>
<td><span data-ttu-id="75ef3-363">Moduli verticali</span><span class="sxs-lookup"><span data-stu-id="75ef3-363">Vertical Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-364">FE30 - FE4F</span><span class="sxs-lookup"><span data-stu-id="75ef3-364">FE30 - FE4F</span></span></td>
<td><span data-ttu-id="75ef3-365">Moduli per la compatibilità con CJK</span><span class="sxs-lookup"><span data-stu-id="75ef3-365">CJK Compatibility Forms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-366">66</span><span class="sxs-lookup"><span data-stu-id="75ef3-366">66</span></span></td>
<td><span data-ttu-id="75ef3-367">FE50 - FE6F</span><span class="sxs-lookup"><span data-stu-id="75ef3-367">FE50 - FE6F</span></span></td>
<td><span data-ttu-id="75ef3-368">Varianti di formato ridotto</span><span class="sxs-lookup"><span data-stu-id="75ef3-368">Small Form Variants</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-369">67</span><span class="sxs-lookup"><span data-stu-id="75ef3-369">67</span></span></td>
<td><span data-ttu-id="75ef3-370">FE70 - FEFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-370">FE70 - FEFF</span></span></td>
<td><span data-ttu-id="75ef3-371">Moduli per la presentazione araba-B</span><span class="sxs-lookup"><span data-stu-id="75ef3-371">Arabic Presentation Forms-B</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-372">68</span><span class="sxs-lookup"><span data-stu-id="75ef3-372">68</span></span></td>
<td><span data-ttu-id="75ef3-373">FF00 - FFEF</span><span class="sxs-lookup"><span data-stu-id="75ef3-373">FF00 - FFEF</span></span></td>
<td><span data-ttu-id="75ef3-374">Moduli carattere e fullwidth</span><span class="sxs-lookup"><span data-stu-id="75ef3-374">Halfwidth And Fullwidth Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-375">69</span><span class="sxs-lookup"><span data-stu-id="75ef3-375">69</span></span></td>
<td><span data-ttu-id="75ef3-376">FFF0 - FFFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-376">FFF0 - FFFF</span></span></td>
<td><span data-ttu-id="75ef3-377">Speciali</span><span class="sxs-lookup"><span data-stu-id="75ef3-377">Specials</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-378">70</span><span class="sxs-lookup"><span data-stu-id="75ef3-378">70</span></span></td>
<td><span data-ttu-id="75ef3-379">0F00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-379">0F00 - 0FFF</span></span></td>
<td><span data-ttu-id="75ef3-380">Tibetano</span><span class="sxs-lookup"><span data-stu-id="75ef3-380">Tibetan</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-381">71</span><span class="sxs-lookup"><span data-stu-id="75ef3-381">71</span></span></td>
<td><span data-ttu-id="75ef3-382">0700 - 074F</span><span class="sxs-lookup"><span data-stu-id="75ef3-382">0700 - 074F</span></span></td>
<td><span data-ttu-id="75ef3-383">Siriaco</span><span class="sxs-lookup"><span data-stu-id="75ef3-383">Syriac</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-384">72</span><span class="sxs-lookup"><span data-stu-id="75ef3-384">72</span></span></td>
<td><span data-ttu-id="75ef3-385">0780 - 07BF</span><span class="sxs-lookup"><span data-stu-id="75ef3-385">0780 - 07BF</span></span></td>
<td><span data-ttu-id="75ef3-386">Thaana</span><span class="sxs-lookup"><span data-stu-id="75ef3-386">Thaana</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-387">73</span><span class="sxs-lookup"><span data-stu-id="75ef3-387">73</span></span></td>
<td><span data-ttu-id="75ef3-388">0D80 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-388">0D80 - 0DFF</span></span></td>
<td><span data-ttu-id="75ef3-389">Singalese</span><span class="sxs-lookup"><span data-stu-id="75ef3-389">Sinhala</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-390">74</span><span class="sxs-lookup"><span data-stu-id="75ef3-390">74</span></span></td>
<td><span data-ttu-id="75ef3-391">1000 - 109F</span><span class="sxs-lookup"><span data-stu-id="75ef3-391">1000 - 109F</span></span></td>
<td><span data-ttu-id="75ef3-392">Myanmar</span><span class="sxs-lookup"><span data-stu-id="75ef3-392">Myanmar</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="75ef3-393">75 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-393">75${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-394">1200 - 137F</span><span class="sxs-lookup"><span data-stu-id="75ef3-394">1200 - 137F</span></span></td>
<td><span data-ttu-id="75ef3-395">Etiope</span><span class="sxs-lookup"><span data-stu-id="75ef3-395">Ethiopic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-396">1380-139F</span><span class="sxs-lookup"><span data-stu-id="75ef3-396">1380 - 139F</span></span></td>
<td><span data-ttu-id="75ef3-397">Supplemento etiope</span><span class="sxs-lookup"><span data-stu-id="75ef3-397">Ethiopic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-398">2D80 - 2DDF</span><span class="sxs-lookup"><span data-stu-id="75ef3-398">2D80 - 2DDF</span></span></td>
<td><span data-ttu-id="75ef3-399">Etiope esteso</span><span class="sxs-lookup"><span data-stu-id="75ef3-399">Ethiopic Extended</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-400">76</span><span class="sxs-lookup"><span data-stu-id="75ef3-400">76</span></span></td>
<td><span data-ttu-id="75ef3-401">13A0 - 13FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-401">13A0 - 13FF</span></span></td>
<td><span data-ttu-id="75ef3-402">Cherokee</span><span class="sxs-lookup"><span data-stu-id="75ef3-402">Cherokee</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-403">77</span><span class="sxs-lookup"><span data-stu-id="75ef3-403">77</span></span></td>
<td><span data-ttu-id="75ef3-404">1400 - 167F</span><span class="sxs-lookup"><span data-stu-id="75ef3-404">1400 - 167F</span></span></td>
<td><span data-ttu-id="75ef3-405">Sillabico aborigeno canadese unificato</span><span class="sxs-lookup"><span data-stu-id="75ef3-405">Unified Canadian Aboriginal Syllabics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-406">78</span><span class="sxs-lookup"><span data-stu-id="75ef3-406">78</span></span></td>
<td><span data-ttu-id="75ef3-407">1680 - 169F</span><span class="sxs-lookup"><span data-stu-id="75ef3-407">1680 - 169F</span></span></td>
<td><span data-ttu-id="75ef3-408">Ogamico</span><span class="sxs-lookup"><span data-stu-id="75ef3-408">Ogham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-409">79</span><span class="sxs-lookup"><span data-stu-id="75ef3-409">79</span></span></td>
<td><span data-ttu-id="75ef3-410">16A0 - 16FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-410">16A0 - 16FF</span></span></td>
<td><span data-ttu-id="75ef3-411">Runico</span><span class="sxs-lookup"><span data-stu-id="75ef3-411">Runic</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="75ef3-412">80 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-412">80${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-413">1780 - 17FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-413">1780 - 17FF</span></span></td>
<td><span data-ttu-id="75ef3-414">Khmer</span><span class="sxs-lookup"><span data-stu-id="75ef3-414">Khmer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-415">19E0 - 19FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-415">19E0 - 19FF</span></span></td>
<td><span data-ttu-id="75ef3-416">Simboli Khmer</span><span class="sxs-lookup"><span data-stu-id="75ef3-416">Khmer Symbols</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-417">81</span><span class="sxs-lookup"><span data-stu-id="75ef3-417">81</span></span></td>
<td><span data-ttu-id="75ef3-418">1800 - 18AF</span><span class="sxs-lookup"><span data-stu-id="75ef3-418">1800 - 18AF</span></span></td>
<td><span data-ttu-id="75ef3-419">Mongolo</span><span class="sxs-lookup"><span data-stu-id="75ef3-419">Mongolian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-420">82</span><span class="sxs-lookup"><span data-stu-id="75ef3-420">82</span></span></td>
<td><span data-ttu-id="75ef3-421">2800 - 28FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-421">2800 - 28FF</span></span></td>
<td><span data-ttu-id="75ef3-422">Modelli Braille</span><span class="sxs-lookup"><span data-stu-id="75ef3-422">Braille Patterns</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="75ef3-423">83 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-423">83${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-424">A000 - A48F</span><span class="sxs-lookup"><span data-stu-id="75ef3-424">A000 - A48F</span></span></td>
<td><span data-ttu-id="75ef3-425">Sillabe di Yi</span><span class="sxs-lookup"><span data-stu-id="75ef3-425">Yi Syllables</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-426">A490 - A4CF</span><span class="sxs-lookup"><span data-stu-id="75ef3-426">A490 - A4CF</span></span></td>
<td><span data-ttu-id="75ef3-427">Radicali Yi</span><span class="sxs-lookup"><span data-stu-id="75ef3-427">Yi Radicals</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="75ef3-428">84 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-428">84${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-429">1700 - 171F</span><span class="sxs-lookup"><span data-stu-id="75ef3-429">1700 - 171F</span></span></td>
<td><span data-ttu-id="75ef3-430">Tagalog</span><span class="sxs-lookup"><span data-stu-id="75ef3-430">Tagalog</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-431">1720 - 173F</span><span class="sxs-lookup"><span data-stu-id="75ef3-431">1720 - 173F</span></span></td>
<td><span data-ttu-id="75ef3-432">Hanunoo</span><span class="sxs-lookup"><span data-stu-id="75ef3-432">Hanunoo</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-433">1740 - 175F</span><span class="sxs-lookup"><span data-stu-id="75ef3-433">1740 - 175F</span></span></td>
<td><span data-ttu-id="75ef3-434">Buhid:</span><span class="sxs-lookup"><span data-stu-id="75ef3-434">Buhid</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-435">1760 - 177F</span><span class="sxs-lookup"><span data-stu-id="75ef3-435">1760 - 177F</span></span></td>
<td><span data-ttu-id="75ef3-436">Tagbanwa</span><span class="sxs-lookup"><span data-stu-id="75ef3-436">Tagbanwa</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-437">85</span><span class="sxs-lookup"><span data-stu-id="75ef3-437">85</span></span></td>
<td><span data-ttu-id="75ef3-438">10300-1032F</span><span class="sxs-lookup"><span data-stu-id="75ef3-438">10300 - 1032F</span></span></td>
<td><span data-ttu-id="75ef3-439">Corsivo precedente</span><span class="sxs-lookup"><span data-stu-id="75ef3-439">Old Italic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-440">86</span><span class="sxs-lookup"><span data-stu-id="75ef3-440">86</span></span></td>
<td><span data-ttu-id="75ef3-441">10330-1034F</span><span class="sxs-lookup"><span data-stu-id="75ef3-441">10330 - 1034F</span></span></td>
<td><span data-ttu-id="75ef3-442">Gothic</span><span class="sxs-lookup"><span data-stu-id="75ef3-442">Gothic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-443">87</span><span class="sxs-lookup"><span data-stu-id="75ef3-443">87</span></span></td>
<td><span data-ttu-id="75ef3-444">10400-1044F</span><span class="sxs-lookup"><span data-stu-id="75ef3-444">10400 - 1044F</span></span></td>
<td><span data-ttu-id="75ef3-445">Deseret</span><span class="sxs-lookup"><span data-stu-id="75ef3-445">Deseret</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="75ef3-446">88 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-446">88${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-447">1D000 - 1D0FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-447">1D000 - 1D0FF</span></span></td>
<td><span data-ttu-id="75ef3-448">Simboli musicali bizantini</span><span class="sxs-lookup"><span data-stu-id="75ef3-448">Byzantine Musical Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-449">1D100 - 1D1FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-449">1D100 - 1D1FF</span></span></td>
<td><span data-ttu-id="75ef3-450">Simboli musicali</span><span class="sxs-lookup"><span data-stu-id="75ef3-450">Musical Symbols</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-451">1D200 - 1D24F</span><span class="sxs-lookup"><span data-stu-id="75ef3-451">1D200 - 1D24F</span></span></td>
<td><span data-ttu-id="75ef3-452">Notazione musicale greca antica</span><span class="sxs-lookup"><span data-stu-id="75ef3-452">Ancient Greek Musical Notation</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-453">89</span><span class="sxs-lookup"><span data-stu-id="75ef3-453">89</span></span></td>
<td><span data-ttu-id="75ef3-454">1D400 - 1D7FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-454">1D400 - 1D7FF</span></span></td>
<td><span data-ttu-id="75ef3-455">Simboli alfanumerici matematici</span><span class="sxs-lookup"><span data-stu-id="75ef3-455">Mathematical Alphanumeric Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="75ef3-456">90 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-456">90${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-457">FF000 - FFFFD</span><span class="sxs-lookup"><span data-stu-id="75ef3-457">FF000 - FFFFD</span></span></td>
<td><span data-ttu-id="75ef3-458">Uso privato (piano 15)</span><span class="sxs-lookup"><span data-stu-id="75ef3-458">Private Use (plane 15)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-459">100000-10FFFD</span><span class="sxs-lookup"><span data-stu-id="75ef3-459">100000 - 10FFFD</span></span></td>
<td><span data-ttu-id="75ef3-460">Uso privato (piano 16)</span><span class="sxs-lookup"><span data-stu-id="75ef3-460">Private Use (plane 16)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="75ef3-461">91 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-461">91${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-462">FE00 - FE0F</span><span class="sxs-lookup"><span data-stu-id="75ef3-462">FE00 - FE0F</span></span></td>
<td><span data-ttu-id="75ef3-463">Selettori di variazione</span><span class="sxs-lookup"><span data-stu-id="75ef3-463">Variation Selectors</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-464">E0100 - E01EF</span><span class="sxs-lookup"><span data-stu-id="75ef3-464">E0100 - E01EF</span></span></td>
<td><span data-ttu-id="75ef3-465">Supplemento per i selettori di variazione</span><span class="sxs-lookup"><span data-stu-id="75ef3-465">Variation Selectors Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-466">92</span><span class="sxs-lookup"><span data-stu-id="75ef3-466">92</span></span></td>
<td><span data-ttu-id="75ef3-467">E0000 - E007F</span><span class="sxs-lookup"><span data-stu-id="75ef3-467">E0000 - E007F</span></span></td>
<td><span data-ttu-id="75ef3-468">Tag</span><span class="sxs-lookup"><span data-stu-id="75ef3-468">Tags</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-469">93</span><span class="sxs-lookup"><span data-stu-id="75ef3-469">93</span></span></td>
<td><span data-ttu-id="75ef3-470">1900 - 194F</span><span class="sxs-lookup"><span data-stu-id="75ef3-470">1900 - 194F</span></span></td>
<td><span data-ttu-id="75ef3-471">Limbu</span><span class="sxs-lookup"><span data-stu-id="75ef3-471">Limbu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-472">94</span><span class="sxs-lookup"><span data-stu-id="75ef3-472">94</span></span></td>
<td><span data-ttu-id="75ef3-473">1950 - 197F</span><span class="sxs-lookup"><span data-stu-id="75ef3-473">1950 - 197F</span></span></td>
<td><span data-ttu-id="75ef3-474">Tai le</span><span class="sxs-lookup"><span data-stu-id="75ef3-474">Tai Le</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-475">95</span><span class="sxs-lookup"><span data-stu-id="75ef3-475">95</span></span></td>
<td><span data-ttu-id="75ef3-476">1980-19DF</span><span class="sxs-lookup"><span data-stu-id="75ef3-476">1980 - 19DF</span></span></td>
<td><span data-ttu-id="75ef3-477">Nuovo tai lue</span><span class="sxs-lookup"><span data-stu-id="75ef3-477">New Tai Lue</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-478">96</span><span class="sxs-lookup"><span data-stu-id="75ef3-478">96</span></span></td>
<td><span data-ttu-id="75ef3-479">1A00 - 1A1F</span><span class="sxs-lookup"><span data-stu-id="75ef3-479">1A00 - 1A1F</span></span></td>
<td><span data-ttu-id="75ef3-480">Buginese</span><span class="sxs-lookup"><span data-stu-id="75ef3-480">Buginese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-481">97</span><span class="sxs-lookup"><span data-stu-id="75ef3-481">97</span></span></td>
<td><span data-ttu-id="75ef3-482">2C00 - 2C5F</span><span class="sxs-lookup"><span data-stu-id="75ef3-482">2C00 - 2C5F</span></span></td>
<td><span data-ttu-id="75ef3-483">Glagolitico</span><span class="sxs-lookup"><span data-stu-id="75ef3-483">Glagolitic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-484">98</span><span class="sxs-lookup"><span data-stu-id="75ef3-484">98</span></span></td>
<td><span data-ttu-id="75ef3-485">2D30-2D7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-485">2D30 - 2D7F</span></span></td>
<td><span data-ttu-id="75ef3-486">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="75ef3-486">Tifinagh</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-487">99</span><span class="sxs-lookup"><span data-stu-id="75ef3-487">99</span></span></td>
<td><span data-ttu-id="75ef3-488">4DC0 - 4DFF</span><span class="sxs-lookup"><span data-stu-id="75ef3-488">4DC0 - 4DFF</span></span></td>
<td><span data-ttu-id="75ef3-489">Simboli esagrammi esagrammi</span><span class="sxs-lookup"><span data-stu-id="75ef3-489">Yijing Hexagram Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-490">100</span><span class="sxs-lookup"><span data-stu-id="75ef3-490">100</span></span></td>
<td><span data-ttu-id="75ef3-491">A800-A82F</span><span class="sxs-lookup"><span data-stu-id="75ef3-491">A800 - A82F</span></span></td>
<td><span data-ttu-id="75ef3-492">Nagri Carattere syloti nagri</span><span class="sxs-lookup"><span data-stu-id="75ef3-492">Syloti Nagri</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="75ef3-493">101 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-493">101${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-494">10000-1007F</span><span class="sxs-lookup"><span data-stu-id="75ef3-494">10000 - 1007F</span></span></td>
<td><span data-ttu-id="75ef3-495">Sillabario B lineare</span><span class="sxs-lookup"><span data-stu-id="75ef3-495">Linear B Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-496">10080-100FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-496">10080 - 100FF</span></span></td>
<td><span data-ttu-id="75ef3-497">Degli ideogrammi lineare B</span><span class="sxs-lookup"><span data-stu-id="75ef3-497">Linear B Ideograms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-498">10100-1013F</span><span class="sxs-lookup"><span data-stu-id="75ef3-498">10100 - 1013F</span></span></td>
<td><span data-ttu-id="75ef3-499">Numeri Aegean</span><span class="sxs-lookup"><span data-stu-id="75ef3-499">Aegean Numbers</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-500">102</span><span class="sxs-lookup"><span data-stu-id="75ef3-500">102</span></span></td>
<td><span data-ttu-id="75ef3-501">10140-1018F</span><span class="sxs-lookup"><span data-stu-id="75ef3-501">10140 - 1018F</span></span></td>
<td><span data-ttu-id="75ef3-502">Numeri greci antichi</span><span class="sxs-lookup"><span data-stu-id="75ef3-502">Ancient Greek Numbers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-503">103</span><span class="sxs-lookup"><span data-stu-id="75ef3-503">103</span></span></td>
<td><span data-ttu-id="75ef3-504">10380-1039F</span><span class="sxs-lookup"><span data-stu-id="75ef3-504">10380 - 1039F</span></span></td>
<td><span data-ttu-id="75ef3-505">Ugaritico</span><span class="sxs-lookup"><span data-stu-id="75ef3-505">Ugaritic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-506">104</span><span class="sxs-lookup"><span data-stu-id="75ef3-506">104</span></span></td>
<td><span data-ttu-id="75ef3-507">103A0 - 103DF</span><span class="sxs-lookup"><span data-stu-id="75ef3-507">103A0 - 103DF</span></span></td>
<td><span data-ttu-id="75ef3-508">Persiano precedente</span><span class="sxs-lookup"><span data-stu-id="75ef3-508">Old Persian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-509">105</span><span class="sxs-lookup"><span data-stu-id="75ef3-509">105</span></span></td>
<td><span data-ttu-id="75ef3-510">10450-1047F</span><span class="sxs-lookup"><span data-stu-id="75ef3-510">10450 - 1047F</span></span></td>
<td><span data-ttu-id="75ef3-511">L'shaviano</span><span class="sxs-lookup"><span data-stu-id="75ef3-511">Shavian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-512">106</span><span class="sxs-lookup"><span data-stu-id="75ef3-512">106</span></span></td>
<td><span data-ttu-id="75ef3-513">10480-104AF</span><span class="sxs-lookup"><span data-stu-id="75ef3-513">10480 - 104AF</span></span></td>
<td><span data-ttu-id="75ef3-514">Osmanya</span><span class="sxs-lookup"><span data-stu-id="75ef3-514">Osmanya</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-515">107</span><span class="sxs-lookup"><span data-stu-id="75ef3-515">107</span></span></td>
<td><span data-ttu-id="75ef3-516">10800-1083F</span><span class="sxs-lookup"><span data-stu-id="75ef3-516">10800 - 1083F</span></span></td>
<td><span data-ttu-id="75ef3-517">Sillabario cipriota</span><span class="sxs-lookup"><span data-stu-id="75ef3-517">Cypriot Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-518">108</span><span class="sxs-lookup"><span data-stu-id="75ef3-518">108</span></span></td>
<td><span data-ttu-id="75ef3-519">10A00 - 10A5F</span><span class="sxs-lookup"><span data-stu-id="75ef3-519">10A00 - 10A5F</span></span></td>
<td><span data-ttu-id="75ef3-520">Kharoshthi</span><span class="sxs-lookup"><span data-stu-id="75ef3-520">Kharoshthi</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-521">109</span><span class="sxs-lookup"><span data-stu-id="75ef3-521">109</span></span></td>
<td><span data-ttu-id="75ef3-522">1D300 - 1D35F</span><span class="sxs-lookup"><span data-stu-id="75ef3-522">1D300 - 1D35F</span></span></td>
<td><span data-ttu-id="75ef3-523">Simboli Tai Xuan Jing</span><span class="sxs-lookup"><span data-stu-id="75ef3-523">Tai Xuan Jing Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="75ef3-524">110 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-524">110${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-525">12000-123FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-525">12000 - 123FF</span></span></td>
<td><span data-ttu-id="75ef3-526">Cuneiforme</span><span class="sxs-lookup"><span data-stu-id="75ef3-526">Cuneiform</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-527">12400-1247F</span><span class="sxs-lookup"><span data-stu-id="75ef3-527">12400 - 1247F</span></span></td>
<td><span data-ttu-id="75ef3-528">Numeri e punteggiatura cuneiforme</span><span class="sxs-lookup"><span data-stu-id="75ef3-528">Cuneiform Numbers and Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-529">111</span><span class="sxs-lookup"><span data-stu-id="75ef3-529">111</span></span></td>
<td><span data-ttu-id="75ef3-530">1D360 - 1D37F</span><span class="sxs-lookup"><span data-stu-id="75ef3-530">1D360 - 1D37F</span></span></td>
<td><span data-ttu-id="75ef3-531">Conteggio dei numeri di asta</span><span class="sxs-lookup"><span data-stu-id="75ef3-531">Counting Rod Numerals</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-532">112</span><span class="sxs-lookup"><span data-stu-id="75ef3-532">112</span></span></td>
<td><span data-ttu-id="75ef3-533">1B80 - 1BBF</span><span class="sxs-lookup"><span data-stu-id="75ef3-533">1B80 - 1BBF</span></span></td>
<td><span data-ttu-id="75ef3-534">Sundanese</span><span class="sxs-lookup"><span data-stu-id="75ef3-534">Sundanese</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-535">113</span><span class="sxs-lookup"><span data-stu-id="75ef3-535">113</span></span></td>
<td><span data-ttu-id="75ef3-536">1C00 - 1C4F</span><span class="sxs-lookup"><span data-stu-id="75ef3-536">1C00 - 1C4F</span></span></td>
<td><span data-ttu-id="75ef3-537">Lepcha</span><span class="sxs-lookup"><span data-stu-id="75ef3-537">Lepcha</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-538">114</span><span class="sxs-lookup"><span data-stu-id="75ef3-538">114</span></span></td>
<td><span data-ttu-id="75ef3-539">1C50 - 1C7F</span><span class="sxs-lookup"><span data-stu-id="75ef3-539">1C50 - 1C7F</span></span></td>
<td><span data-ttu-id="75ef3-540">Chiki OL</span><span class="sxs-lookup"><span data-stu-id="75ef3-540">Ol Chiki</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-541">115</span><span class="sxs-lookup"><span data-stu-id="75ef3-541">115</span></span></td>
<td><span data-ttu-id="75ef3-542">A880 - A8DF</span><span class="sxs-lookup"><span data-stu-id="75ef3-542">A880 - A8DF</span></span></td>
<td><span data-ttu-id="75ef3-543">Saurashtra</span><span class="sxs-lookup"><span data-stu-id="75ef3-543">Saurashtra</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-544">116</span><span class="sxs-lookup"><span data-stu-id="75ef3-544">116</span></span></td>
<td><span data-ttu-id="75ef3-545">A900-A92F</span><span class="sxs-lookup"><span data-stu-id="75ef3-545">A900 - A92F</span></span></td>
<td><span data-ttu-id="75ef3-546">Kayah Li</span><span class="sxs-lookup"><span data-stu-id="75ef3-546">Kayah Li</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-547">117</span><span class="sxs-lookup"><span data-stu-id="75ef3-547">117</span></span></td>
<td><span data-ttu-id="75ef3-548">A930-A95F</span><span class="sxs-lookup"><span data-stu-id="75ef3-548">A930 - A95F</span></span></td>
<td><span data-ttu-id="75ef3-549">Rejang</span><span class="sxs-lookup"><span data-stu-id="75ef3-549">Rejang</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-550">118</span><span class="sxs-lookup"><span data-stu-id="75ef3-550">118</span></span></td>
<td><span data-ttu-id="75ef3-551">AA00 - AA5F</span><span class="sxs-lookup"><span data-stu-id="75ef3-551">AA00 - AA5F</span></span></td>
<td><span data-ttu-id="75ef3-552">Cham</span><span class="sxs-lookup"><span data-stu-id="75ef3-552">Cham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-553">119</span><span class="sxs-lookup"><span data-stu-id="75ef3-553">119</span></span></td>
<td><span data-ttu-id="75ef3-554">10190-101CF</span><span class="sxs-lookup"><span data-stu-id="75ef3-554">10190 - 101CF</span></span></td>
<td><span data-ttu-id="75ef3-555">Simboli antichi</span><span class="sxs-lookup"><span data-stu-id="75ef3-555">Ancient Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-556">120</span><span class="sxs-lookup"><span data-stu-id="75ef3-556">120</span></span></td>
<td><span data-ttu-id="75ef3-557">101D0 - 101FF</span><span class="sxs-lookup"><span data-stu-id="75ef3-557">101D0 - 101FF</span></span></td>
<td><span data-ttu-id="75ef3-558">Disco Festo</span><span class="sxs-lookup"><span data-stu-id="75ef3-558">Phaistos Disc</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="75ef3-559">121 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-559">121${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-560">10280-1029F</span><span class="sxs-lookup"><span data-stu-id="75ef3-560">10280 - 1029F</span></span></td>
<td><span data-ttu-id="75ef3-561">Lycian</span><span class="sxs-lookup"><span data-stu-id="75ef3-561">Lycian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-562">102A0 - 102DF</span><span class="sxs-lookup"><span data-stu-id="75ef3-562">102A0 - 102DF</span></span></td>
<td><span data-ttu-id="75ef3-563">Caria</span><span class="sxs-lookup"><span data-stu-id="75ef3-563">Carian</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-564">10920-1093F</span><span class="sxs-lookup"><span data-stu-id="75ef3-564">10920 - 1093F</span></span></td>
<td><span data-ttu-id="75ef3-565">Lydian</span><span class="sxs-lookup"><span data-stu-id="75ef3-565">Lydian</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="75ef3-566">122 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="75ef3-566">122${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="75ef3-567">1F000 - 1F02F</span><span class="sxs-lookup"><span data-stu-id="75ef3-567">1F000 - 1F02F</span></span></td>
<td><span data-ttu-id="75ef3-568">Riquadri Mahjong</span><span class="sxs-lookup"><span data-stu-id="75ef3-568">Mahjong Tiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-569">1F030 - 1F09F</span><span class="sxs-lookup"><span data-stu-id="75ef3-569">1F030 - 1F09F</span></span></td>
<td><span data-ttu-id="75ef3-570">Tessere domino</span><span class="sxs-lookup"><span data-stu-id="75ef3-570">Domino Tiles</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-571">123</span><span class="sxs-lookup"><span data-stu-id="75ef3-571">123</span></span></td>

<td><span data-ttu-id="75ef3-572"><strong>Windows 2000 e versioni successive:</strong> Stato del layout, orizzontale da destra a sinistra</span><span class="sxs-lookup"><span data-stu-id="75ef3-572"><strong>Windows 2000 and later:</strong> Layout progress, horizontal from right to left</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-573">124</span><span class="sxs-lookup"><span data-stu-id="75ef3-573">124</span></span></td>

<td><span data-ttu-id="75ef3-574"><strong>Windows 2000 e versioni successive:</strong> Stato del layout, verticale prima dell'orizzontale</span><span class="sxs-lookup"><span data-stu-id="75ef3-574"><strong>Windows 2000 and later:</strong> Layout progress, vertical before horizontal</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ef3-575">125</span><span class="sxs-lookup"><span data-stu-id="75ef3-575">125</span></span></td>

<td><span data-ttu-id="75ef3-576"><strong>Windows 2000 e versioni successive:</strong> Stato del layout, dal basso verso l'alto verticale</span><span class="sxs-lookup"><span data-stu-id="75ef3-576"><strong>Windows 2000 and later:</strong> Layout progress, vertical bottom to top</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ef3-577">126-127</span><span class="sxs-lookup"><span data-stu-id="75ef3-577">126-127</span></span></td>

<td><span data-ttu-id="75ef3-578">Riservato per l'utilizzo interno del processo</span><span class="sxs-lookup"><span data-stu-id="75ef3-578">Reserved for process-internal usage</span></span></td>
</tr>
</tbody>
</table>



 

 

 




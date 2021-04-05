---
title: Istruzione BLOCK VarFileInfo
description: Descrive il formato del blocco di informazioni della variabile.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menu di istruzioni di blocco VarFileInfo e altre risorse
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045888"
---
# <a name="varfileinfo-block-statement"></a><span data-ttu-id="0eab8-104">Istruzione BLOCK VarFileInfo</span><span class="sxs-lookup"><span data-stu-id="0eab8-104">VarFileInfo BLOCK statement</span></span>

<span data-ttu-id="0eab8-105">Definisce un blocco di informazioni sulla variabile.</span><span class="sxs-lookup"><span data-stu-id="0eab8-105">Defines a variable information block.</span></span>

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a><span data-ttu-id="0eab8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0eab8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eab8-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="0eab8-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="0eab8-108">Uno degli identificatori di lingua specificati nella sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0eab8-108">One of the language identifiers specified in the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="0eab8-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="0eab8-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="0eab8-110">Uno degli identificatori del set di caratteri specificati nella sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0eab8-110">One of the character-set identifiers specified in the Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0eab8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0eab8-111">Remarks</span></span>

<span data-ttu-id="0eab8-112">È possibile assegnare più di una coppia di identificatori, ma ogni coppia deve essere separata dalla coppia precedente con una virgola.</span><span class="sxs-lookup"><span data-stu-id="0eab8-112">More than one identifier pair can be given, but each pair must be separated from the preceding pair with a comma.</span></span>

<span data-ttu-id="0eab8-113">Il parametro *LangID* specifica uno dei seguenti codici di lingua.</span><span class="sxs-lookup"><span data-stu-id="0eab8-113">The *langID* parameter specifies one of the following language codes.</span></span>



| <span data-ttu-id="0eab8-114">Codice</span><span class="sxs-lookup"><span data-stu-id="0eab8-114">Code</span></span>   | <span data-ttu-id="0eab8-115">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="0eab8-115">Language</span></span>            | <span data-ttu-id="0eab8-116">Codice</span><span class="sxs-lookup"><span data-stu-id="0eab8-116">Code</span></span>   | <span data-ttu-id="0eab8-117">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="0eab8-117">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="0eab8-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="0eab8-118">0x0401</span></span> | <span data-ttu-id="0eab8-119">Arabo</span><span class="sxs-lookup"><span data-stu-id="0eab8-119">Arabic</span></span>              | <span data-ttu-id="0eab8-120">0x0415</span><span class="sxs-lookup"><span data-stu-id="0eab8-120">0x0415</span></span> | <span data-ttu-id="0eab8-121">Polacco</span><span class="sxs-lookup"><span data-stu-id="0eab8-121">Polish</span></span>                    |
| <span data-ttu-id="0eab8-122">0x0402</span><span class="sxs-lookup"><span data-stu-id="0eab8-122">0x0402</span></span> | <span data-ttu-id="0eab8-123">Bulgaro</span><span class="sxs-lookup"><span data-stu-id="0eab8-123">Bulgarian</span></span>           | <span data-ttu-id="0eab8-124">0x0416</span><span class="sxs-lookup"><span data-stu-id="0eab8-124">0x0416</span></span> | <span data-ttu-id="0eab8-125">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="0eab8-125">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="0eab8-126">0x0403</span><span class="sxs-lookup"><span data-stu-id="0eab8-126">0x0403</span></span> | <span data-ttu-id="0eab8-127">Catalano</span><span class="sxs-lookup"><span data-stu-id="0eab8-127">Catalan</span></span>             | <span data-ttu-id="0eab8-128">0x0417</span><span class="sxs-lookup"><span data-stu-id="0eab8-128">0x0417</span></span> | <span data-ttu-id="0eab8-129">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="0eab8-129">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="0eab8-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="0eab8-130">0x0404</span></span> | <span data-ttu-id="0eab8-131">Cinese tradizionale</span><span class="sxs-lookup"><span data-stu-id="0eab8-131">Traditional Chinese</span></span> | <span data-ttu-id="0eab8-132">0x0418</span><span class="sxs-lookup"><span data-stu-id="0eab8-132">0x0418</span></span> | <span data-ttu-id="0eab8-133">Romeno</span><span class="sxs-lookup"><span data-stu-id="0eab8-133">Romanian</span></span>                  |
| <span data-ttu-id="0eab8-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="0eab8-134">0x0405</span></span> | <span data-ttu-id="0eab8-135">Ceco</span><span class="sxs-lookup"><span data-stu-id="0eab8-135">Czech</span></span>               | <span data-ttu-id="0eab8-136">0x0419</span><span class="sxs-lookup"><span data-stu-id="0eab8-136">0x0419</span></span> | <span data-ttu-id="0eab8-137">Russo</span><span class="sxs-lookup"><span data-stu-id="0eab8-137">Russian</span></span>                   |
| <span data-ttu-id="0eab8-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="0eab8-138">0x0406</span></span> | <span data-ttu-id="0eab8-139">Danese</span><span class="sxs-lookup"><span data-stu-id="0eab8-139">Danish</span></span>              | <span data-ttu-id="0eab8-140">0x041A</span><span class="sxs-lookup"><span data-stu-id="0eab8-140">0x041A</span></span> | <span data-ttu-id="0eab8-141">Croato-Serbian (alfabeto latino)</span><span class="sxs-lookup"><span data-stu-id="0eab8-141">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="0eab8-142">0x0407</span><span class="sxs-lookup"><span data-stu-id="0eab8-142">0x0407</span></span> | <span data-ttu-id="0eab8-143">Tedesco</span><span class="sxs-lookup"><span data-stu-id="0eab8-143">German</span></span>              | <span data-ttu-id="0eab8-144">0x041B</span><span class="sxs-lookup"><span data-stu-id="0eab8-144">0x041B</span></span> | <span data-ttu-id="0eab8-145">Slovacco</span><span class="sxs-lookup"><span data-stu-id="0eab8-145">Slovak</span></span>                    |
| <span data-ttu-id="0eab8-146">0x0408</span><span class="sxs-lookup"><span data-stu-id="0eab8-146">0x0408</span></span> | <span data-ttu-id="0eab8-147">Greco</span><span class="sxs-lookup"><span data-stu-id="0eab8-147">Greek</span></span>               | <span data-ttu-id="0eab8-148">0x041C</span><span class="sxs-lookup"><span data-stu-id="0eab8-148">0x041C</span></span> | <span data-ttu-id="0eab8-149">Albanese</span><span class="sxs-lookup"><span data-stu-id="0eab8-149">Albanian</span></span>                  |
| <span data-ttu-id="0eab8-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="0eab8-150">0x0409</span></span> | <span data-ttu-id="0eab8-151">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="0eab8-151">U.S. English</span></span>        | <span data-ttu-id="0eab8-152">0x041D</span><span class="sxs-lookup"><span data-stu-id="0eab8-152">0x041D</span></span> | <span data-ttu-id="0eab8-153">Svedese</span><span class="sxs-lookup"><span data-stu-id="0eab8-153">Swedish</span></span>                   |
| <span data-ttu-id="0eab8-154">0x040A</span><span class="sxs-lookup"><span data-stu-id="0eab8-154">0x040A</span></span> | <span data-ttu-id="0eab8-155">Spagnolo castigliano</span><span class="sxs-lookup"><span data-stu-id="0eab8-155">Castilian Spanish</span></span>   | <span data-ttu-id="0eab8-156">0x041E</span><span class="sxs-lookup"><span data-stu-id="0eab8-156">0x041E</span></span> | <span data-ttu-id="0eab8-157">Thai</span><span class="sxs-lookup"><span data-stu-id="0eab8-157">Thai</span></span>                      |
| <span data-ttu-id="0eab8-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="0eab8-158">0x040B</span></span> | <span data-ttu-id="0eab8-159">Finlandese</span><span class="sxs-lookup"><span data-stu-id="0eab8-159">Finnish</span></span>             | <span data-ttu-id="0eab8-160">0x041F</span><span class="sxs-lookup"><span data-stu-id="0eab8-160">0x041F</span></span> | <span data-ttu-id="0eab8-161">Turco</span><span class="sxs-lookup"><span data-stu-id="0eab8-161">Turkish</span></span>                   |
| <span data-ttu-id="0eab8-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="0eab8-162">0x040C</span></span> | <span data-ttu-id="0eab8-163">Francese</span><span class="sxs-lookup"><span data-stu-id="0eab8-163">French</span></span>              | <span data-ttu-id="0eab8-164">0x0420</span><span class="sxs-lookup"><span data-stu-id="0eab8-164">0x0420</span></span> | <span data-ttu-id="0eab8-165">Urdu</span><span class="sxs-lookup"><span data-stu-id="0eab8-165">Urdu</span></span>                      |
| <span data-ttu-id="0eab8-166">0x040D</span><span class="sxs-lookup"><span data-stu-id="0eab8-166">0x040D</span></span> | <span data-ttu-id="0eab8-167">Ebraico</span><span class="sxs-lookup"><span data-stu-id="0eab8-167">Hebrew</span></span>              | <span data-ttu-id="0eab8-168">0x0421</span><span class="sxs-lookup"><span data-stu-id="0eab8-168">0x0421</span></span> | <span data-ttu-id="0eab8-169">Bahasa</span><span class="sxs-lookup"><span data-stu-id="0eab8-169">Bahasa</span></span>                    |
| <span data-ttu-id="0eab8-170">0x040E</span><span class="sxs-lookup"><span data-stu-id="0eab8-170">0x040E</span></span> | <span data-ttu-id="0eab8-171">Ungherese</span><span class="sxs-lookup"><span data-stu-id="0eab8-171">Hungarian</span></span>           | <span data-ttu-id="0eab8-172">0x0804</span><span class="sxs-lookup"><span data-stu-id="0eab8-172">0x0804</span></span> | <span data-ttu-id="0eab8-173">Cinese semplificato</span><span class="sxs-lookup"><span data-stu-id="0eab8-173">Simplified Chinese</span></span>        |
| <span data-ttu-id="0eab8-174">0x040F</span><span class="sxs-lookup"><span data-stu-id="0eab8-174">0x040F</span></span> | <span data-ttu-id="0eab8-175">Islandese</span><span class="sxs-lookup"><span data-stu-id="0eab8-175">Icelandic</span></span>           | <span data-ttu-id="0eab8-176">0x0807</span><span class="sxs-lookup"><span data-stu-id="0eab8-176">0x0807</span></span> | <span data-ttu-id="0eab8-177">Tedesco svizzero</span><span class="sxs-lookup"><span data-stu-id="0eab8-177">Swiss German</span></span>              |
| <span data-ttu-id="0eab8-178">0x0410</span><span class="sxs-lookup"><span data-stu-id="0eab8-178">0x0410</span></span> | <span data-ttu-id="0eab8-179">Italiano</span><span class="sxs-lookup"><span data-stu-id="0eab8-179">Italian</span></span>             | <span data-ttu-id="0eab8-180">0x0809</span><span class="sxs-lookup"><span data-stu-id="0eab8-180">0x0809</span></span> | <span data-ttu-id="0eab8-181">Regno Unito.</span><span class="sxs-lookup"><span data-stu-id="0eab8-181">U.K.</span></span> <span data-ttu-id="0eab8-182">Inglese</span><span class="sxs-lookup"><span data-stu-id="0eab8-182">English</span></span>              |
| <span data-ttu-id="0eab8-183">0x0411</span><span class="sxs-lookup"><span data-stu-id="0eab8-183">0x0411</span></span> | <span data-ttu-id="0eab8-184">Giapponese</span><span class="sxs-lookup"><span data-stu-id="0eab8-184">Japanese</span></span>            | <span data-ttu-id="0eab8-185">0x080A</span><span class="sxs-lookup"><span data-stu-id="0eab8-185">0x080A</span></span> | <span data-ttu-id="0eab8-186">Spagnolo (Messico)</span><span class="sxs-lookup"><span data-stu-id="0eab8-186">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="0eab8-187">0x0412</span><span class="sxs-lookup"><span data-stu-id="0eab8-187">0x0412</span></span> | <span data-ttu-id="0eab8-188">Coreano</span><span class="sxs-lookup"><span data-stu-id="0eab8-188">Korean</span></span>              | <span data-ttu-id="0eab8-189">0x080C</span><span class="sxs-lookup"><span data-stu-id="0eab8-189">0x080C</span></span> | <span data-ttu-id="0eab8-190">Francese belga</span><span class="sxs-lookup"><span data-stu-id="0eab8-190">Belgian French</span></span>            |
| <span data-ttu-id="0eab8-191">0x0413</span><span class="sxs-lookup"><span data-stu-id="0eab8-191">0x0413</span></span> | <span data-ttu-id="0eab8-192">Olandese</span><span class="sxs-lookup"><span data-stu-id="0eab8-192">Dutch</span></span>               | <span data-ttu-id="0eab8-193">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="0eab8-193">0x0C0C</span></span> | <span data-ttu-id="0eab8-194">Francese (Canada)</span><span class="sxs-lookup"><span data-stu-id="0eab8-194">Canadian French</span></span>           |
| <span data-ttu-id="0eab8-195">0x0414</span><span class="sxs-lookup"><span data-stu-id="0eab8-195">0x0414</span></span> | <span data-ttu-id="0eab8-196">Norvegese – Bokmal</span><span class="sxs-lookup"><span data-stu-id="0eab8-196">Norwegian – Bokmal</span></span>  | <span data-ttu-id="0eab8-197">0x100C</span><span class="sxs-lookup"><span data-stu-id="0eab8-197">0x100C</span></span> | <span data-ttu-id="0eab8-198">Francese svizzero</span><span class="sxs-lookup"><span data-stu-id="0eab8-198">Swiss French</span></span>              |
| <span data-ttu-id="0eab8-199">0x0810</span><span class="sxs-lookup"><span data-stu-id="0eab8-199">0x0810</span></span> | <span data-ttu-id="0eab8-200">Italiano svizzero</span><span class="sxs-lookup"><span data-stu-id="0eab8-200">Swiss Italian</span></span>       | <span data-ttu-id="0eab8-201">0x0816</span><span class="sxs-lookup"><span data-stu-id="0eab8-201">0x0816</span></span> | <span data-ttu-id="0eab8-202">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="0eab8-202">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="0eab8-203">0x0813</span><span class="sxs-lookup"><span data-stu-id="0eab8-203">0x0813</span></span> | <span data-ttu-id="0eab8-204">Olandese belga</span><span class="sxs-lookup"><span data-stu-id="0eab8-204">Belgian Dutch</span></span>       | <span data-ttu-id="0eab8-205">0x081A</span><span class="sxs-lookup"><span data-stu-id="0eab8-205">0x081A</span></span> | <span data-ttu-id="0eab8-206">Serbo-Croatian (alfabeto cirillico)</span><span class="sxs-lookup"><span data-stu-id="0eab8-206">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="0eab8-207">0x0814</span><span class="sxs-lookup"><span data-stu-id="0eab8-207">0x0814</span></span> | <span data-ttu-id="0eab8-208">Norvegese – Nynorsk</span><span class="sxs-lookup"><span data-stu-id="0eab8-208">Norwegian – Nynorsk</span></span> | <span data-ttu-id="0eab8-209">?</span><span class="sxs-lookup"><span data-stu-id="0eab8-209">?</span></span>      | <span data-ttu-id="0eab8-210">?</span><span class="sxs-lookup"><span data-stu-id="0eab8-210">?</span></span>                         |



 

<span data-ttu-id="0eab8-211">Il parametro *charsetID* specifica uno dei seguenti identificatori di set di caratteri:</span><span class="sxs-lookup"><span data-stu-id="0eab8-211">The *charsetID* parameter specifies one of the following character-set identifiers:</span></span>



| <span data-ttu-id="0eab8-212">Identificatore</span><span class="sxs-lookup"><span data-stu-id="0eab8-212">Identifier</span></span> | <span data-ttu-id="0eab8-213">Set di caratteri</span><span class="sxs-lookup"><span data-stu-id="0eab8-213">Character Set</span></span>              |
|------------|----------------------------|
| <span data-ttu-id="0eab8-214">0</span><span class="sxs-lookup"><span data-stu-id="0eab8-214">0</span></span>          | <span data-ttu-id="0eab8-215">ASCII a 7 bit</span><span class="sxs-lookup"><span data-stu-id="0eab8-215">7-bit ASCII</span></span>                |
| <span data-ttu-id="0eab8-216">932</span><span class="sxs-lookup"><span data-stu-id="0eab8-216">932</span></span>        | <span data-ttu-id="0eab8-217">Giappone (MAIUSC – JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="0eab8-217">Japan (Shift – JIS X-0208)</span></span> |
| <span data-ttu-id="0eab8-218">949</span><span class="sxs-lookup"><span data-stu-id="0eab8-218">949</span></span>        | <span data-ttu-id="0eab8-219">Corea (Shift – KSC 5601)</span><span class="sxs-lookup"><span data-stu-id="0eab8-219">Korea (Shift – KSC 5601)</span></span>   |
| <span data-ttu-id="0eab8-220">950</span><span class="sxs-lookup"><span data-stu-id="0eab8-220">950</span></span>        | <span data-ttu-id="0eab8-221">Taiwan (Big5)</span><span class="sxs-lookup"><span data-stu-id="0eab8-221">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="0eab8-222">1200</span><span class="sxs-lookup"><span data-stu-id="0eab8-222">1200</span></span>       | <span data-ttu-id="0eab8-223">Unicode</span><span class="sxs-lookup"><span data-stu-id="0eab8-223">Unicode</span></span>                    |
| <span data-ttu-id="0eab8-224">1250</span><span class="sxs-lookup"><span data-stu-id="0eab8-224">1250</span></span>       | <span data-ttu-id="0eab8-225">Latino 2 (Europa orientale)</span><span class="sxs-lookup"><span data-stu-id="0eab8-225">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="0eab8-226">1251</span><span class="sxs-lookup"><span data-stu-id="0eab8-226">1251</span></span>       | <span data-ttu-id="0eab8-227">Cirillico</span><span class="sxs-lookup"><span data-stu-id="0eab8-227">Cyrillic</span></span>                   |
| <span data-ttu-id="0eab8-228">1252</span><span class="sxs-lookup"><span data-stu-id="0eab8-228">1252</span></span>       | <span data-ttu-id="0eab8-229">Multilingue</span><span class="sxs-lookup"><span data-stu-id="0eab8-229">Multilingual</span></span>               |
| <span data-ttu-id="0eab8-230">1253</span><span class="sxs-lookup"><span data-stu-id="0eab8-230">1253</span></span>       | <span data-ttu-id="0eab8-231">Greco</span><span class="sxs-lookup"><span data-stu-id="0eab8-231">Greek</span></span>                      |
| <span data-ttu-id="0eab8-232">1254</span><span class="sxs-lookup"><span data-stu-id="0eab8-232">1254</span></span>       | <span data-ttu-id="0eab8-233">Turco</span><span class="sxs-lookup"><span data-stu-id="0eab8-233">Turkish</span></span>                    |
| <span data-ttu-id="0eab8-234">1255</span><span class="sxs-lookup"><span data-stu-id="0eab8-234">1255</span></span>       | <span data-ttu-id="0eab8-235">Ebraico</span><span class="sxs-lookup"><span data-stu-id="0eab8-235">Hebrew</span></span>                     |
| <span data-ttu-id="0eab8-236">1256</span><span class="sxs-lookup"><span data-stu-id="0eab8-236">1256</span></span>       | <span data-ttu-id="0eab8-237">Arabo</span><span class="sxs-lookup"><span data-stu-id="0eab8-237">Arabic</span></span>                     |



 

 

 





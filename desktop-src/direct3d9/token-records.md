---
description: In questa sezione viene descritto il formato dei record per ognuno dei token che portano a record. Le informazioni sono suddivise nelle sezioni riportate di seguito.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Record di token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304365"
---
# <a name="token-records"></a><span data-ttu-id="e9ed2-104">Record di token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-104">Token Records</span></span>

<span data-ttu-id="e9ed2-105">In questa sezione viene descritto il formato dei record per ognuno dei token che portano a record.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-105">This section describes the format of the records for each of the record-bearing tokens.</span></span> <span data-ttu-id="e9ed2-106">Le informazioni sono suddivise nelle sezioni riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-106">Information is divided into the following sections.</span></span>

-   [<span data-ttu-id="e9ed2-107">nome del TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-107">TOKEN\_NAME</span></span>](/windows)
-   [<span data-ttu-id="e9ed2-108">\_stringa token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-108">TOKEN\_STRING</span></span>](/windows)
-   [<span data-ttu-id="e9ed2-109">\_Integer token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-109">TOKEN\_INTEGER</span></span>](/windows)
-   [<span data-ttu-id="e9ed2-110">\_GUID token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-110">TOKEN\_GUID</span></span>](/windows)
-   [<span data-ttu-id="e9ed2-111">\_elenco di valori integer del token \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-111">TOKEN\_INTEGER\_LIST</span></span>](/windows)
-   [<span data-ttu-id="e9ed2-112">\_elenco float del token \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-112">TOKEN\_FLOAT\_LIST</span></span>](/windows)

## <a name="token_name"></a><span data-ttu-id="e9ed2-113">nome del TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-113">TOKEN\_NAME</span></span>

<span data-ttu-id="e9ed2-114">Record a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-114">A variable-length record.</span></span> <span data-ttu-id="e9ed2-115">Il token è seguito da un valore Count che specifica il numero di byte che seguono nel campo Name.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-115">The token is followed by a count value that specifies the number of bytes that follow in the name field.</span></span> <span data-ttu-id="e9ed2-116">Un nome ASCII con numero di lunghezza completa il record.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-116">An ASCII name of length count completes the record.</span></span>



| <span data-ttu-id="e9ed2-117">Campo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-117">Field</span></span> | <span data-ttu-id="e9ed2-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-118">Type</span></span>       | <span data-ttu-id="e9ed2-119">Dimensioni (byte)</span><span class="sxs-lookup"><span data-stu-id="e9ed2-119">Size (bytes)</span></span> | <span data-ttu-id="e9ed2-120">Contenuto</span><span class="sxs-lookup"><span data-stu-id="e9ed2-120">Contents</span></span>                       |
|-------|------------|--------------|--------------------------------|
| <span data-ttu-id="e9ed2-121">token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-121">token</span></span> | <span data-ttu-id="e9ed2-122">WORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-122">WORD</span></span>       | <span data-ttu-id="e9ed2-123">2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-123">2</span></span>            | <span data-ttu-id="e9ed2-124">nome del token \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-124">token\_name</span></span>                    |
| <span data-ttu-id="e9ed2-125">count</span><span class="sxs-lookup"><span data-stu-id="e9ed2-125">count</span></span> | <span data-ttu-id="e9ed2-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-126">DWORD</span></span>      | <span data-ttu-id="e9ed2-127">4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-127">4</span></span>            | <span data-ttu-id="e9ed2-128">Lunghezza del campo del nome, in byte</span><span class="sxs-lookup"><span data-stu-id="e9ed2-128">Length of name field, in bytes</span></span> |
| <span data-ttu-id="e9ed2-129">name</span><span class="sxs-lookup"><span data-stu-id="e9ed2-129">name</span></span>  | <span data-ttu-id="e9ed2-130">Matrice di BYTE</span><span class="sxs-lookup"><span data-stu-id="e9ed2-130">BYTE array</span></span> | <span data-ttu-id="e9ed2-131">count</span><span class="sxs-lookup"><span data-stu-id="e9ed2-131">count</span></span>        | <span data-ttu-id="e9ed2-132">Nome ASCII</span><span class="sxs-lookup"><span data-stu-id="e9ed2-132">ASCII name</span></span>                     |



 

## <a name="token_string"></a><span data-ttu-id="e9ed2-133">\_stringa token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-133">TOKEN\_STRING</span></span>

<span data-ttu-id="e9ed2-134">Record a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-134">A variable-length record.</span></span> <span data-ttu-id="e9ed2-135">Il token è seguito da un valore Count che specifica il numero di byte che seguono nel campo della stringa.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-135">The token is followed by a count value that specifies the number of bytes that follow in the string field.</span></span> <span data-ttu-id="e9ed2-136">Una stringa ASCII di lunghezza count continua il record, che viene completato da un token di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-136">An ASCII string of length count continues the record, which is completed by a terminating token.</span></span> <span data-ttu-id="e9ed2-137">La scelta del carattere di terminazione è determinata dai problemi di sintassi descritti altrove.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-137">The choice of terminator is determined by syntax issues discussed elsewhere.</span></span>



| <span data-ttu-id="e9ed2-138">Campo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-138">Field</span></span>      | <span data-ttu-id="e9ed2-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-139">Type</span></span>       | <span data-ttu-id="e9ed2-140">Dimensioni (byte)</span><span class="sxs-lookup"><span data-stu-id="e9ed2-140">Size (bytes)</span></span> | <span data-ttu-id="e9ed2-141">Contenuto</span><span class="sxs-lookup"><span data-stu-id="e9ed2-141">Contents</span></span>                         |
|------------|------------|--------------|----------------------------------|
| <span data-ttu-id="e9ed2-142">token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-142">token</span></span>      | <span data-ttu-id="e9ed2-143">WORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-143">WORD</span></span>       | <span data-ttu-id="e9ed2-144">2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-144">2</span></span>            | <span data-ttu-id="e9ed2-145">\_stringa token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-145">token\_string</span></span>                    |
| <span data-ttu-id="e9ed2-146">count</span><span class="sxs-lookup"><span data-stu-id="e9ed2-146">count</span></span>      | <span data-ttu-id="e9ed2-147">DWORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-147">DWORD</span></span>      | <span data-ttu-id="e9ed2-148">4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-148">4</span></span>            | <span data-ttu-id="e9ed2-149">Lunghezza del campo stringa in byte</span><span class="sxs-lookup"><span data-stu-id="e9ed2-149">Length of string field in bytes</span></span>  |
| <span data-ttu-id="e9ed2-150">Stringa</span><span class="sxs-lookup"><span data-stu-id="e9ed2-150">strinG</span></span>     | <span data-ttu-id="e9ed2-151">Matrice di BYTE</span><span class="sxs-lookup"><span data-stu-id="e9ed2-151">BYTE array</span></span> | <span data-ttu-id="e9ed2-152">count</span><span class="sxs-lookup"><span data-stu-id="e9ed2-152">count</span></span>        | <span data-ttu-id="e9ed2-153">Stringa ASCII</span><span class="sxs-lookup"><span data-stu-id="e9ed2-153">ASCII string</span></span>                     |
| <span data-ttu-id="e9ed2-154">terminazione</span><span class="sxs-lookup"><span data-stu-id="e9ed2-154">terminator</span></span> | <span data-ttu-id="e9ed2-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-155">DWORD</span></span>      | <span data-ttu-id="e9ed2-156">4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-156">4</span></span>            | <span data-ttu-id="e9ed2-157">punto e virgola del tOKEN \_ o \_ virgola del token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-157">tOKEN\_SEMICOLON or TOKEN\_COMMA</span></span> |



 

## <a name="token_integer"></a><span data-ttu-id="e9ed2-158">\_Integer token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-158">TOKEN\_INTEGER</span></span>

<span data-ttu-id="e9ed2-159">Record A lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-159">A fixed length record.</span></span> <span data-ttu-id="e9ed2-160">Il token è seguito dal valore Integer obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-160">The token is followed by the integer value required.</span></span>



| <span data-ttu-id="e9ed2-161">Campo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-161">Field</span></span> | <span data-ttu-id="e9ed2-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-162">Type</span></span>  | <span data-ttu-id="e9ed2-163">Dimensioni (byte)</span><span class="sxs-lookup"><span data-stu-id="e9ed2-163">Size (bytes)</span></span> | <span data-ttu-id="e9ed2-164">Contenuto</span><span class="sxs-lookup"><span data-stu-id="e9ed2-164">Contents</span></span>       |
|-------|-------|--------------|----------------|
| <span data-ttu-id="e9ed2-165">token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-165">token</span></span> | <span data-ttu-id="e9ed2-166">WORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-166">WORD</span></span>  | <span data-ttu-id="e9ed2-167">2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-167">2</span></span>            | <span data-ttu-id="e9ed2-168">\_Integer tOKEN</span><span class="sxs-lookup"><span data-stu-id="e9ed2-168">tOKEN\_INTEGER</span></span> |
| <span data-ttu-id="e9ed2-169">Valore</span><span class="sxs-lookup"><span data-stu-id="e9ed2-169">valuE</span></span> | <span data-ttu-id="e9ed2-170">DWORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-170">DWORD</span></span> | <span data-ttu-id="e9ed2-171">4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-171">4</span></span>            | <span data-ttu-id="e9ed2-172">Singolo Integer</span><span class="sxs-lookup"><span data-stu-id="e9ed2-172">Single integer</span></span> |



 

## <a name="token_guid"></a><span data-ttu-id="e9ed2-173">\_GUID token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-173">TOKEN\_GUID</span></span>

<span data-ttu-id="e9ed2-174">Record a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-174">A fixed-length record.</span></span> <span data-ttu-id="e9ed2-175">Il token è seguito dai quattro campi dati definiti dallo standard OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-175">The token is followed by the four data fields as defined by the OSF DCE standard.</span></span>



| <span data-ttu-id="e9ed2-176">Campo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-176">Field</span></span> | <span data-ttu-id="e9ed2-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-177">Type</span></span>       | <span data-ttu-id="e9ed2-178">Dimensioni (byte)</span><span class="sxs-lookup"><span data-stu-id="e9ed2-178">Size (bytes)</span></span> | <span data-ttu-id="e9ed2-179">Contenuto</span><span class="sxs-lookup"><span data-stu-id="e9ed2-179">Contents</span></span>          |
|-------|------------|--------------|-------------------|
| <span data-ttu-id="e9ed2-180">token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-180">token</span></span> | <span data-ttu-id="e9ed2-181">WORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-181">WORD</span></span>       | <span data-ttu-id="e9ed2-182">2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-182">2</span></span>            | <span data-ttu-id="e9ed2-183">\_GUID tOKEN</span><span class="sxs-lookup"><span data-stu-id="e9ed2-183">tOKEN\_GUID</span></span>       |
| <span data-ttu-id="e9ed2-184">Data1</span><span class="sxs-lookup"><span data-stu-id="e9ed2-184">Data1</span></span> | <span data-ttu-id="e9ed2-185">DWORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-185">DWORD</span></span>      | <span data-ttu-id="e9ed2-186">4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-186">4</span></span>            | <span data-ttu-id="e9ed2-187">Campo dati UUID 1</span><span class="sxs-lookup"><span data-stu-id="e9ed2-187">UUID data field 1</span></span> |
| <span data-ttu-id="e9ed2-188">Data2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-188">Data2</span></span> | <span data-ttu-id="e9ed2-189">WORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-189">WORD</span></span>       | <span data-ttu-id="e9ed2-190">2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-190">2</span></span>            | <span data-ttu-id="e9ed2-191">Campo dati UUID 2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-191">UUID data field 2</span></span> |
| <span data-ttu-id="e9ed2-192">Data3</span><span class="sxs-lookup"><span data-stu-id="e9ed2-192">Data3</span></span> | <span data-ttu-id="e9ed2-193">WORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-193">WORD</span></span>       | <span data-ttu-id="e9ed2-194">2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-194">2</span></span>            | <span data-ttu-id="e9ed2-195">Campo dati UUID 3</span><span class="sxs-lookup"><span data-stu-id="e9ed2-195">UUID data field 3</span></span> |
| <span data-ttu-id="e9ed2-196">DATA4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-196">Data4</span></span> | <span data-ttu-id="e9ed2-197">Matrice di BYTE</span><span class="sxs-lookup"><span data-stu-id="e9ed2-197">BYTE array</span></span> | <span data-ttu-id="e9ed2-198">8</span><span class="sxs-lookup"><span data-stu-id="e9ed2-198">8</span></span>            | <span data-ttu-id="e9ed2-199">Campo dati UUID 4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-199">UUID data field 4</span></span> |



 

## <a name="token_integer_list"></a><span data-ttu-id="e9ed2-200">\_elenco di valori integer del token \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-200">TOKEN\_INTEGER\_LIST</span></span>

<span data-ttu-id="e9ed2-201">Record a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-201">A variable-length record.</span></span> <span data-ttu-id="e9ed2-202">Il token è seguito da un valore Count che specifica il numero di numeri interi che seguono nel campo dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-202">The token is followed by a count value that specifies the number of integers that follow in the list field.</span></span> <span data-ttu-id="e9ed2-203">Per maggiore efficienza, gli elenchi di numeri interi consecutivi devono essere composti in un singolo elenco.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-203">For efficiency, consecutive integer lists should be compounded into a single list.</span></span>



| <span data-ttu-id="e9ed2-204">Campo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-204">Field</span></span> | <span data-ttu-id="e9ed2-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-205">Type</span></span>  | <span data-ttu-id="e9ed2-206">Dimensioni (byte)</span><span class="sxs-lookup"><span data-stu-id="e9ed2-206">Size (bytes)</span></span> | <span data-ttu-id="e9ed2-207">Contenuto</span><span class="sxs-lookup"><span data-stu-id="e9ed2-207">Contents</span></span>                         |
|-------|-------|--------------|----------------------------------|
| <span data-ttu-id="e9ed2-208">token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-208">token</span></span> | <span data-ttu-id="e9ed2-209">WORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-209">WORD</span></span>  | <span data-ttu-id="e9ed2-210">2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-210">2</span></span>            | <span data-ttu-id="e9ed2-211">\_elenco di valori integer del tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-211">tOKEN\_INTEGER\_LISt</span></span>             |
| <span data-ttu-id="e9ed2-212">count</span><span class="sxs-lookup"><span data-stu-id="e9ed2-212">count</span></span> | <span data-ttu-id="e9ed2-213">DWORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-213">DWORD</span></span> | <span data-ttu-id="e9ed2-214">4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-214">4</span></span>            | <span data-ttu-id="e9ed2-215">Numero di numeri interi nel campo elenco</span><span class="sxs-lookup"><span data-stu-id="e9ed2-215">Number of integers in list field</span></span> |
| <span data-ttu-id="e9ed2-216">list</span><span class="sxs-lookup"><span data-stu-id="e9ed2-216">list</span></span>  | <span data-ttu-id="e9ed2-217">DWORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-217">DWORD</span></span> | <span data-ttu-id="e9ed2-218">conteggio 4 x</span><span class="sxs-lookup"><span data-stu-id="e9ed2-218">4 x count</span></span>    | <span data-ttu-id="e9ed2-219">Elenco di numeri interi</span><span class="sxs-lookup"><span data-stu-id="e9ed2-219">Integer list</span></span>                     |



 

## <a name="token_float_list"></a><span data-ttu-id="e9ed2-220">\_elenco float del token \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-220">TOKEN\_FLOAT\_LIST</span></span>

<span data-ttu-id="e9ed2-221">Record a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-221">A variable-length record.</span></span> <span data-ttu-id="e9ed2-222">Il token è seguito da un valore Count che specifica il numero di valori float o Double che seguono nel campo dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-222">The token is followed by a count value that specifies the number of floats or doubles that follow in the list field.</span></span> <span data-ttu-id="e9ed2-223">Le dimensioni del valore a virgola mobile (float o Double) sono determinate dal valore di float SizeSpecified nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-223">The size of the floating point value (float or double) is determined by the value of float sizespecified in the file header.</span></span> <span data-ttu-id="e9ed2-224">Per maggiore efficienza, gli \_ elenchi float di token consecutivi \_ devono essere composti in un singolo elenco.</span><span class="sxs-lookup"><span data-stu-id="e9ed2-224">For efficiency, consecutive TOKEN\_FLOAT\_LISTs should be compounded into a single list.</span></span>



| <span data-ttu-id="e9ed2-225">Campo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-225">Field</span></span> | <span data-ttu-id="e9ed2-226">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9ed2-226">Type</span></span>               | <span data-ttu-id="e9ed2-227">Dimensioni (byte)</span><span class="sxs-lookup"><span data-stu-id="e9ed2-227">Size (bytes)</span></span>   | <span data-ttu-id="e9ed2-228">Contenuto</span><span class="sxs-lookup"><span data-stu-id="e9ed2-228">Contents</span></span>                                  |
|-------|--------------------|----------------|-------------------------------------------|
| <span data-ttu-id="e9ed2-229">token</span><span class="sxs-lookup"><span data-stu-id="e9ed2-229">token</span></span> | <span data-ttu-id="e9ed2-230">WORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-230">WORD</span></span>               | <span data-ttu-id="e9ed2-231">2</span><span class="sxs-lookup"><span data-stu-id="e9ed2-231">2</span></span>              | <span data-ttu-id="e9ed2-232">\_elenco float del tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="e9ed2-232">tOKEN\_FLOAT\_LISt</span></span>                        |
| <span data-ttu-id="e9ed2-233">count</span><span class="sxs-lookup"><span data-stu-id="e9ed2-233">count</span></span> | <span data-ttu-id="e9ed2-234">DWORD</span><span class="sxs-lookup"><span data-stu-id="e9ed2-234">DWORD</span></span>              | <span data-ttu-id="e9ed2-235">4</span><span class="sxs-lookup"><span data-stu-id="e9ed2-235">4</span></span>              | <span data-ttu-id="e9ed2-236">Numero di valori float o Double nel campo elenco</span><span class="sxs-lookup"><span data-stu-id="e9ed2-236">Number of floats or doubles in list field</span></span> |
| <span data-ttu-id="e9ed2-237">list</span><span class="sxs-lookup"><span data-stu-id="e9ed2-237">list</span></span>  | <span data-ttu-id="e9ed2-238">matrice float/double</span><span class="sxs-lookup"><span data-stu-id="e9ed2-238">float/double array</span></span> | <span data-ttu-id="e9ed2-239">conteggio 4 o 8 x</span><span class="sxs-lookup"><span data-stu-id="e9ed2-239">4 or 8 x count</span></span> | <span data-ttu-id="e9ed2-240">Elenco float o Double</span><span class="sxs-lookup"><span data-stu-id="e9ed2-240">Float or double list</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="e9ed2-241">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9ed2-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9ed2-242">Codifica binaria</span><span class="sxs-lookup"><span data-stu-id="e9ed2-242">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 

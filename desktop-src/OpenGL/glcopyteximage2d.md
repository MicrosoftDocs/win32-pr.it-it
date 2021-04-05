---
title: funzione glCopyTexImage2D (GL. h)
description: La funzione glCopyTexImage2D copia i pixel dal framebuffer in un'immagine di trama bidimensionale.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- funzione glCopyTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873973"
---
# <a name="glcopyteximage2d-function"></a><span data-ttu-id="10fd1-104">glCopyTexImage2D (funzione)</span><span class="sxs-lookup"><span data-stu-id="10fd1-104">glCopyTexImage2D function</span></span>

<span data-ttu-id="10fd1-105">La funzione **glCopyTexImage2D** copia i pixel dal framebuffer in un'immagine di trama bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="10fd1-105">The **glCopyTexImage2D** function copies pixels from the framebuffer into a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="10fd1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10fd1-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="10fd1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="10fd1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10fd1-108">*target*</span><span class="sxs-lookup"><span data-stu-id="10fd1-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="10fd1-109">Destinazione in cui verranno modificati i dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="10fd1-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="10fd1-110">Deve avere il valore di \_ trama GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="10fd1-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="10fd1-111">*level*</span><span class="sxs-lookup"><span data-stu-id="10fd1-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="10fd1-112">Numero del livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="10fd1-112">The level-of-detail number.</span></span> <span data-ttu-id="10fd1-113">Il livello 0 è l'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="10fd1-113">Level 0 is the base image.</span></span> <span data-ttu-id="10fd1-114">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="10fd1-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="10fd1-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="10fd1-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="10fd1-116">Il formato interno e la risoluzione dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="10fd1-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="10fd1-117">I valori 1, 2, 3 e 4 non sono accettati per *internalFormat*.</span><span class="sxs-lookup"><span data-stu-id="10fd1-117">The values 1, 2, 3, and 4 are not accepted for *internalFormat*.</span></span> <span data-ttu-id="10fd1-118">Il parametro può assumere uno dei seguenti valori simbolici.</span><span class="sxs-lookup"><span data-stu-id="10fd1-118">The parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="10fd1-119">Costante</span><span class="sxs-lookup"><span data-stu-id="10fd1-119">Constant</span></span>                 | <span data-ttu-id="10fd1-120">Bit R</span><span class="sxs-lookup"><span data-stu-id="10fd1-120">R Bits</span></span> | <span data-ttu-id="10fd1-121">Bit G</span><span class="sxs-lookup"><span data-stu-id="10fd1-121">G Bits</span></span> | <span data-ttu-id="10fd1-122">Bit B</span><span class="sxs-lookup"><span data-stu-id="10fd1-122">B Bits</span></span> | <span data-ttu-id="10fd1-123">Bit</span><span class="sxs-lookup"><span data-stu-id="10fd1-123">A Bits</span></span> | <span data-ttu-id="10fd1-124">Bit L</span><span class="sxs-lookup"><span data-stu-id="10fd1-124">L Bits</span></span> | <span data-ttu-id="10fd1-125">Bit I</span><span class="sxs-lookup"><span data-stu-id="10fd1-125">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="10fd1-126">\_alfa GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-126">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="10fd1-127">\_ALPHA4 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-127">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="10fd1-128">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-128">4</span></span>      |        |        |
| <span data-ttu-id="10fd1-129">\_ALPHA8 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-129">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="10fd1-130">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-130">8</span></span>      |        |        |
| <span data-ttu-id="10fd1-131">\_ALPHA12 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-131">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="10fd1-132">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-132">12</span></span>     |        |        |
| <span data-ttu-id="10fd1-133">\_ALPHA16 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-133">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="10fd1-134">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-134">16</span></span>     |        |        |
| <span data-ttu-id="10fd1-135">\_luminanza GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-135">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="10fd1-136">\_LUMINANCE4 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-136">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="10fd1-137">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-137">4</span></span>      |        |
| <span data-ttu-id="10fd1-138">\_LUMINANCE8 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-138">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="10fd1-139">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-139">8</span></span>      |        |
| <span data-ttu-id="10fd1-140">\_LUMINANCE12 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-140">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="10fd1-141">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-141">12</span></span>     |        |
| <span data-ttu-id="10fd1-142">\_LUMINANCE16 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-142">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="10fd1-143">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-143">16</span></span>     |        |
| <span data-ttu-id="10fd1-144">\_alfa luminanza GL \_</span><span class="sxs-lookup"><span data-stu-id="10fd1-144">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="10fd1-145">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="10fd1-145">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="10fd1-146">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-146">4</span></span>      | <span data-ttu-id="10fd1-147">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-147">4</span></span>      |        |
| <span data-ttu-id="10fd1-148">GL \_ LUMINANCE6 \_ alfa2</span><span class="sxs-lookup"><span data-stu-id="10fd1-148">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="10fd1-149">2</span><span class="sxs-lookup"><span data-stu-id="10fd1-149">2</span></span>      | <span data-ttu-id="10fd1-150">6</span><span class="sxs-lookup"><span data-stu-id="10fd1-150">6</span></span>      |        |
| <span data-ttu-id="10fd1-151">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="10fd1-151">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="10fd1-152">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-152">8</span></span>      | <span data-ttu-id="10fd1-153">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-153">8</span></span>      |        |
| <span data-ttu-id="10fd1-154">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="10fd1-154">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="10fd1-155">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-155">4</span></span>      | <span data-ttu-id="10fd1-156">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-156">12</span></span>     |        |
| <span data-ttu-id="10fd1-157">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="10fd1-157">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="10fd1-158">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-158">12</span></span>     | <span data-ttu-id="10fd1-159">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-159">12</span></span>     |        |
| <span data-ttu-id="10fd1-160">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="10fd1-160">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="10fd1-161">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-161">16</span></span>     | <span data-ttu-id="10fd1-162">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-162">16</span></span>     |        |
| <span data-ttu-id="10fd1-163">\_intensità GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-163">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="10fd1-164">\_INTENSITY4 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-164">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="10fd1-165">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-165">4</span></span>      |
| <span data-ttu-id="10fd1-166">\_INTENSITY8 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-166">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="10fd1-167">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-167">8</span></span>      |
| <span data-ttu-id="10fd1-168">\_INTENSITY12 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-168">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="10fd1-169">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-169">12</span></span>     |
| <span data-ttu-id="10fd1-170">\_INTENSITY16 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-170">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="10fd1-171">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-171">16</span></span>     |
| <span data-ttu-id="10fd1-172">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="10fd1-172">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="10fd1-173">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="10fd1-173">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="10fd1-174">3</span><span class="sxs-lookup"><span data-stu-id="10fd1-174">3</span></span>      | <span data-ttu-id="10fd1-175">3</span><span class="sxs-lookup"><span data-stu-id="10fd1-175">3</span></span>      | <span data-ttu-id="10fd1-176">2</span><span class="sxs-lookup"><span data-stu-id="10fd1-176">2</span></span>      |        |        |        |
| <span data-ttu-id="10fd1-177">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-177">GL\_RGB4</span></span>                 | <span data-ttu-id="10fd1-178">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-178">4</span></span>      | <span data-ttu-id="10fd1-179">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-179">4</span></span>      | <span data-ttu-id="10fd1-180">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-180">4</span></span>      |        |        |        |
| <span data-ttu-id="10fd1-181">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-181">GL\_RGB5</span></span>                 | <span data-ttu-id="10fd1-182">5</span><span class="sxs-lookup"><span data-stu-id="10fd1-182">5</span></span>      | <span data-ttu-id="10fd1-183">5</span><span class="sxs-lookup"><span data-stu-id="10fd1-183">5</span></span>      | <span data-ttu-id="10fd1-184">5</span><span class="sxs-lookup"><span data-stu-id="10fd1-184">5</span></span>      |        |        |        |
| <span data-ttu-id="10fd1-185">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-185">GL\_RGB8</span></span>                 | <span data-ttu-id="10fd1-186">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-186">8</span></span>      | <span data-ttu-id="10fd1-187">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-187">8</span></span>      | <span data-ttu-id="10fd1-188">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-188">8</span></span>      |        |        |        |
| <span data-ttu-id="10fd1-189">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-189">GL\_RGB10</span></span>                | <span data-ttu-id="10fd1-190">10</span><span class="sxs-lookup"><span data-stu-id="10fd1-190">10</span></span>     | <span data-ttu-id="10fd1-191">10</span><span class="sxs-lookup"><span data-stu-id="10fd1-191">10</span></span>     | <span data-ttu-id="10fd1-192">10</span><span class="sxs-lookup"><span data-stu-id="10fd1-192">10</span></span>     |        |        |        |
| <span data-ttu-id="10fd1-193">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-193">GL\_RGB12</span></span>                | <span data-ttu-id="10fd1-194">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-194">12</span></span>     | <span data-ttu-id="10fd1-195">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-195">12</span></span>     | <span data-ttu-id="10fd1-196">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-196">12</span></span>     |        |        |        |
| <span data-ttu-id="10fd1-197">\_Rgb16 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-197">GL\_RGB16</span></span>                | <span data-ttu-id="10fd1-198">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-198">16</span></span>     | <span data-ttu-id="10fd1-199">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-199">16</span></span>     | <span data-ttu-id="10fd1-200">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-200">16</span></span>     |        |        |        |
| <span data-ttu-id="10fd1-201">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-201">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="10fd1-202">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-202">GL\_RGBA2</span></span>                | <span data-ttu-id="10fd1-203">2</span><span class="sxs-lookup"><span data-stu-id="10fd1-203">2</span></span>      | <span data-ttu-id="10fd1-204">2</span><span class="sxs-lookup"><span data-stu-id="10fd1-204">2</span></span>      | <span data-ttu-id="10fd1-205">2</span><span class="sxs-lookup"><span data-stu-id="10fd1-205">2</span></span>      | <span data-ttu-id="10fd1-206">2</span><span class="sxs-lookup"><span data-stu-id="10fd1-206">2</span></span>      |        |        |
| <span data-ttu-id="10fd1-207">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-207">GL\_RGBA4</span></span>                | <span data-ttu-id="10fd1-208">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-208">4</span></span>      | <span data-ttu-id="10fd1-209">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-209">4</span></span>      | <span data-ttu-id="10fd1-210">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-210">4</span></span>      | <span data-ttu-id="10fd1-211">4</span><span class="sxs-lookup"><span data-stu-id="10fd1-211">4</span></span>      |        |        |
| <span data-ttu-id="10fd1-212">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="10fd1-212">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="10fd1-213">5</span><span class="sxs-lookup"><span data-stu-id="10fd1-213">5</span></span>      | <span data-ttu-id="10fd1-214">5</span><span class="sxs-lookup"><span data-stu-id="10fd1-214">5</span></span>      | <span data-ttu-id="10fd1-215">5</span><span class="sxs-lookup"><span data-stu-id="10fd1-215">5</span></span>      | <span data-ttu-id="10fd1-216">1</span><span class="sxs-lookup"><span data-stu-id="10fd1-216">1</span></span>      |        |        |
| <span data-ttu-id="10fd1-217">\_Rgba8 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-217">GL\_RGBA8</span></span>                | <span data-ttu-id="10fd1-218">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-218">8</span></span>      | <span data-ttu-id="10fd1-219">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-219">8</span></span>      | <span data-ttu-id="10fd1-220">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-220">8</span></span>      | <span data-ttu-id="10fd1-221">8</span><span class="sxs-lookup"><span data-stu-id="10fd1-221">8</span></span>      |        |        |
| <span data-ttu-id="10fd1-222">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="10fd1-222">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="10fd1-223">10</span><span class="sxs-lookup"><span data-stu-id="10fd1-223">10</span></span>     | <span data-ttu-id="10fd1-224">10</span><span class="sxs-lookup"><span data-stu-id="10fd1-224">10</span></span>     | <span data-ttu-id="10fd1-225">10</span><span class="sxs-lookup"><span data-stu-id="10fd1-225">10</span></span>     | <span data-ttu-id="10fd1-226">2</span><span class="sxs-lookup"><span data-stu-id="10fd1-226">2</span></span>      |        |        |
| <span data-ttu-id="10fd1-227">\_RGBA12 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-227">GL\_RGBA12</span></span>               | <span data-ttu-id="10fd1-228">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-228">12</span></span>     | <span data-ttu-id="10fd1-229">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-229">12</span></span>     | <span data-ttu-id="10fd1-230">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-230">12</span></span>     | <span data-ttu-id="10fd1-231">12</span><span class="sxs-lookup"><span data-stu-id="10fd1-231">12</span></span>     |        |        |
| <span data-ttu-id="10fd1-232">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="10fd1-232">GL\_RGBA16</span></span>               | <span data-ttu-id="10fd1-233">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-233">16</span></span>     | <span data-ttu-id="10fd1-234">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-234">16</span></span>     | <span data-ttu-id="10fd1-235">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-235">16</span></span>     | <span data-ttu-id="10fd1-236">16</span><span class="sxs-lookup"><span data-stu-id="10fd1-236">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="10fd1-237">*x*</span><span class="sxs-lookup"><span data-stu-id="10fd1-237">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="10fd1-238">Coordinata del piano x della finestra dell'angolo inferiore sinistro dell'area rettangolare dei pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="10fd1-238">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="10fd1-239">*y*</span><span class="sxs-lookup"><span data-stu-id="10fd1-239">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="10fd1-240">Coordinata del piano y della finestra dell'angolo inferiore sinistro dell'area rettangolare dei pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="10fd1-240">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="10fd1-241">*width*</span><span class="sxs-lookup"><span data-stu-id="10fd1-241">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="10fd1-242">Larghezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="10fd1-242">The width of the texture image.</span></span> <span data-ttu-id="10fd1-243">Deve essere \* un *bordo* di 2n + 2 per alcuni numeri interi *n*.</span><span class="sxs-lookup"><span data-stu-id="10fd1-243">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="10fd1-244">*height*</span><span class="sxs-lookup"><span data-stu-id="10fd1-244">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="10fd1-245">Altezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="10fd1-245">The height of the texture image.</span></span> <span data-ttu-id="10fd1-246">Deve essere \* un *bordo* di 2n + 2 per alcuni numeri interi *n*.</span><span class="sxs-lookup"><span data-stu-id="10fd1-246">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="10fd1-247">*bordo*</span><span class="sxs-lookup"><span data-stu-id="10fd1-247">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="10fd1-248">Larghezza del bordo.</span><span class="sxs-lookup"><span data-stu-id="10fd1-248">The width of the border.</span></span> <span data-ttu-id="10fd1-249">Deve essere zero o 1.</span><span class="sxs-lookup"><span data-stu-id="10fd1-249">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10fd1-250">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10fd1-250">Return value</span></span>

<span data-ttu-id="10fd1-251">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="10fd1-251">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10fd1-252">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="10fd1-252">Error codes</span></span>

<span data-ttu-id="10fd1-253">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="10fd1-253">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="10fd1-254">Nome</span><span class="sxs-lookup"><span data-stu-id="10fd1-254">Name</span></span>                                                                                                  | <span data-ttu-id="10fd1-255">Significato</span><span class="sxs-lookup"><span data-stu-id="10fd1-255">Meaning</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10fd1-256"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10fd1-256"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="10fd1-257">*target* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="10fd1-257">*target* was not an accepted value.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="10fd1-258"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10fd1-258"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="10fd1-259">il *livello* è minore di zero o maggiore di log2 *Max*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="10fd1-259">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                               |
| <dl> <span data-ttu-id="10fd1-260"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10fd1-260"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="10fd1-261">il *bordo* non è zero o 1.</span><span class="sxs-lookup"><span data-stu-id="10fd1-261">*border* was not zero or 1.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="10fd1-262"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10fd1-262"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="10fd1-263">*Width* è minore di zero, maggiore di 2 + GL \_ \_ dimensione della trama max \_ oppure la *larghezza* non può essere rappresentata come il bordo 2n + 2 \*  per alcuni numeri interi *n*.</span><span class="sxs-lookup"><span data-stu-id="10fd1-263">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n + 2 \* *border* for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="10fd1-264"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10fd1-264"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="10fd1-265">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="10fd1-265">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="10fd1-266">Commenti</span><span class="sxs-lookup"><span data-stu-id="10fd1-266">Remarks</span></span>

<span data-ttu-id="10fd1-267">La funzione **glCopyTexImage2D** definisce un'immagine di trama bidimensionale usando i pixel del framebuffer corrente, anziché dalla memoria principale come nel caso di [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="10fd1-267">The **glCopyTexImage2D** function defines a two-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage2D**](glteximage2d.md).</span></span>

<span data-ttu-id="10fd1-268">Usando il livello mipmap specificato con *Level*, le matrici di trama sono definite come un rettangolo di pixel con l'angolo inferiore sinistro posizionato in corrispondenza delle coordinate *x* e *y*, Width uguale a *Width* + (2 \* *Border*) e un'altezza uguale all' *altezza* + (2 \* *bordo*).</span><span class="sxs-lookup"><span data-stu-id="10fd1-268">Using the mipmap level specified with *level*, texture arrays are defined as a rectangle of pixels with the lower-left corner located at the coordinates *x* and *y*, width equal to *width* + (2 \* *border*), and a height equal to *height* + (2 \* *border*).</span></span> <span data-ttu-id="10fd1-269">Il formato interno della matrice di trama viene specificato con il parametro *internalFormat* .</span><span class="sxs-lookup"><span data-stu-id="10fd1-269">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="10fd1-270">La funzione **glCopyTexImage2D** elabora i pixel in una riga allo stesso modo di [**glCopyPixels**](glcopypixels.md) , ad eccezione del fatto che prima della conversione finale dei pixel, tutti i valori dei componenti pixel vengono fissati all'intervallo \[ 0, 1 \] e vengono convertiti nel formato interno della trama per l'archiviazione nella matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="10fd1-270">The **glCopyTexImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="10fd1-271">L'ordinamento dei pixel è determinato dalle coordinate *x* e *y* inferiori corrispondenti alle coordinate di trama *s* e *t* inferiori.</span><span class="sxs-lookup"><span data-stu-id="10fd1-271">Pixel ordering is determined with lower *x* and *y* coordinates corresponding to lower *s* and *t* texture coordinates.</span></span> <span data-ttu-id="10fd1-272">Se uno dei pixel all'interno di una riga specificata del framebuffer corrente è esterno alla finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="10fd1-272">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="10fd1-273">Non è possibile includere chiamate a **glCopyTexImage2D** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="10fd1-273">You cannot include calls to **glCopyTexImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="10fd1-274">La funzione **glCopyTexImage2D** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="10fd1-274">The **glCopyTexImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="10fd1-275">La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.</span><span class="sxs-lookup"><span data-stu-id="10fd1-275">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="10fd1-276">Le funzioni [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono su [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="10fd1-276">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="10fd1-277">La funzione seguente recupera le informazioni correlate a **glCopyTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="10fd1-277">The following function retrieves information related to **glCopyTexImage2D**:</span></span>

<span data-ttu-id="10fd1-278">[**glIsEnabled**](glisenabled.md) con argomento di \_ trama GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="10fd1-278">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="10fd1-279">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10fd1-279">Requirements</span></span>



| <span data-ttu-id="10fd1-280">Requisito</span><span class="sxs-lookup"><span data-stu-id="10fd1-280">Requirement</span></span> | <span data-ttu-id="10fd1-281">Valore</span><span class="sxs-lookup"><span data-stu-id="10fd1-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10fd1-282">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10fd1-282">Minimum supported client</span></span><br/> | <span data-ttu-id="10fd1-283">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="10fd1-283">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="10fd1-284">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10fd1-284">Minimum supported server</span></span><br/> | <span data-ttu-id="10fd1-285">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="10fd1-285">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="10fd1-286">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10fd1-286">Header</span></span><br/>                   | <dl> <span data-ttu-id="10fd1-287"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="10fd1-287"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="10fd1-288">Libreria</span><span class="sxs-lookup"><span data-stu-id="10fd1-288">Library</span></span><br/>                  | <dl> <span data-ttu-id="10fd1-289"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10fd1-289"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="10fd1-290">DLL</span><span class="sxs-lookup"><span data-stu-id="10fd1-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10fd1-291"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10fd1-291"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fd1-292">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10fd1-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fd1-293">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="10fd1-293">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="10fd1-294">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="10fd1-294">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="10fd1-295">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="10fd1-295">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="10fd1-296">**Remo**</span><span class="sxs-lookup"><span data-stu-id="10fd1-296">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="10fd1-297">**glFog**</span><span class="sxs-lookup"><span data-stu-id="10fd1-297">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="10fd1-298">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="10fd1-298">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="10fd1-299">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="10fd1-299">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="10fd1-300">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="10fd1-300">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="10fd1-301">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="10fd1-301">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="10fd1-302">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="10fd1-302">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="10fd1-303">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="10fd1-303">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="10fd1-304">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="10fd1-304">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 






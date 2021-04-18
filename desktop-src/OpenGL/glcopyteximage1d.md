---
title: funzione glCopyTexImage1D (GL. h)
description: La funzione glCopyTexImage1D copia i pixel dal framebuffer in un'immagine di trama unidimensionale.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- funzione glCopyTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301926"
---
# <a name="glcopyteximage1d-function"></a><span data-ttu-id="1647f-104">glCopyTexImage1D (funzione)</span><span class="sxs-lookup"><span data-stu-id="1647f-104">glCopyTexImage1D function</span></span>

<span data-ttu-id="1647f-105">La funzione **glCopyTexImage1D** copia i pixel dal framebuffer in un'immagine di trama unidimensionale.</span><span class="sxs-lookup"><span data-stu-id="1647f-105">The **glCopyTexImage1D** function copies pixels from the framebuffer into a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="1647f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1647f-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="1647f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1647f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1647f-108">*target*</span><span class="sxs-lookup"><span data-stu-id="1647f-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="1647f-109">Destinazione per cui verranno modificati i dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1647f-109">The target for which the image data will be changed.</span></span> <span data-ttu-id="1647f-110">Deve avere il valore GL \_ texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="1647f-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="1647f-111">*level*</span><span class="sxs-lookup"><span data-stu-id="1647f-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="1647f-112">Numero del livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="1647f-112">The level-of-detail number.</span></span> <span data-ttu-id="1647f-113">Il livello 0 è l'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="1647f-113">Level 0 is the base image.</span></span> <span data-ttu-id="1647f-114">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="1647f-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="1647f-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="1647f-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="1647f-116">Il formato interno e la risoluzione dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="1647f-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="1647f-117">Questo parametro deve essere uno dei seguenti valori simbolici.</span><span class="sxs-lookup"><span data-stu-id="1647f-117">This parameter must be one of the following symbolic values.</span></span>



| <span data-ttu-id="1647f-118">Costante</span><span class="sxs-lookup"><span data-stu-id="1647f-118">Constant</span></span>                 | <span data-ttu-id="1647f-119">Bit R</span><span class="sxs-lookup"><span data-stu-id="1647f-119">R Bits</span></span> | <span data-ttu-id="1647f-120">Bit G</span><span class="sxs-lookup"><span data-stu-id="1647f-120">G Bits</span></span> | <span data-ttu-id="1647f-121">Bit B</span><span class="sxs-lookup"><span data-stu-id="1647f-121">B Bits</span></span> | <span data-ttu-id="1647f-122">Bit</span><span class="sxs-lookup"><span data-stu-id="1647f-122">A Bits</span></span> | <span data-ttu-id="1647f-123">Bit L</span><span class="sxs-lookup"><span data-stu-id="1647f-123">L Bits</span></span> | <span data-ttu-id="1647f-124">Bit I</span><span class="sxs-lookup"><span data-stu-id="1647f-124">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="1647f-125">\_alfa GL</span><span class="sxs-lookup"><span data-stu-id="1647f-125">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="1647f-126">\_ALPHA4 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-126">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="1647f-127">4</span><span class="sxs-lookup"><span data-stu-id="1647f-127">4</span></span>      |        |        |
| <span data-ttu-id="1647f-128">\_ALPHA8 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-128">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="1647f-129">8</span><span class="sxs-lookup"><span data-stu-id="1647f-129">8</span></span>      |        |        |
| <span data-ttu-id="1647f-130">\_ALPHA12 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-130">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="1647f-131">12</span><span class="sxs-lookup"><span data-stu-id="1647f-131">12</span></span>     |        |        |
| <span data-ttu-id="1647f-132">\_ALPHA16 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-132">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="1647f-133">16</span><span class="sxs-lookup"><span data-stu-id="1647f-133">16</span></span>     |        |        |
| <span data-ttu-id="1647f-134">\_luminanza GL</span><span class="sxs-lookup"><span data-stu-id="1647f-134">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="1647f-135">\_LUMINANCE4 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-135">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="1647f-136">4</span><span class="sxs-lookup"><span data-stu-id="1647f-136">4</span></span>      |        |
| <span data-ttu-id="1647f-137">\_LUMINANCE8 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-137">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="1647f-138">8</span><span class="sxs-lookup"><span data-stu-id="1647f-138">8</span></span>      |        |
| <span data-ttu-id="1647f-139">\_LUMINANCE12 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-139">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="1647f-140">12</span><span class="sxs-lookup"><span data-stu-id="1647f-140">12</span></span>     |        |
| <span data-ttu-id="1647f-141">\_LUMINANCE16 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-141">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="1647f-142">16</span><span class="sxs-lookup"><span data-stu-id="1647f-142">16</span></span>     |        |
| <span data-ttu-id="1647f-143">\_alfa luminanza GL \_</span><span class="sxs-lookup"><span data-stu-id="1647f-143">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="1647f-144">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="1647f-144">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="1647f-145">4</span><span class="sxs-lookup"><span data-stu-id="1647f-145">4</span></span>      | <span data-ttu-id="1647f-146">4</span><span class="sxs-lookup"><span data-stu-id="1647f-146">4</span></span>      |        |
| <span data-ttu-id="1647f-147">GL \_ LUMINANCE6 \_ alfa2</span><span class="sxs-lookup"><span data-stu-id="1647f-147">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="1647f-148">2</span><span class="sxs-lookup"><span data-stu-id="1647f-148">2</span></span>      | <span data-ttu-id="1647f-149">6</span><span class="sxs-lookup"><span data-stu-id="1647f-149">6</span></span>      |        |
| <span data-ttu-id="1647f-150">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="1647f-150">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="1647f-151">8</span><span class="sxs-lookup"><span data-stu-id="1647f-151">8</span></span>      | <span data-ttu-id="1647f-152">8</span><span class="sxs-lookup"><span data-stu-id="1647f-152">8</span></span>      |        |
| <span data-ttu-id="1647f-153">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="1647f-153">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="1647f-154">4</span><span class="sxs-lookup"><span data-stu-id="1647f-154">4</span></span>      | <span data-ttu-id="1647f-155">12</span><span class="sxs-lookup"><span data-stu-id="1647f-155">12</span></span>     |        |
| <span data-ttu-id="1647f-156">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="1647f-156">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="1647f-157">12</span><span class="sxs-lookup"><span data-stu-id="1647f-157">12</span></span>     | <span data-ttu-id="1647f-158">12</span><span class="sxs-lookup"><span data-stu-id="1647f-158">12</span></span>     |        |
| <span data-ttu-id="1647f-159">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="1647f-159">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="1647f-160">16</span><span class="sxs-lookup"><span data-stu-id="1647f-160">16</span></span>     | <span data-ttu-id="1647f-161">16</span><span class="sxs-lookup"><span data-stu-id="1647f-161">16</span></span>     |        |
| <span data-ttu-id="1647f-162">\_intensità GL</span><span class="sxs-lookup"><span data-stu-id="1647f-162">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="1647f-163">\_INTENSITY4 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-163">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="1647f-164">4</span><span class="sxs-lookup"><span data-stu-id="1647f-164">4</span></span>      |
| <span data-ttu-id="1647f-165">\_INTENSITY8 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-165">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="1647f-166">8</span><span class="sxs-lookup"><span data-stu-id="1647f-166">8</span></span>      |
| <span data-ttu-id="1647f-167">\_INTENSITY12 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-167">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="1647f-168">12</span><span class="sxs-lookup"><span data-stu-id="1647f-168">12</span></span>     |
| <span data-ttu-id="1647f-169">\_INTENSITY16 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-169">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="1647f-170">16</span><span class="sxs-lookup"><span data-stu-id="1647f-170">16</span></span>     |
| <span data-ttu-id="1647f-171">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="1647f-171">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="1647f-172">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="1647f-172">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="1647f-173">3</span><span class="sxs-lookup"><span data-stu-id="1647f-173">3</span></span>      | <span data-ttu-id="1647f-174">3</span><span class="sxs-lookup"><span data-stu-id="1647f-174">3</span></span>      | <span data-ttu-id="1647f-175">2</span><span class="sxs-lookup"><span data-stu-id="1647f-175">2</span></span>      |        |        |        |
| <span data-ttu-id="1647f-176">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-176">GL\_RGB4</span></span>                 | <span data-ttu-id="1647f-177">4</span><span class="sxs-lookup"><span data-stu-id="1647f-177">4</span></span>      | <span data-ttu-id="1647f-178">4</span><span class="sxs-lookup"><span data-stu-id="1647f-178">4</span></span>      | <span data-ttu-id="1647f-179">4</span><span class="sxs-lookup"><span data-stu-id="1647f-179">4</span></span>      |        |        |        |
| <span data-ttu-id="1647f-180">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-180">GL\_RGB5</span></span>                 | <span data-ttu-id="1647f-181">5</span><span class="sxs-lookup"><span data-stu-id="1647f-181">5</span></span>      | <span data-ttu-id="1647f-182">5</span><span class="sxs-lookup"><span data-stu-id="1647f-182">5</span></span>      | <span data-ttu-id="1647f-183">5</span><span class="sxs-lookup"><span data-stu-id="1647f-183">5</span></span>      |        |        |        |
| <span data-ttu-id="1647f-184">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-184">GL\_RGB8</span></span>                 | <span data-ttu-id="1647f-185">8</span><span class="sxs-lookup"><span data-stu-id="1647f-185">8</span></span>      | <span data-ttu-id="1647f-186">8</span><span class="sxs-lookup"><span data-stu-id="1647f-186">8</span></span>      | <span data-ttu-id="1647f-187">8</span><span class="sxs-lookup"><span data-stu-id="1647f-187">8</span></span>      |        |        |        |
| <span data-ttu-id="1647f-188">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-188">GL\_RGB10</span></span>                | <span data-ttu-id="1647f-189">10</span><span class="sxs-lookup"><span data-stu-id="1647f-189">10</span></span>     | <span data-ttu-id="1647f-190">10</span><span class="sxs-lookup"><span data-stu-id="1647f-190">10</span></span>     | <span data-ttu-id="1647f-191">10</span><span class="sxs-lookup"><span data-stu-id="1647f-191">10</span></span>     |        |        |        |
| <span data-ttu-id="1647f-192">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-192">GL\_RGB12</span></span>                | <span data-ttu-id="1647f-193">12</span><span class="sxs-lookup"><span data-stu-id="1647f-193">12</span></span>     | <span data-ttu-id="1647f-194">12</span><span class="sxs-lookup"><span data-stu-id="1647f-194">12</span></span>     | <span data-ttu-id="1647f-195">12</span><span class="sxs-lookup"><span data-stu-id="1647f-195">12</span></span>     |        |        |        |
| <span data-ttu-id="1647f-196">\_Rgb16 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-196">GL\_RGB16</span></span>                | <span data-ttu-id="1647f-197">16</span><span class="sxs-lookup"><span data-stu-id="1647f-197">16</span></span>     | <span data-ttu-id="1647f-198">16</span><span class="sxs-lookup"><span data-stu-id="1647f-198">16</span></span>     | <span data-ttu-id="1647f-199">16</span><span class="sxs-lookup"><span data-stu-id="1647f-199">16</span></span>     |        |        |        |
| <span data-ttu-id="1647f-200">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="1647f-200">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="1647f-201">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-201">GL\_RGBA2</span></span>                | <span data-ttu-id="1647f-202">2</span><span class="sxs-lookup"><span data-stu-id="1647f-202">2</span></span>      | <span data-ttu-id="1647f-203">2</span><span class="sxs-lookup"><span data-stu-id="1647f-203">2</span></span>      | <span data-ttu-id="1647f-204">2</span><span class="sxs-lookup"><span data-stu-id="1647f-204">2</span></span>      | <span data-ttu-id="1647f-205">2</span><span class="sxs-lookup"><span data-stu-id="1647f-205">2</span></span>      |        |        |
| <span data-ttu-id="1647f-206">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-206">GL\_RGBA4</span></span>                | <span data-ttu-id="1647f-207">4</span><span class="sxs-lookup"><span data-stu-id="1647f-207">4</span></span>      | <span data-ttu-id="1647f-208">4</span><span class="sxs-lookup"><span data-stu-id="1647f-208">4</span></span>      | <span data-ttu-id="1647f-209">4</span><span class="sxs-lookup"><span data-stu-id="1647f-209">4</span></span>      | <span data-ttu-id="1647f-210">4</span><span class="sxs-lookup"><span data-stu-id="1647f-210">4</span></span>      |        |        |
| <span data-ttu-id="1647f-211">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="1647f-211">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="1647f-212">5</span><span class="sxs-lookup"><span data-stu-id="1647f-212">5</span></span>      | <span data-ttu-id="1647f-213">5</span><span class="sxs-lookup"><span data-stu-id="1647f-213">5</span></span>      | <span data-ttu-id="1647f-214">5</span><span class="sxs-lookup"><span data-stu-id="1647f-214">5</span></span>      | <span data-ttu-id="1647f-215">1</span><span class="sxs-lookup"><span data-stu-id="1647f-215">1</span></span>      |        |        |
| <span data-ttu-id="1647f-216">\_Rgba8 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-216">GL\_RGBA8</span></span>                | <span data-ttu-id="1647f-217">8</span><span class="sxs-lookup"><span data-stu-id="1647f-217">8</span></span>      | <span data-ttu-id="1647f-218">8</span><span class="sxs-lookup"><span data-stu-id="1647f-218">8</span></span>      | <span data-ttu-id="1647f-219">8</span><span class="sxs-lookup"><span data-stu-id="1647f-219">8</span></span>      | <span data-ttu-id="1647f-220">8</span><span class="sxs-lookup"><span data-stu-id="1647f-220">8</span></span>      |        |        |
| <span data-ttu-id="1647f-221">GL \_ RGB10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="1647f-221">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="1647f-222">10</span><span class="sxs-lookup"><span data-stu-id="1647f-222">10</span></span>     | <span data-ttu-id="1647f-223">10</span><span class="sxs-lookup"><span data-stu-id="1647f-223">10</span></span>     | <span data-ttu-id="1647f-224">10</span><span class="sxs-lookup"><span data-stu-id="1647f-224">10</span></span>     | <span data-ttu-id="1647f-225">2</span><span class="sxs-lookup"><span data-stu-id="1647f-225">2</span></span>      |        |        |
| <span data-ttu-id="1647f-226">\_RGBA12 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-226">GL\_RGBA12</span></span>               | <span data-ttu-id="1647f-227">12</span><span class="sxs-lookup"><span data-stu-id="1647f-227">12</span></span>     | <span data-ttu-id="1647f-228">12</span><span class="sxs-lookup"><span data-stu-id="1647f-228">12</span></span>     | <span data-ttu-id="1647f-229">12</span><span class="sxs-lookup"><span data-stu-id="1647f-229">12</span></span>     | <span data-ttu-id="1647f-230">12</span><span class="sxs-lookup"><span data-stu-id="1647f-230">12</span></span>     |        |        |
| <span data-ttu-id="1647f-231">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="1647f-231">GL\_RGBA16</span></span>               | <span data-ttu-id="1647f-232">16</span><span class="sxs-lookup"><span data-stu-id="1647f-232">16</span></span>     | <span data-ttu-id="1647f-233">16</span><span class="sxs-lookup"><span data-stu-id="1647f-233">16</span></span>     | <span data-ttu-id="1647f-234">16</span><span class="sxs-lookup"><span data-stu-id="1647f-234">16</span></span>     | <span data-ttu-id="1647f-235">16</span><span class="sxs-lookup"><span data-stu-id="1647f-235">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="1647f-236">*x*</span><span class="sxs-lookup"><span data-stu-id="1647f-236">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="1647f-237">Coordinata del piano x della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="1647f-237">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="1647f-238">*y*</span><span class="sxs-lookup"><span data-stu-id="1647f-238">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="1647f-239">Coordinata del piano y della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="1647f-239">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="1647f-240">*width*</span><span class="sxs-lookup"><span data-stu-id="1647f-240">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="1647f-241">Larghezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="1647f-241">The width of the texture image.</span></span> <span data-ttu-id="1647f-242">Deve essere zero o 2n + 2 (*bordo*) per alcuni numeri interi *n*.</span><span class="sxs-lookup"><span data-stu-id="1647f-242">Must be zero or 2n + 2(*border*) for some integer *n*.</span></span> <span data-ttu-id="1647f-243">L'altezza dell'immagine della trama è 1.</span><span class="sxs-lookup"><span data-stu-id="1647f-243">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="1647f-244">*bordo*</span><span class="sxs-lookup"><span data-stu-id="1647f-244">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="1647f-245">Larghezza del bordo.</span><span class="sxs-lookup"><span data-stu-id="1647f-245">The width of the border.</span></span> <span data-ttu-id="1647f-246">Deve essere zero o 1.</span><span class="sxs-lookup"><span data-stu-id="1647f-246">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1647f-247">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1647f-247">Return value</span></span>

<span data-ttu-id="1647f-248">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1647f-248">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1647f-249">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="1647f-249">Error codes</span></span>

<span data-ttu-id="1647f-250">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1647f-250">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1647f-251">Nome</span><span class="sxs-lookup"><span data-stu-id="1647f-251">Name</span></span>                                                                                                  | <span data-ttu-id="1647f-252">Significato</span><span class="sxs-lookup"><span data-stu-id="1647f-252">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1647f-253"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1647f-253"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1647f-254">*target* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="1647f-254">*target* was not an accepted value.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="1647f-255"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1647f-255"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1647f-256">il *livello* è minore di zero o maggiore di log2 *Max*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1647f-256">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                           |
| <dl> <span data-ttu-id="1647f-257"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1647f-257"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1647f-258">il *bordo* non è zero o 1.</span><span class="sxs-lookup"><span data-stu-id="1647f-258">*border* was not zero or 1.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="1647f-259"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1647f-259"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1647f-260">*Width* è minore di zero, maggiore di 2 + GL \_ \_ dimensione della trama max \_ oppure la *larghezza* non può essere rappresentata come 2n + (*bordo*) per alcuni numeri interi *n*.</span><span class="sxs-lookup"><span data-stu-id="1647f-260">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n +(*border*) for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="1647f-261"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1647f-261"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1647f-262">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1647f-262">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="1647f-263">Commenti</span><span class="sxs-lookup"><span data-stu-id="1647f-263">Remarks</span></span>

<span data-ttu-id="1647f-264">La funzione **glCopyTexImage1D** definisce un'immagine di trama unidimensionale usando i pixel del framebuffer corrente, anziché dalla memoria principale come nel caso di [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="1647f-264">The **glCopyTexImage1D** function defines a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage1D**](glteximage1d.md).</span></span>

<span data-ttu-id="1647f-265">Usando il livello mipmap specificato con *Level*, le matrici di trama sono definite come una riga in pixel allineata all'angolo inferiore sinistro della finestra in corrispondenza delle coordinate specificate da *x* e *y*, con una lunghezza uguale a *Width* + 2 \* *Border*.</span><span class="sxs-lookup"><span data-stu-id="1647f-265">Using the mipmap level specified with *level*, texture arrays are defined as a pixel row aligned with the lower-left corner of the window at the coordinates specified by *x* and *y*, with a length equal to *width* + 2 \* *border*.</span></span> <span data-ttu-id="1647f-266">Il formato interno della matrice di trama viene specificato con il parametro *internalFormat* .</span><span class="sxs-lookup"><span data-stu-id="1647f-266">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="1647f-267">La funzione **glCopyTexImage1D** elabora i pixel in una riga nello stesso modo in cui si trova [**glCopyPixels**](glcopypixels.md), ad eccezione del fatto che prima della conversione finale dei pixel, tutti i valori dei componenti pixel vengono bloccati nell'intervallo \[ 0, 1 \] e vengono convertiti nel formato interno della trama per l'archiviazione nella matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="1647f-267">The **glCopyTexImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="1647f-268">L'ordinamento dei pixel è determinato da coordinate *x* inferiori corrispondenti a coordinate di trama inferiori.</span><span class="sxs-lookup"><span data-stu-id="1647f-268">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="1647f-269">Se uno dei pixel all'interno di una riga specificata del framebuffer corrente è esterno alla finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="1647f-269">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="1647f-270">Non è possibile includere chiamate a **glCopyTexImage1D** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1647f-270">You cannot include calls to **glCopyTexImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="1647f-271">La funzione **glCopyTexImage1D** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="1647f-271">The **glCopyTexImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="1647f-272">La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.</span><span class="sxs-lookup"><span data-stu-id="1647f-272">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="1647f-273">Le funzioni [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono su [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="1647f-273">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="1647f-274">La funzione seguente recupera le informazioni correlate a **glCopyTexImage1D**:</span><span class="sxs-lookup"><span data-stu-id="1647f-274">The following function retrieves information related to **glCopyTexImage1D**:</span></span>

<span data-ttu-id="1647f-275">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="1647f-275">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="1647f-276">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1647f-276">Requirements</span></span>



| <span data-ttu-id="1647f-277">Requisito</span><span class="sxs-lookup"><span data-stu-id="1647f-277">Requirement</span></span> | <span data-ttu-id="1647f-278">Valore</span><span class="sxs-lookup"><span data-stu-id="1647f-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1647f-279">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1647f-279">Minimum supported client</span></span><br/> | <span data-ttu-id="1647f-280">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1647f-280">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1647f-281">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1647f-281">Minimum supported server</span></span><br/> | <span data-ttu-id="1647f-282">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1647f-282">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1647f-283">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1647f-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="1647f-284"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1647f-284"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1647f-285">Libreria</span><span class="sxs-lookup"><span data-stu-id="1647f-285">Library</span></span><br/>                  | <dl> <span data-ttu-id="1647f-286"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1647f-286"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1647f-287">DLL</span><span class="sxs-lookup"><span data-stu-id="1647f-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1647f-288"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1647f-288"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1647f-289">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1647f-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1647f-290">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="1647f-290">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="1647f-291">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1647f-291">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1647f-292">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="1647f-292">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="1647f-293">**glFog**</span><span class="sxs-lookup"><span data-stu-id="1647f-293">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="1647f-294">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="1647f-294">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="1647f-295">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="1647f-295">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="1647f-296">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="1647f-296">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="1647f-297">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="1647f-297">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="1647f-298">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1647f-298">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1647f-299">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1647f-299">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1647f-300">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="1647f-300">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 






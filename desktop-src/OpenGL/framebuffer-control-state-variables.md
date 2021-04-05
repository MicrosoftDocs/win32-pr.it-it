---
title: Variabili di stato del controllo framebuffer
description: Variabili di stato del controllo framebuffer
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variabili di stato del controllo framebuffer OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857073"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="63140-104">Variabili di stato del controllo framebuffer</span><span class="sxs-lookup"><span data-stu-id="63140-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="63140-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_buffer di disegni GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="63140-106">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-106">Description:</span></span>     | <span data-ttu-id="63140-107">Buffer selezionati per il disegno</span><span class="sxs-lookup"><span data-stu-id="63140-107">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="63140-108">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-108">Attribute group:</span></span> | <span data-ttu-id="63140-109">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="63140-109">color-buffer</span></span>                           |
| <span data-ttu-id="63140-110">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-110">Initial value:</span></span>   |                                        |
| <span data-ttu-id="63140-111">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-111">Get command:</span></span>     | [<span data-ttu-id="63140-112">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="63140-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="63140-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_WRITEMASK indice \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63140-114">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-114">Description:</span></span>     | <span data-ttu-id="63140-115">Writemask indice colori</span><span class="sxs-lookup"><span data-stu-id="63140-115">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="63140-116">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-116">Attribute group:</span></span> | <span data-ttu-id="63140-117">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="63140-117">color-buffer</span></span>                                                                     |
| <span data-ttu-id="63140-118">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-118">Initial value:</span></span>   | <span data-ttu-id="63140-119">1</span><span class="sxs-lookup"><span data-stu-id="63140-119">1's</span></span>                                                                              |
| <span data-ttu-id="63140-120">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-120">Get command:</span></span>     | [<span data-ttu-id="63140-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="63140-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="63140-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK colore \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63140-123">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-123">Description:</span></span>     | <span data-ttu-id="63140-124">Abilitazione della scrittura di colori; R, G, B o A</span><span class="sxs-lookup"><span data-stu-id="63140-124">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="63140-125">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-125">Attribute group:</span></span> | <span data-ttu-id="63140-126">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="63140-126">color-buffer</span></span>                                                                     |
| <span data-ttu-id="63140-127">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-127">Initial value:</span></span>   | <span data-ttu-id="63140-128">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="63140-128">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="63140-129">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-129">Get command:</span></span>     | [<span data-ttu-id="63140-130">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="63140-130">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="63140-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_WRITEMASK profondità \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63140-132">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-132">Description:</span></span>     | <span data-ttu-id="63140-133">Buffer di profondità abilitato per la scrittura</span><span class="sxs-lookup"><span data-stu-id="63140-133">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="63140-134">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-134">Attribute group:</span></span> | <span data-ttu-id="63140-135">buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="63140-135">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="63140-136">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-136">Initial value:</span></span>   | <span data-ttu-id="63140-137">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="63140-137">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="63140-138">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-138">Get command:</span></span>     | [<span data-ttu-id="63140-139">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="63140-139">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="63140-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_WRITEMASK stencil \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63140-141">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-141">Description:</span></span>     | <span data-ttu-id="63140-142">Stencil-buffer writemask</span><span class="sxs-lookup"><span data-stu-id="63140-142">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="63140-143">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-143">Attribute group:</span></span> | <span data-ttu-id="63140-144">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="63140-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="63140-145">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-145">Initial value:</span></span>   | <span data-ttu-id="63140-146">1</span><span class="sxs-lookup"><span data-stu-id="63140-146">1's</span></span>                                                                              |
| <span data-ttu-id="63140-147">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-147">Get command:</span></span>     | [<span data-ttu-id="63140-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="63140-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="63140-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_valore di \_ cancellazione del colore GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="63140-150">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-150">Description:</span></span>     | <span data-ttu-id="63140-151">Valore Clear del buffer dei colori (modalità RGBA)</span><span class="sxs-lookup"><span data-stu-id="63140-151">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="63140-152">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-152">Attribute group:</span></span> | <span data-ttu-id="63140-153">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="63140-153">color-buffer</span></span>                                                                   |
| <span data-ttu-id="63140-154">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-154">Initial value:</span></span>   | <span data-ttu-id="63140-155">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="63140-155">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="63140-156">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-156">Get command:</span></span>     | [<span data-ttu-id="63140-157">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="63140-157">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="63140-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_valore di \_ cancellazione \_ indice GL</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="63140-159">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-159">Description:</span></span>     | <span data-ttu-id="63140-160">Valore Clear del buffer dei colori (modalità di indicizzazione dei colori)</span><span class="sxs-lookup"><span data-stu-id="63140-160">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="63140-161">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-161">Attribute group:</span></span> | <span data-ttu-id="63140-162">buffer a colori</span><span class="sxs-lookup"><span data-stu-id="63140-162">color-buffer</span></span>                                                                   |
| <span data-ttu-id="63140-163">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-163">Initial value:</span></span>   | <span data-ttu-id="63140-164">0</span><span class="sxs-lookup"><span data-stu-id="63140-164">0</span></span>                                                                              |
| <span data-ttu-id="63140-165">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-165">Get command:</span></span>     | [<span data-ttu-id="63140-166">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="63140-166">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="63140-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ valore Clear profondità \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63140-168">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-168">Description:</span></span>     | <span data-ttu-id="63140-169">Depth-valore Clear del buffer</span><span class="sxs-lookup"><span data-stu-id="63140-169">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="63140-170">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-170">Attribute group:</span></span> | <span data-ttu-id="63140-171">buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="63140-171">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="63140-172">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-172">Initial value:</span></span>   | <span data-ttu-id="63140-173">1</span><span class="sxs-lookup"><span data-stu-id="63140-173">1</span></span>                                                                                |
| <span data-ttu-id="63140-174">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-174">Get command:</span></span>     | [<span data-ttu-id="63140-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="63140-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="63140-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ valore chiaro stencil \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63140-177">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-177">Description:</span></span>     | <span data-ttu-id="63140-178">Stencil-valore non crittografato del buffer</span><span class="sxs-lookup"><span data-stu-id="63140-178">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="63140-179">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-179">Attribute group:</span></span> | <span data-ttu-id="63140-180">stencil-buffer</span><span class="sxs-lookup"><span data-stu-id="63140-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="63140-181">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-181">Initial value:</span></span>   | <span data-ttu-id="63140-182">0</span><span class="sxs-lookup"><span data-stu-id="63140-182">0</span></span>                                                                                |
| <span data-ttu-id="63140-183">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-183">Get command:</span></span>     | [<span data-ttu-id="63140-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="63140-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="63140-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_ \_ valore non crittografato \_ Contabilità GL</dt> </span><span class="sxs-lookup"><span data-stu-id="63140-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="63140-186">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="63140-186">Description:</span></span>     | <span data-ttu-id="63140-187">Accumulo-valore Clear buffer</span><span class="sxs-lookup"><span data-stu-id="63140-187">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="63140-188">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="63140-188">Attribute group:</span></span> | <span data-ttu-id="63140-189">accut-buffer</span><span class="sxs-lookup"><span data-stu-id="63140-189">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="63140-190">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="63140-190">Initial value:</span></span>   | <span data-ttu-id="63140-191">0</span><span class="sxs-lookup"><span data-stu-id="63140-191">0</span></span>                                                                              |
| <span data-ttu-id="63140-192">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="63140-192">Get command:</span></span>     | [<span data-ttu-id="63140-193">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="63140-193">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 





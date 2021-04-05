---
title: Variabili di stato della trasformazione
description: Variabili di stato della trasformazione
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variabili di stato della trasformazione OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3434fe9f9aa528aa8d201b56ed363753c594690f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334276"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="75138-104">Variabili di stato della trasformazione</span><span class="sxs-lookup"><span data-stu-id="75138-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="75138-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_matrice GL MODELVIEW \_</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="75138-106">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-106">Description:</span></span>     | <span data-ttu-id="75138-107">Stack matrice Modelview</span><span class="sxs-lookup"><span data-stu-id="75138-107">Modelview matrix stack</span></span>             |
| <span data-ttu-id="75138-108">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-108">Attribute group:</span></span> |                                    |
| <span data-ttu-id="75138-109">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-109">Initial value:</span></span>   | <span data-ttu-id="75138-110">Identità</span><span class="sxs-lookup"><span data-stu-id="75138-110">Identity</span></span>                           |
| <span data-ttu-id="75138-111">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-111">Get command:</span></span>     | [<span data-ttu-id="75138-112">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="75138-112">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="75138-113"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matrice di proiezione GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-113"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="75138-114">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-114">Description:</span></span>     | <span data-ttu-id="75138-115">Stack matrice di proiezione</span><span class="sxs-lookup"><span data-stu-id="75138-115">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="75138-116">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-116">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="75138-117">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-117">Initial value:</span></span>   | <span data-ttu-id="75138-118">Identità</span><span class="sxs-lookup"><span data-stu-id="75138-118">Identity</span></span>                                                                       |
| <span data-ttu-id="75138-119">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-119">Get command:</span></span>     | [<span data-ttu-id="75138-120">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="75138-120">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="75138-121"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matrice di trama GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-121"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="75138-122">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-122">Description:</span></span>     | <span data-ttu-id="75138-123">Stack matrice trama</span><span class="sxs-lookup"><span data-stu-id="75138-123">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="75138-124">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-124">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="75138-125">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-125">Initial value:</span></span>   | <span data-ttu-id="75138-126">Identità</span><span class="sxs-lookup"><span data-stu-id="75138-126">Identity</span></span>                                                                       |
| <span data-ttu-id="75138-127">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-127">Get command:</span></span>     | [<span data-ttu-id="75138-128">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="75138-128">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="75138-129"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_riquadro di visualizzazione GL</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-129"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75138-130">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-130">Description:</span></span>     | <span data-ttu-id="75138-131">Origine e extent del viewport</span><span class="sxs-lookup"><span data-stu-id="75138-131">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="75138-132">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-132">Attribute group:</span></span> | <span data-ttu-id="75138-133">riquadro di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="75138-133">viewport</span></span>                                                                         |
| <span data-ttu-id="75138-134">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-134">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="75138-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-135">Get command:</span></span>     | [<span data-ttu-id="75138-136">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="75138-136">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="75138-137"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_intervallo di profondità GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-137"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="75138-138">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-138">Description:</span></span>     | <span data-ttu-id="75138-139">Intervallo di profondità vicino e lontano</span><span class="sxs-lookup"><span data-stu-id="75138-139">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="75138-140">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-140">Attribute group:</span></span> | <span data-ttu-id="75138-141">riquadro di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="75138-141">viewport</span></span>                                                                       |
| <span data-ttu-id="75138-142">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-142">Initial value:</span></span>   | <span data-ttu-id="75138-143">0, 1</span><span class="sxs-lookup"><span data-stu-id="75138-143">0, 1</span></span>                                                                           |
| <span data-ttu-id="75138-144">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-144">Get command:</span></span>     | [<span data-ttu-id="75138-145">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="75138-145">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="75138-146"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>\_ \_ profondità dello stack MODELVIEW GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-146"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75138-147">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-147">Description:</span></span>     | <span data-ttu-id="75138-148">Puntatore dello stack della matrice Modelview</span><span class="sxs-lookup"><span data-stu-id="75138-148">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="75138-149">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-149">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="75138-150">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-150">Initial value:</span></span>   | <span data-ttu-id="75138-151">1</span><span class="sxs-lookup"><span data-stu-id="75138-151">1</span></span>                                                                                |
| <span data-ttu-id="75138-152">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-152">Get command:</span></span>     | [<span data-ttu-id="75138-153">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="75138-153">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="75138-154"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_ \_ profondità dello stack di proiezione GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-154"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75138-155">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-155">Description:</span></span>     | <span data-ttu-id="75138-156">Puntatore dello stack della matrice di proiezione</span><span class="sxs-lookup"><span data-stu-id="75138-156">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="75138-157">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-157">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="75138-158">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-158">Initial value:</span></span>   | <span data-ttu-id="75138-159">1</span><span class="sxs-lookup"><span data-stu-id="75138-159">1</span></span>                                                                                |
| <span data-ttu-id="75138-160">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-160">Get command:</span></span>     | [<span data-ttu-id="75138-161">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="75138-161">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="75138-162"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>\_ \_ profondità dello stack di trama GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-162"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75138-163">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-163">Description:</span></span>     | <span data-ttu-id="75138-164">Puntatore dello stack della matrice di trama</span><span class="sxs-lookup"><span data-stu-id="75138-164">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="75138-165">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-165">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="75138-166">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-166">Initial value:</span></span>   | <span data-ttu-id="75138-167">1</span><span class="sxs-lookup"><span data-stu-id="75138-167">1</span></span>                                                                                |
| <span data-ttu-id="75138-168">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-168">Get command:</span></span>     | [<span data-ttu-id="75138-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="75138-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="75138-170"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_modalità matrice \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-170"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75138-171">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-171">Description:</span></span>     | <span data-ttu-id="75138-172">Modalità matrice corrente</span><span class="sxs-lookup"><span data-stu-id="75138-172">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="75138-173">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-173">Attribute group:</span></span> | <span data-ttu-id="75138-174">trasformazione</span><span class="sxs-lookup"><span data-stu-id="75138-174">transform</span></span>                                                                        |
| <span data-ttu-id="75138-175">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-175">Initial value:</span></span>   | <span data-ttu-id="75138-176">\_MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="75138-176">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="75138-177">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-177">Get command:</span></span>     | [<span data-ttu-id="75138-178">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="75138-178">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="75138-179"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>\_normalizzare GL</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-179"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

|                  |                                     |
|------------------|-------------------------------------|
| <span data-ttu-id="75138-180">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-180">Description:</span></span>     | <span data-ttu-id="75138-181">Normalizzazione normale corrente</span><span class="sxs-lookup"><span data-stu-id="75138-181">Current normal normalization on/off</span></span> |
| <span data-ttu-id="75138-182">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-182">Attribute group:</span></span> | <span data-ttu-id="75138-183">trasforma/Abilita</span><span class="sxs-lookup"><span data-stu-id="75138-183">transform/enable</span></span>                    |
| <span data-ttu-id="75138-184">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-184">Initial value:</span></span>   | <span data-ttu-id="75138-185">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="75138-185">GL\_FALSE</span></span>                           |
| <span data-ttu-id="75138-186">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-186">Get command:</span></span>     | [<span data-ttu-id="75138-187">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="75138-187">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="75138-188"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Piano di ritaglio GL \_ *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-188"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="75138-189">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-189">Description:</span></span>     | <span data-ttu-id="75138-190">Coefficienti del piano di ritaglio utente</span><span class="sxs-lookup"><span data-stu-id="75138-190">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="75138-191">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-191">Attribute group:</span></span> | <span data-ttu-id="75138-192">trasformazione</span><span class="sxs-lookup"><span data-stu-id="75138-192">transform</span></span>                                |
| <span data-ttu-id="75138-193">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-193">Initial value:</span></span>   | <span data-ttu-id="75138-194">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="75138-194">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="75138-195">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-195">Get command:</span></span>     | [<span data-ttu-id="75138-196">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="75138-196">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="75138-197"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Piano di ritaglio GL \_ *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="75138-197"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="75138-198">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="75138-198">Description:</span></span>     | <span data-ttu-id="75138-199">*i* TH il piano di ritaglio utente è abilitato</span><span class="sxs-lookup"><span data-stu-id="75138-199">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="75138-200">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="75138-200">Attribute group:</span></span> | <span data-ttu-id="75138-201">trasforma/Abilita</span><span class="sxs-lookup"><span data-stu-id="75138-201">transform/enable</span></span>                   |
| <span data-ttu-id="75138-202">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="75138-202">Initial value:</span></span>   | <span data-ttu-id="75138-203">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="75138-203">GL\_FALSE</span></span>                          |
| <span data-ttu-id="75138-204">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="75138-204">Get command:</span></span>     | [<span data-ttu-id="75138-205">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="75138-205">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 





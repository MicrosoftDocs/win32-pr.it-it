---
title: Variabili di stato di illuminazione
description: Variabili di stato di illuminazione
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Variabili di stato di illuminazione OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857398"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="4de32-104">Variabili di stato di illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="4de32-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>\_illuminazione GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-106">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-106">Description:</span></span>     | <span data-ttu-id="4de32-107">True se l'illuminazione è abilitata</span><span class="sxs-lookup"><span data-stu-id="4de32-107">True if lighting is enabled</span></span>        |
| <span data-ttu-id="4de32-108">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-108">Attribute group:</span></span> | <span data-ttu-id="4de32-109">illuminazione/abilitazione</span><span class="sxs-lookup"><span data-stu-id="4de32-109">lighting/enable</span></span>                    |
| <span data-ttu-id="4de32-110">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-110">Initial value:</span></span>   | <span data-ttu-id="4de32-111">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4de32-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="4de32-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-112">Get command:</span></span>     | [<span data-ttu-id="4de32-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4de32-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="4de32-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_materiale colore \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-115">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-115">Description:</span></span>     | <span data-ttu-id="4de32-116">True se è abilitata la verifica dei colori</span><span class="sxs-lookup"><span data-stu-id="4de32-116">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="4de32-117">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-117">Attribute group:</span></span> | <span data-ttu-id="4de32-118">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-118">lighting</span></span>                           |
| <span data-ttu-id="4de32-119">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-119">Initial value:</span></span>   | <span data-ttu-id="4de32-120">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4de32-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="4de32-121">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-121">Get command:</span></span>     | [<span data-ttu-id="4de32-122">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4de32-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="4de32-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_parametro del \_ materiale \_ colore GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4de32-124">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-124">Description:</span></span>     | <span data-ttu-id="4de32-125">Proprietà materiali che verificano il colore corrente</span><span class="sxs-lookup"><span data-stu-id="4de32-125">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="4de32-126">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-126">Attribute group:</span></span> | <span data-ttu-id="4de32-127">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-127">lighting</span></span>                                                                         |
| <span data-ttu-id="4de32-128">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-128">Initial value:</span></span>   | <span data-ttu-id="4de32-129">\_ambiente GL \_ e \_ diffusa</span><span class="sxs-lookup"><span data-stu-id="4de32-129">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="4de32-130">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-130">Get command:</span></span>     | [<span data-ttu-id="4de32-131">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="4de32-131">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4de32-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_ \_ aspetto materiale colore \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4de32-133">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-133">Description:</span></span>     | <span data-ttu-id="4de32-134">Visi interessati dal rilevamento dei colori</span><span class="sxs-lookup"><span data-stu-id="4de32-134">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="4de32-135">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-135">Attribute group:</span></span> | <span data-ttu-id="4de32-136">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-136">lighting</span></span>                                                                         |
| <span data-ttu-id="4de32-137">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-137">Initial value:</span></span>   | <span data-ttu-id="4de32-138">\_primo \_ e \_ indietro GL</span><span class="sxs-lookup"><span data-stu-id="4de32-138">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="4de32-139">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-139">Get command:</span></span>     | [<span data-ttu-id="4de32-140">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="4de32-140">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4de32-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_ambiente GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4de32-142">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-142">Description:</span></span>     | <span data-ttu-id="4de32-143">Colore materiale ambiente</span><span class="sxs-lookup"><span data-stu-id="4de32-143">Ambient material color</span></span>                   |
| <span data-ttu-id="4de32-144">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-144">Attribute group:</span></span> | <span data-ttu-id="4de32-145">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-145">lighting</span></span>                                 |
| <span data-ttu-id="4de32-146">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-146">Initial value:</span></span>   | <span data-ttu-id="4de32-147">(0.2, 0.2, 0.2, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4de32-147">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="4de32-148">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-148">Get command:</span></span>     | [<span data-ttu-id="4de32-149">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-149">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4de32-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ diffuse</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4de32-151">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-151">Description:</span></span>     | <span data-ttu-id="4de32-152">Colore materiale diffuso</span><span class="sxs-lookup"><span data-stu-id="4de32-152">Diffuse material color</span></span>                   |
| <span data-ttu-id="4de32-153">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-153">Attribute group:</span></span> | <span data-ttu-id="4de32-154">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-154">lighting</span></span>                                 |
| <span data-ttu-id="4de32-155">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-155">Initial value:</span></span>   | <span data-ttu-id="4de32-156">(0.8, 0.8, 0.8, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4de32-156">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="4de32-157">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-157">Get command:</span></span>     | [<span data-ttu-id="4de32-158">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-158">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4de32-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_speculare GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4de32-160">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-160">Description:</span></span>     | <span data-ttu-id="4de32-161">Colore materiale speculare</span><span class="sxs-lookup"><span data-stu-id="4de32-161">Specular material color</span></span>                  |
| <span data-ttu-id="4de32-162">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-162">Attribute group:</span></span> | <span data-ttu-id="4de32-163">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-163">lighting</span></span>                                 |
| <span data-ttu-id="4de32-164">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-164">Initial value:</span></span>   | <span data-ttu-id="4de32-165">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4de32-165">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="4de32-166">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-166">Get command:</span></span>     | [<span data-ttu-id="4de32-167">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-167">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4de32-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_emissione GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4de32-169">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-169">Description:</span></span>     | <span data-ttu-id="4de32-170">Colore materiale emissivo</span><span class="sxs-lookup"><span data-stu-id="4de32-170">Emissive material color</span></span>                  |
| <span data-ttu-id="4de32-171">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-171">Attribute group:</span></span> | <span data-ttu-id="4de32-172">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-172">lighting</span></span>                                 |
| <span data-ttu-id="4de32-173">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-173">Initial value:</span></span>   | <span data-ttu-id="4de32-174">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4de32-174">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="4de32-175">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-175">Get command:</span></span>     | [<span data-ttu-id="4de32-176">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-176">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4de32-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>\_lucentezza GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4de32-178">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-178">Description:</span></span>     | <span data-ttu-id="4de32-179">Esponente speculare del materiale</span><span class="sxs-lookup"><span data-stu-id="4de32-179">Specular exponent of material</span></span>            |
| <span data-ttu-id="4de32-180">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-180">Attribute group:</span></span> | <span data-ttu-id="4de32-181">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-181">lighting</span></span>                                 |
| <span data-ttu-id="4de32-182">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-182">Initial value:</span></span>   | <span data-ttu-id="4de32-183">0,0</span><span class="sxs-lookup"><span data-stu-id="4de32-183">0.0</span></span>                                      |
| <span data-ttu-id="4de32-184">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-184">Get command:</span></span>     | [<span data-ttu-id="4de32-185">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-185">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="4de32-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>\_ \_ ambiente modello di luce GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="4de32-187">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-187">Description:</span></span>     | <span data-ttu-id="4de32-188">Colore della scena ambiente</span><span class="sxs-lookup"><span data-stu-id="4de32-188">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="4de32-189">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-189">Attribute group:</span></span> | <span data-ttu-id="4de32-190">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-190">lighting</span></span>                                                                       |
| <span data-ttu-id="4de32-191">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-191">Initial value:</span></span>   | <span data-ttu-id="4de32-192">(0.2, 0.2, 0.2, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4de32-192">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="4de32-193">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-193">Get command:</span></span>     | [<span data-ttu-id="4de32-194">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="4de32-194">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4de32-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ \_ Visualizzatore locale del modello GL Light \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4de32-196">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-196">Description:</span></span>     | <span data-ttu-id="4de32-197">Visualizzatore locale</span><span class="sxs-lookup"><span data-stu-id="4de32-197">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="4de32-198">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-198">Attribute group:</span></span> | <span data-ttu-id="4de32-199">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-199">lighting</span></span>                                                                         |
| <span data-ttu-id="4de32-200">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-200">Initial value:</span></span>   | <span data-ttu-id="4de32-201">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4de32-201">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="4de32-202">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-202">Get command:</span></span>     | [<span data-ttu-id="4de32-203">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="4de32-203">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4de32-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>\_modello GL Light \_ Two- \_ \_ Side</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4de32-205">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-205">Description:</span></span>     | <span data-ttu-id="4de32-206">USA illuminazione a due lati</span><span class="sxs-lookup"><span data-stu-id="4de32-206">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="4de32-207">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-207">Attribute group:</span></span> | <span data-ttu-id="4de32-208">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-208">lighting</span></span>                                                                         |
| <span data-ttu-id="4de32-209">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-209">Initial value:</span></span>   | <span data-ttu-id="4de32-210">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4de32-210">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="4de32-211">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-211">Get command:</span></span>     | [<span data-ttu-id="4de32-212">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="4de32-212">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="4de32-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_ambiente GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-214">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-214">Description:</span></span>     | <span data-ttu-id="4de32-215">Intensità di ambiente della luce *i*</span><span class="sxs-lookup"><span data-stu-id="4de32-215">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="4de32-216">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-216">Attribute group:</span></span> | <span data-ttu-id="4de32-217">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-217">lighting</span></span>                           |
| <span data-ttu-id="4de32-218">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-218">Initial value:</span></span>   | <span data-ttu-id="4de32-219">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="4de32-219">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="4de32-220">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-220">Get command:</span></span>     | [<span data-ttu-id="4de32-221">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-221">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ diffuse</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-223">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-223">Description:</span></span>     | <span data-ttu-id="4de32-224">Intensità diffusa della luce *i*</span><span class="sxs-lookup"><span data-stu-id="4de32-224">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="4de32-225">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-225">Attribute group:</span></span> | <span data-ttu-id="4de32-226">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-226">lighting</span></span>                           |
| <span data-ttu-id="4de32-227">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-227">Initial value:</span></span>   |                                    |
| <span data-ttu-id="4de32-228">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-228">Get command:</span></span>     | [<span data-ttu-id="4de32-229">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-229">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_speculare GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-231">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-231">Description:</span></span>     | <span data-ttu-id="4de32-232">Intensità speculare della luce *i*</span><span class="sxs-lookup"><span data-stu-id="4de32-232">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="4de32-233">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-233">Attribute group:</span></span> | <span data-ttu-id="4de32-234">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-234">lighting</span></span>                           |
| <span data-ttu-id="4de32-235">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-235">Initial value:</span></span>   |                                    |
| <span data-ttu-id="4de32-236">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-236">Get command:</span></span>     | [<span data-ttu-id="4de32-237">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-237">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>\_posizione GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-239">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-239">Description:</span></span>     | <span data-ttu-id="4de32-240">Posizione della luce *i*</span><span class="sxs-lookup"><span data-stu-id="4de32-240">Position of light *i*</span></span>              |
| <span data-ttu-id="4de32-241">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-241">Attribute group:</span></span> | <span data-ttu-id="4de32-242">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-242">lighting</span></span>                           |
| <span data-ttu-id="4de32-243">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-243">Initial value:</span></span>   | <span data-ttu-id="4de32-244">(0,0, 0.0, 1.0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="4de32-244">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="4de32-245">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-245">Get command:</span></span>     | [<span data-ttu-id="4de32-246">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-246">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_ \_ attenuazione costante GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-248">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-248">Description:</span></span>     | <span data-ttu-id="4de32-249">Fattore di attenuazione costante</span><span class="sxs-lookup"><span data-stu-id="4de32-249">Constant attenuation factor</span></span>        |
| <span data-ttu-id="4de32-250">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-250">Attribute group:</span></span> | <span data-ttu-id="4de32-251">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-251">lighting</span></span>                           |
| <span data-ttu-id="4de32-252">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-252">Initial value:</span></span>   | <span data-ttu-id="4de32-253">1.0</span><span class="sxs-lookup"><span data-stu-id="4de32-253">1.0</span></span>                                |
| <span data-ttu-id="4de32-254">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-254">Get command:</span></span>     | [<span data-ttu-id="4de32-255">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-255">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_ \_ attenuazione lineare GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-257">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-257">Description:</span></span>     | <span data-ttu-id="4de32-258">Fattore di attenuazione lineare</span><span class="sxs-lookup"><span data-stu-id="4de32-258">Linear attenuation factor</span></span>          |
| <span data-ttu-id="4de32-259">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-259">Attribute group:</span></span> | <span data-ttu-id="4de32-260">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-260">lighting</span></span>                           |
| <span data-ttu-id="4de32-261">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-261">Initial value:</span></span>   | <span data-ttu-id="4de32-262">0,0</span><span class="sxs-lookup"><span data-stu-id="4de32-262">0.0</span></span>                                |
| <span data-ttu-id="4de32-263">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-263">Get command:</span></span>     | [<span data-ttu-id="4de32-264">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-264">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_attenuazione quadratica GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-266">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-266">Description:</span></span>     | <span data-ttu-id="4de32-267">Fattore di attenuazione quadratica</span><span class="sxs-lookup"><span data-stu-id="4de32-267">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="4de32-268">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-268">Attribute group:</span></span> | <span data-ttu-id="4de32-269">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-269">lighting</span></span>                           |
| <span data-ttu-id="4de32-270">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-270">Initial value:</span></span>   | <span data-ttu-id="4de32-271">0,0</span><span class="sxs-lookup"><span data-stu-id="4de32-271">0.0</span></span>                                |
| <span data-ttu-id="4de32-272">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-272">Get command:</span></span>     | [<span data-ttu-id="4de32-273">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-273">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>\_direzione spot \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-275">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-275">Description:</span></span>     | <span data-ttu-id="4de32-276">Direzione Spotlight della luce *i*</span><span class="sxs-lookup"><span data-stu-id="4de32-276">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="4de32-277">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-277">Attribute group:</span></span> | <span data-ttu-id="4de32-278">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-278">lighting</span></span>                           |
| <span data-ttu-id="4de32-279">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-279">Initial value:</span></span>   | <span data-ttu-id="4de32-280">(0,0, 0,0,-1,0)</span><span class="sxs-lookup"><span data-stu-id="4de32-280">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="4de32-281">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-281">Get command:</span></span>     | [<span data-ttu-id="4de32-282">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-282">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>\_esponente spot GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-284">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-284">Description:</span></span>     | <span data-ttu-id="4de32-285">Esponente Spotlight della luce *i*</span><span class="sxs-lookup"><span data-stu-id="4de32-285">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="4de32-286">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-286">Attribute group:</span></span> | <span data-ttu-id="4de32-287">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-287">lighting</span></span>                           |
| <span data-ttu-id="4de32-288">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-288">Initial value:</span></span>   | <span data-ttu-id="4de32-289">0,0</span><span class="sxs-lookup"><span data-stu-id="4de32-289">0.0</span></span>                                |
| <span data-ttu-id="4de32-290">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-290">Get command:</span></span>     | [<span data-ttu-id="4de32-291">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-291">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>\_taglio GL spot \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-293">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-293">Description:</span></span>     | <span data-ttu-id="4de32-294">Angolo in primo piano della luce *i*</span><span class="sxs-lookup"><span data-stu-id="4de32-294">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="4de32-295">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-295">Attribute group:</span></span> | <span data-ttu-id="4de32-296">illuminazione</span><span class="sxs-lookup"><span data-stu-id="4de32-296">lighting</span></span>                           |
| <span data-ttu-id="4de32-297">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-297">Initial value:</span></span>   | <span data-ttu-id="4de32-298">180,0</span><span class="sxs-lookup"><span data-stu-id="4de32-298">180.0</span></span>                              |
| <span data-ttu-id="4de32-299">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-299">Get command:</span></span>     | [<span data-ttu-id="4de32-300">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="4de32-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="4de32-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ Light *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="4de32-302">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-302">Description:</span></span>     | <span data-ttu-id="4de32-303">True se la *luce è* abilitata</span><span class="sxs-lookup"><span data-stu-id="4de32-303">True if light *i* enabled</span></span>          |
| <span data-ttu-id="4de32-304">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-304">Attribute group:</span></span> | <span data-ttu-id="4de32-305">illuminazione/abilitazione</span><span class="sxs-lookup"><span data-stu-id="4de32-305">lighting/enable</span></span>                    |
| <span data-ttu-id="4de32-306">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-306">Initial value:</span></span>   | <span data-ttu-id="4de32-307">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="4de32-307">GL\_FALSE</span></span>                          |
| <span data-ttu-id="4de32-308">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-308">Get command:</span></span>     | [<span data-ttu-id="4de32-309">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4de32-309">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="4de32-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>indici di \_ colore GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4de32-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="4de32-311">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="4de32-311">Description:</span></span>     | <span data-ttu-id="4de32-312">*C (a)*, *c (d)* e *c (s* ) per l'illuminazione degli indici dei colori</span><span class="sxs-lookup"><span data-stu-id="4de32-312">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="4de32-313">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="4de32-313">Attribute group:</span></span> | <span data-ttu-id="4de32-314">illuminazione/abilitazione</span><span class="sxs-lookup"><span data-stu-id="4de32-314">lighting/enable</span></span>                                                                |
| <span data-ttu-id="4de32-315">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="4de32-315">Initial value:</span></span>   | <span data-ttu-id="4de32-316">0, 1, 1</span><span class="sxs-lookup"><span data-stu-id="4de32-316">0,1,1</span></span>                                                                          |
| <span data-ttu-id="4de32-317">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4de32-317">Get command:</span></span>     | [<span data-ttu-id="4de32-318">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="4de32-318">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 





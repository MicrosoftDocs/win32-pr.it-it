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
ms.openlocfilehash: 3c5a2d029727f4ff4a9eee353230e0843a39f082
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909849"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="1530e-104">Variabili di stato di illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="1530e-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>ILLUMINAZIONE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

| <span data-ttu-id="1530e-106">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-106">Property</span></span> | <span data-ttu-id="1530e-107">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-108">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-108">Description:</span></span>     | <span data-ttu-id="1530e-109">True se l'illuminazione è abilitata</span><span class="sxs-lookup"><span data-stu-id="1530e-109">True if lighting is enabled</span></span>        |
| <span data-ttu-id="1530e-110">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-110">Attribute group:</span></span> | <span data-ttu-id="1530e-111">illuminazione/abilitazione</span><span class="sxs-lookup"><span data-stu-id="1530e-111">lighting/enable</span></span>                    |
| <span data-ttu-id="1530e-112">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-112">Initial value:</span></span>   | <span data-ttu-id="1530e-113">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="1530e-113">GL\_FALSE</span></span>                          |
| <span data-ttu-id="1530e-114">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-114">Get command:</span></span>     | [<span data-ttu-id="1530e-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1530e-115">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="1530e-116"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>MATERIALE COLORE GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-116"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

| <span data-ttu-id="1530e-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-117">Property</span></span> | <span data-ttu-id="1530e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-118">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-119">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-119">Description:</span></span>     | <span data-ttu-id="1530e-120">True se il rilevamento dei colori è abilitato</span><span class="sxs-lookup"><span data-stu-id="1530e-120">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="1530e-121">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-121">Attribute group:</span></span> | <span data-ttu-id="1530e-122">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-122">lighting</span></span>                           |
| <span data-ttu-id="1530e-123">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-123">Initial value:</span></span>   | <span data-ttu-id="1530e-124">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="1530e-124">GL\_FALSE</span></span>                          |
| <span data-ttu-id="1530e-125">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-125">Get command:</span></span>     | [<span data-ttu-id="1530e-126">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1530e-126">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="1530e-127"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>PARAMETRO DEL MATERIALE COLORE GL \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-127"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

| <span data-ttu-id="1530e-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-128">Property</span></span> | <span data-ttu-id="1530e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-129">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1530e-130">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-130">Description:</span></span>     | <span data-ttu-id="1530e-131">Proprietà dei materiali che tracciano il colore corrente</span><span class="sxs-lookup"><span data-stu-id="1530e-131">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="1530e-132">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-132">Attribute group:</span></span> | <span data-ttu-id="1530e-133">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-133">lighting</span></span>                                                                         |
| <span data-ttu-id="1530e-134">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-134">Initial value:</span></span>   | <span data-ttu-id="1530e-135">GL \_ AMBIENTE \_ E \_ DIFFUSIONE</span><span class="sxs-lookup"><span data-stu-id="1530e-135">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="1530e-136">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-136">Get command:</span></span>     | [<span data-ttu-id="1530e-137">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="1530e-137">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="1530e-138"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL \_ COLOR \_ MATERIAL \_ FACE</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-138"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

| <span data-ttu-id="1530e-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-139">Property</span></span> | <span data-ttu-id="1530e-140">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-140">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1530e-141">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-141">Description:</span></span>     | <span data-ttu-id="1530e-142">Visi interessati dal rilevamento dei colori</span><span class="sxs-lookup"><span data-stu-id="1530e-142">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="1530e-143">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-143">Attribute group:</span></span> | <span data-ttu-id="1530e-144">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-144">lighting</span></span>                                                                         |
| <span data-ttu-id="1530e-145">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-145">Initial value:</span></span>   | <span data-ttu-id="1530e-146">GL \_ FRONT \_ AND \_ BACK</span><span class="sxs-lookup"><span data-stu-id="1530e-146">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="1530e-147">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-147">Get command:</span></span>     | [<span data-ttu-id="1530e-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="1530e-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="1530e-149"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>AMBIENTE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-149"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

| <span data-ttu-id="1530e-150">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-150">Property</span></span> | <span data-ttu-id="1530e-151">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-151">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="1530e-152">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-152">Description:</span></span>     | <span data-ttu-id="1530e-153">Colore materiale ambientale</span><span class="sxs-lookup"><span data-stu-id="1530e-153">Ambient material color</span></span>                   |
| <span data-ttu-id="1530e-154">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-154">Attribute group:</span></span> | <span data-ttu-id="1530e-155">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-155">lighting</span></span>                                 |
| <span data-ttu-id="1530e-156">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-156">Initial value:</span></span>   | <span data-ttu-id="1530e-157">(0.2,0.2,0.2,1.0)</span><span class="sxs-lookup"><span data-stu-id="1530e-157">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="1530e-158">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-158">Get command:</span></span>     | [<span data-ttu-id="1530e-159">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-159">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="1530e-160"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ DIFFUSE</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-160"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

| <span data-ttu-id="1530e-161">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-161">Property</span></span> | <span data-ttu-id="1530e-162">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-162">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="1530e-163">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-163">Description:</span></span>     | <span data-ttu-id="1530e-164">Colore materiale diffuso</span><span class="sxs-lookup"><span data-stu-id="1530e-164">Diffuse material color</span></span>                   |
| <span data-ttu-id="1530e-165">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-165">Attribute group:</span></span> | <span data-ttu-id="1530e-166">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-166">lighting</span></span>                                 |
| <span data-ttu-id="1530e-167">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-167">Initial value:</span></span>   | <span data-ttu-id="1530e-168">(0.8,0.8,0.8,1.0)</span><span class="sxs-lookup"><span data-stu-id="1530e-168">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="1530e-169">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-169">Get command:</span></span>     | [<span data-ttu-id="1530e-170">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-170">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="1530e-171"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ SPECULAR</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-171"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

| <span data-ttu-id="1530e-172">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-172">Property</span></span> | <span data-ttu-id="1530e-173">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-173">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="1530e-174">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-174">Description:</span></span>     | <span data-ttu-id="1530e-175">Colore del materiale speculare</span><span class="sxs-lookup"><span data-stu-id="1530e-175">Specular material color</span></span>                  |
| <span data-ttu-id="1530e-176">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-176">Attribute group:</span></span> | <span data-ttu-id="1530e-177">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-177">lighting</span></span>                                 |
| <span data-ttu-id="1530e-178">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-178">Initial value:</span></span>   | <span data-ttu-id="1530e-179">(0.0,0.0,0.0,1.0)</span><span class="sxs-lookup"><span data-stu-id="1530e-179">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="1530e-180">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-180">Get command:</span></span>     | [<span data-ttu-id="1530e-181">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-181">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="1530e-182"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>EMISSIONE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-182"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

| <span data-ttu-id="1530e-183">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-183">Property</span></span> | <span data-ttu-id="1530e-184">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-184">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="1530e-185">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-185">Description:</span></span>     | <span data-ttu-id="1530e-186">Colore materiale emissivo</span><span class="sxs-lookup"><span data-stu-id="1530e-186">Emissive material color</span></span>                  |
| <span data-ttu-id="1530e-187">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-187">Attribute group:</span></span> | <span data-ttu-id="1530e-188">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-188">lighting</span></span>                                 |
| <span data-ttu-id="1530e-189">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-189">Initial value:</span></span>   | <span data-ttu-id="1530e-190">(0.0,0.0,0.0,1.0)</span><span class="sxs-lookup"><span data-stu-id="1530e-190">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="1530e-191">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-191">Get command:</span></span>     | [<span data-ttu-id="1530e-192">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-192">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="1530e-193"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL \_ SHININESS</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-193"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

| <span data-ttu-id="1530e-194">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-194">Property</span></span> | <span data-ttu-id="1530e-195">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-195">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="1530e-196">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-196">Description:</span></span>     | <span data-ttu-id="1530e-197">Esponente speculare del materiale</span><span class="sxs-lookup"><span data-stu-id="1530e-197">Specular exponent of material</span></span>            |
| <span data-ttu-id="1530e-198">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-198">Attribute group:</span></span> | <span data-ttu-id="1530e-199">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-199">lighting</span></span>                                 |
| <span data-ttu-id="1530e-200">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-200">Initial value:</span></span>   | <span data-ttu-id="1530e-201">0,0</span><span class="sxs-lookup"><span data-stu-id="1530e-201">0.0</span></span>                                      |
| <span data-ttu-id="1530e-202">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-202">Get command:</span></span>     | [<span data-ttu-id="1530e-203">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-203">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="1530e-204"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>AMBIENTE \_ DEL \_ MODELLO \_ GL LIGHT</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-204"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

| <span data-ttu-id="1530e-205">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-205">Property</span></span> | <span data-ttu-id="1530e-206">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-206">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1530e-207">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-207">Description:</span></span>     | <span data-ttu-id="1530e-208">Colore della scena di ambiente</span><span class="sxs-lookup"><span data-stu-id="1530e-208">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="1530e-209">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-209">Attribute group:</span></span> | <span data-ttu-id="1530e-210">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-210">lighting</span></span>                                                                       |
| <span data-ttu-id="1530e-211">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-211">Initial value:</span></span>   | <span data-ttu-id="1530e-212">(0.2,0.2,0.2,1.0)</span><span class="sxs-lookup"><span data-stu-id="1530e-212">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="1530e-213">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-213">Get command:</span></span>     | [<span data-ttu-id="1530e-214">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="1530e-214">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="1530e-215"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL \_ LIGHT \_ MODEL \_ LOCAL \_ VIEWER</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-215"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

| <span data-ttu-id="1530e-216">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-216">Property</span></span> | <span data-ttu-id="1530e-217">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-217">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1530e-218">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-218">Description:</span></span>     | <span data-ttu-id="1530e-219">Il visualizzatore è locale</span><span class="sxs-lookup"><span data-stu-id="1530e-219">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="1530e-220">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-220">Attribute group:</span></span> | <span data-ttu-id="1530e-221">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-221">lighting</span></span>                                                                         |
| <span data-ttu-id="1530e-222">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-222">Initial value:</span></span>   | <span data-ttu-id="1530e-223">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="1530e-223">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="1530e-224">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-224">Get command:</span></span>     | [<span data-ttu-id="1530e-225">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="1530e-225">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="1530e-226"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-226"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

| <span data-ttu-id="1530e-227">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-227">Property</span></span> | <span data-ttu-id="1530e-228">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-228">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1530e-229">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-229">Description:</span></span>     | <span data-ttu-id="1530e-230">Usare l'illuminazione a due lati</span><span class="sxs-lookup"><span data-stu-id="1530e-230">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="1530e-231">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-231">Attribute group:</span></span> | <span data-ttu-id="1530e-232">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-232">lighting</span></span>                                                                         |
| <span data-ttu-id="1530e-233">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-233">Initial value:</span></span>   | <span data-ttu-id="1530e-234">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="1530e-234">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="1530e-235">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-235">Get command:</span></span>     | [<span data-ttu-id="1530e-236">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="1530e-236">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="1530e-237"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>AMBIENTE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-237"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

| <span data-ttu-id="1530e-238">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-238">Property</span></span> | <span data-ttu-id="1530e-239">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-239">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-240">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-240">Description:</span></span>     | <span data-ttu-id="1530e-241">Intensità ambientale della luce *i*</span><span class="sxs-lookup"><span data-stu-id="1530e-241">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="1530e-242">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-242">Attribute group:</span></span> | <span data-ttu-id="1530e-243">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-243">lighting</span></span>                           |
| <span data-ttu-id="1530e-244">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-244">Initial value:</span></span>   | <span data-ttu-id="1530e-245">(0.0,0.0,0.0,1.0)</span><span class="sxs-lookup"><span data-stu-id="1530e-245">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="1530e-246">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-246">Get command:</span></span>     | [<span data-ttu-id="1530e-247">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-247">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-248"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ DIFFUSE</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-248"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

| <span data-ttu-id="1530e-249">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-249">Property</span></span> | <span data-ttu-id="1530e-250">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-250">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-251">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-251">Description:</span></span>     | <span data-ttu-id="1530e-252">Intensità diffusa della luce *i*</span><span class="sxs-lookup"><span data-stu-id="1530e-252">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="1530e-253">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-253">Attribute group:</span></span> | <span data-ttu-id="1530e-254">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-254">lighting</span></span>                           |
| <span data-ttu-id="1530e-255">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-255">Initial value:</span></span>   |                                    |
| <span data-ttu-id="1530e-256">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-256">Get command:</span></span>     | [<span data-ttu-id="1530e-257">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-257">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-258"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>SPECULARE GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-258"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

| <span data-ttu-id="1530e-259">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-259">Property</span></span> | <span data-ttu-id="1530e-260">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-260">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-261">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-261">Description:</span></span>     | <span data-ttu-id="1530e-262">Intensità speculare della luce *i*</span><span class="sxs-lookup"><span data-stu-id="1530e-262">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="1530e-263">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-263">Attribute group:</span></span> | <span data-ttu-id="1530e-264">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-264">lighting</span></span>                           |
| <span data-ttu-id="1530e-265">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-265">Initial value:</span></span>   |                                    |
| <span data-ttu-id="1530e-266">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-266">Get command:</span></span>     | [<span data-ttu-id="1530e-267">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-267">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-268"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>POSIZIONE \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-268"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

| <span data-ttu-id="1530e-269">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-269">Property</span></span> | <span data-ttu-id="1530e-270">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-270">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-271">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-271">Description:</span></span>     | <span data-ttu-id="1530e-272">Posizione della luce *i*</span><span class="sxs-lookup"><span data-stu-id="1530e-272">Position of light *i*</span></span>              |
| <span data-ttu-id="1530e-273">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-273">Attribute group:</span></span> | <span data-ttu-id="1530e-274">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-274">lighting</span></span>                           |
| <span data-ttu-id="1530e-275">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-275">Initial value:</span></span>   | <span data-ttu-id="1530e-276">(0.0,0.0,1.0,0.0)</span><span class="sxs-lookup"><span data-stu-id="1530e-276">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="1530e-277">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-277">Get command:</span></span>     | [<span data-ttu-id="1530e-278">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-278">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-279"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>ATTENUAZIONE COSTANTE GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-279"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

| <span data-ttu-id="1530e-280">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-280">Property</span></span> | <span data-ttu-id="1530e-281">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-281">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-282">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-282">Description:</span></span>     | <span data-ttu-id="1530e-283">Fattore di attenuazione costante</span><span class="sxs-lookup"><span data-stu-id="1530e-283">Constant attenuation factor</span></span>        |
| <span data-ttu-id="1530e-284">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-284">Attribute group:</span></span> | <span data-ttu-id="1530e-285">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-285">lighting</span></span>                           |
| <span data-ttu-id="1530e-286">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-286">Initial value:</span></span>   | <span data-ttu-id="1530e-287">1,0</span><span class="sxs-lookup"><span data-stu-id="1530e-287">1.0</span></span>                                |
| <span data-ttu-id="1530e-288">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-288">Get command:</span></span>     | [<span data-ttu-id="1530e-289">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-289">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-290"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>ATTENUAZIONE \_ \_ LINEARE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-290"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

| <span data-ttu-id="1530e-291">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-291">Property</span></span> | <span data-ttu-id="1530e-292">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-292">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-293">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-293">Description:</span></span>     | <span data-ttu-id="1530e-294">Fattore di attenuazione lineare</span><span class="sxs-lookup"><span data-stu-id="1530e-294">Linear attenuation factor</span></span>          |
| <span data-ttu-id="1530e-295">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-295">Attribute group:</span></span> | <span data-ttu-id="1530e-296">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-296">lighting</span></span>                           |
| <span data-ttu-id="1530e-297">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-297">Initial value:</span></span>   | <span data-ttu-id="1530e-298">0,0</span><span class="sxs-lookup"><span data-stu-id="1530e-298">0.0</span></span>                                |
| <span data-ttu-id="1530e-299">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-299">Get command:</span></span>     | [<span data-ttu-id="1530e-300">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-301"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_ATTENUAZIONE \_ QUADRATICA GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-301"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

| <span data-ttu-id="1530e-302">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-302">Property</span></span> | <span data-ttu-id="1530e-303">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-303">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-304">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-304">Description:</span></span>     | <span data-ttu-id="1530e-305">Fattore di attenuazione quadratica</span><span class="sxs-lookup"><span data-stu-id="1530e-305">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="1530e-306">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-306">Attribute group:</span></span> | <span data-ttu-id="1530e-307">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-307">lighting</span></span>                           |
| <span data-ttu-id="1530e-308">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-308">Initial value:</span></span>   | <span data-ttu-id="1530e-309">0,0</span><span class="sxs-lookup"><span data-stu-id="1530e-309">0.0</span></span>                                |
| <span data-ttu-id="1530e-310">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-310">Get command:</span></span>     | [<span data-ttu-id="1530e-311">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-311">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-312"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>DIREZIONE \_ DEL PUNTO \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-312"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

| <span data-ttu-id="1530e-313">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-313">Property</span></span> | <span data-ttu-id="1530e-314">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-314">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-315">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-315">Description:</span></span>     | <span data-ttu-id="1530e-316">Direzione riflettore della *luce i*</span><span class="sxs-lookup"><span data-stu-id="1530e-316">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="1530e-317">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-317">Attribute group:</span></span> | <span data-ttu-id="1530e-318">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-318">lighting</span></span>                           |
| <span data-ttu-id="1530e-319">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-319">Initial value:</span></span>   | <span data-ttu-id="1530e-320">(0.0,0.0,-1.0)</span><span class="sxs-lookup"><span data-stu-id="1530e-320">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="1530e-321">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-321">Get command:</span></span>     | [<span data-ttu-id="1530e-322">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-322">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-323"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>ESPONENTE DI GL \_ SPOT \_</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-323"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

| <span data-ttu-id="1530e-324">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-324">Property</span></span> | <span data-ttu-id="1530e-325">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-325">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-326">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-326">Description:</span></span>     | <span data-ttu-id="1530e-327">Esponente in evidenza della luce *i*</span><span class="sxs-lookup"><span data-stu-id="1530e-327">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="1530e-328">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-328">Attribute group:</span></span> | <span data-ttu-id="1530e-329">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-329">lighting</span></span>                           |
| <span data-ttu-id="1530e-330">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-330">Initial value:</span></span>   | <span data-ttu-id="1530e-331">0,0</span><span class="sxs-lookup"><span data-stu-id="1530e-331">0.0</span></span>                                |
| <span data-ttu-id="1530e-332">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-332">Get command:</span></span>     | [<span data-ttu-id="1530e-333">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-333">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-334"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL \_ SPOT \_ CUTOFF</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-334"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

| <span data-ttu-id="1530e-335">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-335">Property</span></span> | <span data-ttu-id="1530e-336">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-336">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-337">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-337">Description:</span></span>     | <span data-ttu-id="1530e-338">Angolo in evidenza della luce *i*</span><span class="sxs-lookup"><span data-stu-id="1530e-338">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="1530e-339">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-339">Attribute group:</span></span> | <span data-ttu-id="1530e-340">illuminazione</span><span class="sxs-lookup"><span data-stu-id="1530e-340">lighting</span></span>                           |
| <span data-ttu-id="1530e-341">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-341">Initial value:</span></span>   | <span data-ttu-id="1530e-342">180.0</span><span class="sxs-lookup"><span data-stu-id="1530e-342">180.0</span></span>                              |
| <span data-ttu-id="1530e-343">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-343">Get command:</span></span>     | [<span data-ttu-id="1530e-344">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="1530e-344">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="1530e-345"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ LIGHT *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-345"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

| <span data-ttu-id="1530e-346">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-346">Property</span></span> | <span data-ttu-id="1530e-347">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-347">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="1530e-348">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-348">Description:</span></span>     | <span data-ttu-id="1530e-349">True se la luce *è abilitata*</span><span class="sxs-lookup"><span data-stu-id="1530e-349">True if light *i* enabled</span></span>          |
| <span data-ttu-id="1530e-350">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-350">Attribute group:</span></span> | <span data-ttu-id="1530e-351">illuminazione/abilitazione</span><span class="sxs-lookup"><span data-stu-id="1530e-351">lighting/enable</span></span>                    |
| <span data-ttu-id="1530e-352">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-352">Initial value:</span></span>   | <span data-ttu-id="1530e-353">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="1530e-353">GL\_FALSE</span></span>                          |
| <span data-ttu-id="1530e-354">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-354">Get command:</span></span>     | [<span data-ttu-id="1530e-355">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1530e-355">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="1530e-356"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>INDICI \_ DEI \_ COLORI GL</dt> </span><span class="sxs-lookup"><span data-stu-id="1530e-356"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

| <span data-ttu-id="1530e-357">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1530e-357">Property</span></span> | <span data-ttu-id="1530e-358">Valore</span><span class="sxs-lookup"><span data-stu-id="1530e-358">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1530e-359">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="1530e-359">Description:</span></span>     | <span data-ttu-id="1530e-360">*C (a)*, *C (d)* e *C (s)* per l'illuminazione dell'indice colori</span><span class="sxs-lookup"><span data-stu-id="1530e-360">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="1530e-361">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="1530e-361">Attribute group:</span></span> | <span data-ttu-id="1530e-362">illuminazione/abilitazione</span><span class="sxs-lookup"><span data-stu-id="1530e-362">lighting/enable</span></span>                                                                |
| <span data-ttu-id="1530e-363">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="1530e-363">Initial value:</span></span>   | <span data-ttu-id="1530e-364">0,1,1</span><span class="sxs-lookup"><span data-stu-id="1530e-364">0,1,1</span></span>                                                                          |
| <span data-ttu-id="1530e-365">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="1530e-365">Get command:</span></span>     | [<span data-ttu-id="1530e-366">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="1530e-366">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 





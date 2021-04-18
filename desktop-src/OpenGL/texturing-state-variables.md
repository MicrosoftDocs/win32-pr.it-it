---
title: Variabili di stato di texturing
description: Variabili di stato di texturing
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variabili di stato di texturing OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299103"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="00d61-104">Variabili di stato di texturing</span><span class="sxs-lookup"><span data-stu-id="00d61-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="00d61-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Trama GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="00d61-106">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-106">Description:</span></span>     | <span data-ttu-id="00d61-107">True se il   texturing x-d è abilitato (*x* è 1-d o 2-d)</span><span class="sxs-lookup"><span data-stu-id="00d61-107">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="00d61-108">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-108">Attribute group:</span></span> | <span data-ttu-id="00d61-109">trama/Abilita</span><span class="sxs-lookup"><span data-stu-id="00d61-109">texture/enable</span></span>                                        |
| <span data-ttu-id="00d61-110">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-110">Initial value:</span></span>   | <span data-ttu-id="00d61-111">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="00d61-111">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="00d61-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-112">Get command:</span></span>     | [<span data-ttu-id="00d61-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="00d61-113">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="00d61-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_trama GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| <span data-ttu-id="00d61-115">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-115">Description:</span></span>     | <span data-ttu-id="00d61-116">*x*   -D immagine trama al livello di dettaglio *i*</span><span class="sxs-lookup"><span data-stu-id="00d61-116">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="00d61-117">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-117">Attribute group:</span></span> |                                              |
| <span data-ttu-id="00d61-118">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-118">Initial value:</span></span>   |                                              |
| <span data-ttu-id="00d61-119">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-119">Get command:</span></span>     | [<span data-ttu-id="00d61-120">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="00d61-120">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="00d61-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_spessore trama \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="00d61-122">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-122">Description:</span></span>     | <span data-ttu-id="00d61-123">*x*   -D immagine trama *i*   ' altezza</span><span class="sxs-lookup"><span data-stu-id="00d61-123">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="00d61-124">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-124">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="00d61-125">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-125">Initial value:</span></span>   | <span data-ttu-id="00d61-126">0</span><span class="sxs-lookup"><span data-stu-id="00d61-126">0</span></span>                                                        |
| <span data-ttu-id="00d61-127">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-127">Get command:</span></span>     | [<span data-ttu-id="00d61-128">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="00d61-128">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="00d61-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_altezza trama \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="00d61-130">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-130">Description:</span></span>     | <span data-ttu-id="00d61-131">*x*   -D immagine trama *i*   ' altezza</span><span class="sxs-lookup"><span data-stu-id="00d61-131">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="00d61-132">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-132">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="00d61-133">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-133">Initial value:</span></span>   | <span data-ttu-id="00d61-134">0</span><span class="sxs-lookup"><span data-stu-id="00d61-134">0</span></span>                                                        |
| <span data-ttu-id="00d61-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-135">Get command:</span></span>     | [<span data-ttu-id="00d61-136">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="00d61-136">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="00d61-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_bordo trama \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="00d61-138">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-138">Description:</span></span>     | <span data-ttu-id="00d61-139">*x*   -D bordo immagine di trama *i*  </span><span class="sxs-lookup"><span data-stu-id="00d61-139">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="00d61-140">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="00d61-141">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-141">Initial value:</span></span>   | <span data-ttu-id="00d61-142">0</span><span class="sxs-lookup"><span data-stu-id="00d61-142">0</span></span>                                                        |
| <span data-ttu-id="00d61-143">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-143">Get command:</span></span>     | [<span data-ttu-id="00d61-144">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="00d61-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="00d61-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_componenti di trama GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="00d61-146">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-146">Description:</span></span>     | <span data-ttu-id="00d61-147">Componenti immagine trama</span><span class="sxs-lookup"><span data-stu-id="00d61-147">Texture image components</span></span>                                 |
| <span data-ttu-id="00d61-148">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-148">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="00d61-149">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-149">Initial value:</span></span>   | <span data-ttu-id="00d61-150">1</span><span class="sxs-lookup"><span data-stu-id="00d61-150">1</span></span>                                                        |
| <span data-ttu-id="00d61-151">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-151">Get command:</span></span>     | [<span data-ttu-id="00d61-152">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="00d61-152">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="00d61-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_ \_ colore bordo trama \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="00d61-154">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-154">Description:</span></span>     | <span data-ttu-id="00d61-155">Colore bordo trama</span><span class="sxs-lookup"><span data-stu-id="00d61-155">Texture border color</span></span>                           |
| <span data-ttu-id="00d61-156">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-156">Attribute group:</span></span> | <span data-ttu-id="00d61-157">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-157">texture</span></span>                                        |
| <span data-ttu-id="00d61-158">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-158">Initial value:</span></span>   | <span data-ttu-id="00d61-159">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="00d61-159">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="00d61-160">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-160">Get command:</span></span>     | [<span data-ttu-id="00d61-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="00d61-161">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="00d61-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_ \_ Filtro minimo trama \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="00d61-163">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-163">Description:</span></span>     | <span data-ttu-id="00d61-164">Texture minification (funzione)</span><span class="sxs-lookup"><span data-stu-id="00d61-164">Texture minification function</span></span>                  |
| <span data-ttu-id="00d61-165">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-165">Attribute group:</span></span> | <span data-ttu-id="00d61-166">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-166">texture</span></span>                                        |
| <span data-ttu-id="00d61-167">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-167">Initial value:</span></span>   | <span data-ttu-id="00d61-168">GL \_ più vicino \_ MIPMAP \_ lineare</span><span class="sxs-lookup"><span data-stu-id="00d61-168">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="00d61-169">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-169">Get command:</span></span>     | [<span data-ttu-id="00d61-170">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="00d61-170">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="00d61-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_ \_ filtro mag trama di contabilità \_</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="00d61-172">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-172">Description:</span></span>     | <span data-ttu-id="00d61-173">Funzione di ingrandimento trama</span><span class="sxs-lookup"><span data-stu-id="00d61-173">Texture magnification function</span></span>                 |
| <span data-ttu-id="00d61-174">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-174">Attribute group:</span></span> | <span data-ttu-id="00d61-175">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-175">texture</span></span>                                        |
| <span data-ttu-id="00d61-176">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-176">Initial value:</span></span>   | <span data-ttu-id="00d61-177">\_linea GL</span><span class="sxs-lookup"><span data-stu-id="00d61-177">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="00d61-178">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-178">Get command:</span></span>     | [<span data-ttu-id="00d61-179">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="00d61-179">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="00d61-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>Trama GL a \_ \_ capo \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="00d61-181">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-181">Description:</span></span>     | <span data-ttu-id="00d61-182">Modalità a capo trama (*x*   è S o T)</span><span class="sxs-lookup"><span data-stu-id="00d61-182">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="00d61-183">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-183">Attribute group:</span></span> | <span data-ttu-id="00d61-184">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-184">texture</span></span>                                        |
| <span data-ttu-id="00d61-185">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-185">Initial value:</span></span>   | <span data-ttu-id="00d61-186">\_ripetizione GL</span><span class="sxs-lookup"><span data-stu-id="00d61-186">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="00d61-187">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-187">Get command:</span></span>     | [<span data-ttu-id="00d61-188">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="00d61-188">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="00d61-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>\_ \_ modalità ENV trama \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="00d61-190">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-190">Description:</span></span>     | <span data-ttu-id="00d61-191">Funzione texture Application</span><span class="sxs-lookup"><span data-stu-id="00d61-191">Texture application function</span></span>         |
| <span data-ttu-id="00d61-192">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-192">Attribute group:</span></span> | <span data-ttu-id="00d61-193">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-193">texture</span></span>                              |
| <span data-ttu-id="00d61-194">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-194">Initial value:</span></span>   | <span data-ttu-id="00d61-195">\_modulazione GL</span><span class="sxs-lookup"><span data-stu-id="00d61-195">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="00d61-196">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-196">Get command:</span></span>     | [<span data-ttu-id="00d61-197">**glGetTexEnviv**</span><span class="sxs-lookup"><span data-stu-id="00d61-197">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="00d61-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>\_ \_ colore ENV trama \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="00d61-199">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-199">Description:</span></span>     | <span data-ttu-id="00d61-200">Colore ambiente trama</span><span class="sxs-lookup"><span data-stu-id="00d61-200">Texture environment color</span></span>            |
| <span data-ttu-id="00d61-201">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-201">Attribute group:</span></span> | <span data-ttu-id="00d61-202">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-202">texture</span></span>                              |
| <span data-ttu-id="00d61-203">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-203">Initial value:</span></span>   | <span data-ttu-id="00d61-204">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="00d61-204">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="00d61-205">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-205">Get command:</span></span>     | [<span data-ttu-id="00d61-206">**glGetTexEnvfv**</span><span class="sxs-lookup"><span data-stu-id="00d61-206">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="00d61-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>\_Gen trama \_ GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="00d61-208">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-208">Description:</span></span>     | <span data-ttu-id="00d61-209">Texgen è abilitato (*x*   è S, T, R o Q)</span><span class="sxs-lookup"><span data-stu-id="00d61-209">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="00d61-210">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-210">Attribute group:</span></span> | <span data-ttu-id="00d61-211">trama/Abilita</span><span class="sxs-lookup"><span data-stu-id="00d61-211">texture/enable</span></span>                           |
| <span data-ttu-id="00d61-212">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-212">Initial value:</span></span>   | <span data-ttu-id="00d61-213">GL \_ false</span><span class="sxs-lookup"><span data-stu-id="00d61-213">GL\_FALSE</span></span>                                |
| <span data-ttu-id="00d61-214">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-214">Get command:</span></span>     | [<span data-ttu-id="00d61-215">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="00d61-215">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="00d61-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_piano d'occhio GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="00d61-217">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-217">Description:</span></span>     | <span data-ttu-id="00d61-218">Coefficienti di equazione del piano Texgen</span><span class="sxs-lookup"><span data-stu-id="00d61-218">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="00d61-219">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-219">Attribute group:</span></span> | <span data-ttu-id="00d61-220">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-220">texture</span></span>                              |
| <span data-ttu-id="00d61-221">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-221">Initial value:</span></span>   |                                      |
| <span data-ttu-id="00d61-222">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-222">Get command:</span></span>     | [<span data-ttu-id="00d61-223">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="00d61-223">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="00d61-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_piano oggetto \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="00d61-225">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-225">Description:</span></span>     | <span data-ttu-id="00d61-226">Coefficienti lineari oggetto Texgen</span><span class="sxs-lookup"><span data-stu-id="00d61-226">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="00d61-227">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-227">Attribute group:</span></span> | <span data-ttu-id="00d61-228">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-228">texture</span></span>                              |
| <span data-ttu-id="00d61-229">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-229">Initial value:</span></span>   |                                      |
| <span data-ttu-id="00d61-230">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-230">Get command:</span></span>     | [<span data-ttu-id="00d61-231">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="00d61-231">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="00d61-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>\_modalità di \_ generazione \_ trama GL</dt> </span><span class="sxs-lookup"><span data-stu-id="00d61-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="00d61-233">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="00d61-233">Description:</span></span>     | <span data-ttu-id="00d61-234">Funzione utilizzata per texgen</span><span class="sxs-lookup"><span data-stu-id="00d61-234">Function used for texgen</span></span>             |
| <span data-ttu-id="00d61-235">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="00d61-235">Attribute group:</span></span> | <span data-ttu-id="00d61-236">trama</span><span class="sxs-lookup"><span data-stu-id="00d61-236">texture</span></span>                              |
| <span data-ttu-id="00d61-237">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="00d61-237">Initial value:</span></span>   | <span data-ttu-id="00d61-238">GL \_ occhio \_ lineare</span><span class="sxs-lookup"><span data-stu-id="00d61-238">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="00d61-239">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="00d61-239">Get command:</span></span>     | [<span data-ttu-id="00d61-240">**glGetTexGeniv**</span><span class="sxs-lookup"><span data-stu-id="00d61-240">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 





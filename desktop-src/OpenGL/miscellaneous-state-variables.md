---
title: Variabili di stato varie
description: Variabili di stato varie
ms.assetid: 4c99b9b6-5cd3-49d1-9bfe-fa1421d892f2
keywords:
- Variabili di stato varie OpenGL
topic_type:
- apiref
api_name:
- Miscellaneous State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de565d9e6f8055f1b2ebc90c4deec83da463e7d5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909858"
---
# <a name="miscellaneous-state-variables"></a><span data-ttu-id="8835b-104">Variabili di stato varie</span><span class="sxs-lookup"><span data-stu-id="8835b-104">Miscellaneous State Variables</span></span>

<dl> <span data-ttu-id="8835b-105"><dt><span id="GL_LIST_BASE"></span><span id="gl_list_base"></span>GL \_ LIST \_ BASE</dt> </span><span class="sxs-lookup"><span data-stu-id="8835b-105"><dt><span id="GL_LIST_BASE"></span><span id="gl_list_base"></span>GL\_LIST\_BASE</dt> </span></span><dd> 

| <span data-ttu-id="8835b-106">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8835b-106">Property</span></span> | <span data-ttu-id="8835b-107">Valore</span><span class="sxs-lookup"><span data-stu-id="8835b-107">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="8835b-108">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="8835b-108">Description:</span></span>     | <span data-ttu-id="8835b-109">Impostazione di **glListBase**</span><span class="sxs-lookup"><span data-stu-id="8835b-109">Setting of **glListBase**</span></span>              |
| <span data-ttu-id="8835b-110">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="8835b-110">Attribute group:</span></span> | <span data-ttu-id="8835b-111">list</span><span class="sxs-lookup"><span data-stu-id="8835b-111">list</span></span>                                   |
| <span data-ttu-id="8835b-112">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="8835b-112">Initial value:</span></span>   | <span data-ttu-id="8835b-113">0</span><span class="sxs-lookup"><span data-stu-id="8835b-113">0</span></span>                                      |
| <span data-ttu-id="8835b-114">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="8835b-114">Get command:</span></span>     | [<span data-ttu-id="8835b-115">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8835b-115">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="8835b-116"></dd> <dt><span id="GL_LIST_INDEX"></span><span id="gl_list_index"></span>GL \_ LIST \_ INDEX</dt> </span><span class="sxs-lookup"><span data-stu-id="8835b-116"></dd> <dt><span id="GL_LIST_INDEX"></span><span id="gl_list_index"></span>GL\_LIST\_INDEX</dt> </span></span><dd> 

| <span data-ttu-id="8835b-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8835b-117">Property</span></span> | <span data-ttu-id="8835b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8835b-118">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8835b-119">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="8835b-119">Description:</span></span>     | <span data-ttu-id="8835b-120">Numero di elenchi di visualizzazione in costruzione; 0 se nessuno</span><span class="sxs-lookup"><span data-stu-id="8835b-120">Number of display lists under construction; 0 if none</span></span>                            |
| <span data-ttu-id="8835b-121">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="8835b-121">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="8835b-122">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="8835b-122">Initial value:</span></span>   | <span data-ttu-id="8835b-123">0</span><span class="sxs-lookup"><span data-stu-id="8835b-123">0</span></span>                                                                                |
| <span data-ttu-id="8835b-124">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="8835b-124">Get command:</span></span>     | [<span data-ttu-id="8835b-125">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8835b-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8835b-126"></dd> <dt><span id="GL_LIST_MODE"></span><span id="gl_list_mode"></span>MODALITÀ ELENCO GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="8835b-126"></dd> <dt><span id="GL_LIST_MODE"></span><span id="gl_list_mode"></span>GL\_LIST\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="8835b-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8835b-127">Property</span></span> | <span data-ttu-id="8835b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8835b-128">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8835b-129">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="8835b-129">Description:</span></span>     | <span data-ttu-id="8835b-130">Modalità di visualizzazione dell'elenco in costruzione; undefined if none</span><span class="sxs-lookup"><span data-stu-id="8835b-130">Mode of display list under construction; undefined if none</span></span>                       |
| <span data-ttu-id="8835b-131">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="8835b-131">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="8835b-132">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="8835b-132">Initial value:</span></span>   | <span data-ttu-id="8835b-133">0</span><span class="sxs-lookup"><span data-stu-id="8835b-133">0</span></span>                                                                                |
| <span data-ttu-id="8835b-134">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="8835b-134">Get command:</span></span>     | [<span data-ttu-id="8835b-135">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8835b-135">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8835b-136"></dd> <dt><span id="GL_ATTRIB_STACK_DEPTH"></span><span id="gl_attrib_stack_depth"></span>GL \_ ATTRIB \_ STACK \_ DEPTH</dt> </span><span class="sxs-lookup"><span data-stu-id="8835b-136"></dd> <dt><span id="GL_ATTRIB_STACK_DEPTH"></span><span id="gl_attrib_stack_depth"></span>GL\_ATTRIB\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="8835b-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8835b-137">Property</span></span> | <span data-ttu-id="8835b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8835b-138">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8835b-139">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="8835b-139">Description:</span></span>     | <span data-ttu-id="8835b-140">Puntatore dello stack di attributi</span><span class="sxs-lookup"><span data-stu-id="8835b-140">Attribute stack pointer</span></span>                                                          |
| <span data-ttu-id="8835b-141">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="8835b-141">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="8835b-142">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="8835b-142">Initial value:</span></span>   | <span data-ttu-id="8835b-143">0</span><span class="sxs-lookup"><span data-stu-id="8835b-143">0</span></span>                                                                                |
| <span data-ttu-id="8835b-144">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="8835b-144">Get command:</span></span>     | [<span data-ttu-id="8835b-145">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8835b-145">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8835b-146"></dd> <dt><span id="GL_NAME_STACK_DEPTH"></span><span id="gl_name_stack_depth"></span>PROFONDITÀ DELLO STACK DEI NOMI DI CONTABILITÀ \_ \_ \_ GENERALE</dt> </span><span class="sxs-lookup"><span data-stu-id="8835b-146"></dd> <dt><span id="GL_NAME_STACK_DEPTH"></span><span id="gl_name_stack_depth"></span>GL\_NAME\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="8835b-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8835b-147">Property</span></span> | <span data-ttu-id="8835b-148">Valore</span><span class="sxs-lookup"><span data-stu-id="8835b-148">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8835b-149">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="8835b-149">Description:</span></span>     | <span data-ttu-id="8835b-150">Profondità dello stack dei nomi</span><span class="sxs-lookup"><span data-stu-id="8835b-150">Name stack depth</span></span>                                                                 |
| <span data-ttu-id="8835b-151">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="8835b-151">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="8835b-152">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="8835b-152">Initial value:</span></span>   | <span data-ttu-id="8835b-153">0</span><span class="sxs-lookup"><span data-stu-id="8835b-153">0</span></span>                                                                                |
| <span data-ttu-id="8835b-154">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="8835b-154">Get command:</span></span>     | [<span data-ttu-id="8835b-155">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8835b-155">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8835b-156"></dd> <dt><span id="GL_RENDER_MODE"></span><span id="gl_render_mode"></span>MODALITÀ \_ DI RENDERING \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="8835b-156"></dd> <dt><span id="GL_RENDER_MODE"></span><span id="gl_render_mode"></span>GL\_RENDER\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="8835b-157">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8835b-157">Property</span></span> | <span data-ttu-id="8835b-158">Valore</span><span class="sxs-lookup"><span data-stu-id="8835b-158">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8835b-159">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="8835b-159">Description:</span></span>     | <span data-ttu-id="8835b-160">**Impostazione glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="8835b-160">**glRenderMode** setting</span></span>                                                         |
| <span data-ttu-id="8835b-161">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="8835b-161">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="8835b-162">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="8835b-162">Initial value:</span></span>   | <span data-ttu-id="8835b-163">RENDERING \_ GL</span><span class="sxs-lookup"><span data-stu-id="8835b-163">GL\_RENDER</span></span>                                                                       |
| <span data-ttu-id="8835b-164">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="8835b-164">Get command:</span></span>     | [<span data-ttu-id="8835b-165">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8835b-165">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 



| <span data-ttu-id="8835b-166">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8835b-166">Property</span></span> | <span data-ttu-id="8835b-167">Valore</span><span class="sxs-lookup"><span data-stu-id="8835b-167">Value</span></span> |
|------------------|----------------------------------|
| <span data-ttu-id="8835b-168">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="8835b-168">Description:</span></span>     | <span data-ttu-id="8835b-169">Codici di errore correnti</span><span class="sxs-lookup"><span data-stu-id="8835b-169">Current error codes</span></span>              |
| <span data-ttu-id="8835b-170">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="8835b-170">Attribute group:</span></span> |                                  |
| <span data-ttu-id="8835b-171">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="8835b-171">Initial value:</span></span>   | <span data-ttu-id="8835b-172">0</span><span class="sxs-lookup"><span data-stu-id="8835b-172">0</span></span>                                |
| <span data-ttu-id="8835b-173">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="8835b-173">Get command:</span></span>     | [<span data-ttu-id="8835b-174">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="8835b-174">**glGetError**</span></span>](glgeterror.md) |



 

</dd> </dl>

 

 





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
ms.openlocfilehash: 73da6292187fcbc9cd17f94fe88f63160d89be5b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103717893"
---
# <a name="miscellaneous-state-variables"></a><span data-ttu-id="0d0f1-104">Variabili di stato varie</span><span class="sxs-lookup"><span data-stu-id="0d0f1-104">Miscellaneous State Variables</span></span>

<dl> <span data-ttu-id="0d0f1-105"><dt><span id="GL_LIST_BASE"></span><span id="gl_list_base"></span>\_base elenco \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="0d0f1-105"><dt><span id="GL_LIST_BASE"></span><span id="gl_list_base"></span>GL\_LIST\_BASE</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="0d0f1-106">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-106">Description:</span></span>     | <span data-ttu-id="0d0f1-107">Impostazione di **glListBase**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-107">Setting of **glListBase**</span></span>              |
| <span data-ttu-id="0d0f1-108">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-108">Attribute group:</span></span> | <span data-ttu-id="0d0f1-109">list</span><span class="sxs-lookup"><span data-stu-id="0d0f1-109">list</span></span>                                   |
| <span data-ttu-id="0d0f1-110">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-110">Initial value:</span></span>   | <span data-ttu-id="0d0f1-111">0</span><span class="sxs-lookup"><span data-stu-id="0d0f1-111">0</span></span>                                      |
| <span data-ttu-id="0d0f1-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-112">Get command:</span></span>     | [<span data-ttu-id="0d0f1-113">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-113">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="0d0f1-114"></dd> <dt><span id="GL_LIST_INDEX"></span><span id="gl_list_index"></span>\_Indice elenco \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="0d0f1-114"></dd> <dt><span id="GL_LIST_INDEX"></span><span id="gl_list_index"></span>GL\_LIST\_INDEX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0d0f1-115">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-115">Description:</span></span>     | <span data-ttu-id="0d0f1-116">Numero di elenchi di visualizzazione in costruzione; 0 se None</span><span class="sxs-lookup"><span data-stu-id="0d0f1-116">Number of display lists under construction; 0 if none</span></span>                            |
| <span data-ttu-id="0d0f1-117">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-117">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0d0f1-118">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-118">Initial value:</span></span>   | <span data-ttu-id="0d0f1-119">0</span><span class="sxs-lookup"><span data-stu-id="0d0f1-119">0</span></span>                                                                                |
| <span data-ttu-id="0d0f1-120">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-120">Get command:</span></span>     | [<span data-ttu-id="0d0f1-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0d0f1-122"></dd> <dt><span id="GL_LIST_MODE"></span><span id="gl_list_mode"></span>\_modalità elenco \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="0d0f1-122"></dd> <dt><span id="GL_LIST_MODE"></span><span id="gl_list_mode"></span>GL\_LIST\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0d0f1-123">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-123">Description:</span></span>     | <span data-ttu-id="0d0f1-124">Modalità di visualizzazione dell'elenco in costruzione; non definito se None</span><span class="sxs-lookup"><span data-stu-id="0d0f1-124">Mode of display list under construction; undefined if none</span></span>                       |
| <span data-ttu-id="0d0f1-125">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-125">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0d0f1-126">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-126">Initial value:</span></span>   | <span data-ttu-id="0d0f1-127">0</span><span class="sxs-lookup"><span data-stu-id="0d0f1-127">0</span></span>                                                                                |
| <span data-ttu-id="0d0f1-128">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-128">Get command:</span></span>     | [<span data-ttu-id="0d0f1-129">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-129">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0d0f1-130"></dd> <dt><span id="GL_ATTRIB_STACK_DEPTH"></span><span id="gl_attrib_stack_depth"></span>\_ \_ profondità dello stack dell'attrib GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0d0f1-130"></dd> <dt><span id="GL_ATTRIB_STACK_DEPTH"></span><span id="gl_attrib_stack_depth"></span>GL\_ATTRIB\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0d0f1-131">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-131">Description:</span></span>     | <span data-ttu-id="0d0f1-132">Puntatore stack attributo</span><span class="sxs-lookup"><span data-stu-id="0d0f1-132">Attribute stack pointer</span></span>                                                          |
| <span data-ttu-id="0d0f1-133">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-133">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0d0f1-134">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-134">Initial value:</span></span>   | <span data-ttu-id="0d0f1-135">0</span><span class="sxs-lookup"><span data-stu-id="0d0f1-135">0</span></span>                                                                                |
| <span data-ttu-id="0d0f1-136">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-136">Get command:</span></span>     | [<span data-ttu-id="0d0f1-137">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-137">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0d0f1-138"></dd> <dt><span id="GL_NAME_STACK_DEPTH"></span><span id="gl_name_stack_depth"></span>\_ \_ profondità stack nome \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="0d0f1-138"></dd> <dt><span id="GL_NAME_STACK_DEPTH"></span><span id="gl_name_stack_depth"></span>GL\_NAME\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0d0f1-139">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-139">Description:</span></span>     | <span data-ttu-id="0d0f1-140">Profondità dello stack di nomi</span><span class="sxs-lookup"><span data-stu-id="0d0f1-140">Name stack depth</span></span>                                                                 |
| <span data-ttu-id="0d0f1-141">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-141">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0d0f1-142">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-142">Initial value:</span></span>   | <span data-ttu-id="0d0f1-143">0</span><span class="sxs-lookup"><span data-stu-id="0d0f1-143">0</span></span>                                                                                |
| <span data-ttu-id="0d0f1-144">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-144">Get command:</span></span>     | [<span data-ttu-id="0d0f1-145">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-145">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0d0f1-146"></dd> <dt><span id="GL_RENDER_MODE"></span><span id="gl_render_mode"></span>\_modalità di rendering GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0d0f1-146"></dd> <dt><span id="GL_RENDER_MODE"></span><span id="gl_render_mode"></span>GL\_RENDER\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0d0f1-147">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-147">Description:</span></span>     | <span data-ttu-id="0d0f1-148">impostazione **glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-148">**glRenderMode** setting</span></span>                                                         |
| <span data-ttu-id="0d0f1-149">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-149">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0d0f1-150">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-150">Initial value:</span></span>   | <span data-ttu-id="0d0f1-151">\_rendering GL</span><span class="sxs-lookup"><span data-stu-id="0d0f1-151">GL\_RENDER</span></span>                                                                       |
| <span data-ttu-id="0d0f1-152">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-152">Get command:</span></span>     | [<span data-ttu-id="0d0f1-153">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-153">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 



|                  |                                  |
|------------------|----------------------------------|
| <span data-ttu-id="0d0f1-154">Descrizione:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-154">Description:</span></span>     | <span data-ttu-id="0d0f1-155">Codici di errore correnti</span><span class="sxs-lookup"><span data-stu-id="0d0f1-155">Current error codes</span></span>              |
| <span data-ttu-id="0d0f1-156">Gruppo di attributi:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-156">Attribute group:</span></span> |                                  |
| <span data-ttu-id="0d0f1-157">Valore iniziale:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-157">Initial value:</span></span>   | <span data-ttu-id="0d0f1-158">0</span><span class="sxs-lookup"><span data-stu-id="0d0f1-158">0</span></span>                                |
| <span data-ttu-id="0d0f1-159">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="0d0f1-159">Get command:</span></span>     | [<span data-ttu-id="0d0f1-160">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="0d0f1-160">**glGetError**</span></span>](glgeterror.md) |



 

</dd> </dl>

 

 





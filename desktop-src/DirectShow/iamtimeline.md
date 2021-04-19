---
description: L'interfaccia IAMTimeline fornisce metodi per la modifica della sequenza temporale, l'oggetto centrale in Microsoft DirectShow editing Services (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Interfaccia IAMTimeline (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332049"
---
# <a name="iamtimeline-interface"></a><span data-ttu-id="4c9a3-103">Interfaccia IAMTimeline</span><span class="sxs-lookup"><span data-stu-id="4c9a3-103">IAMTimeline interface</span></span>

> [!Note]  
> <span data-ttu-id="4c9a3-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-104">\[Deprecated.</span></span> <span data-ttu-id="4c9a3-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c9a3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c9a3-106">L' `IAMTimeline` interfaccia fornisce i metodi per modificare la sequenza temporale, ovvero l'oggetto centrale in Microsoft [DirectShow editing Services](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="4c9a3-106">The `IAMTimeline` interface provides methods for manipulating the timeline, the central object in Microsoft [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="4c9a3-107">Una sequenza temporale è una raccolta di elementi ordinati in tempo, ad esempio clip video, clip audio, effetti e transizioni tra clip.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-107">A timeline is a collection of time-ordered elements, such as video clips, audio clips, effects, and transitions between clips.</span></span> <span data-ttu-id="4c9a3-108">Il motore di rendering utilizza la sequenza temporale per creare un grafico di filtro, dal quale l'applicazione può generare l'output sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-108">The render engine uses the timeline to create a filter graph, from which the application can generate the rendered output.</span></span>

<span data-ttu-id="4c9a3-109">`IAMTimeline` esegue tre servizi di base.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-109">`IAMTimeline` performs three basic services.</span></span> <span data-ttu-id="4c9a3-110">Esso</span><span class="sxs-lookup"><span data-stu-id="4c9a3-110">It</span></span>

-   <span data-ttu-id="4c9a3-111">Crea gli oggetti nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-111">Creates the objects in the timeline.</span></span>
-   <span data-ttu-id="4c9a3-112">Funge da contenitore per tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-112">Acts as a container for those objects.</span></span>
-   <span data-ttu-id="4c9a3-113">Imposta e recupera i parametri generali della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-113">Sets and retrieves general parameters of the timeline.</span></span>

<span data-ttu-id="4c9a3-114">Per creare l'oggetto sequenza temporale, chiamare **CoCreateInstance** con l'identificatore di classe CLSID \_ AMTimeline.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-114">To create the timeline object, call **CoCreateInstance** with the class identifier CLSID\_AMTimeline.</span></span>

## <a name="members"></a><span data-ttu-id="4c9a3-115">Membri</span><span class="sxs-lookup"><span data-stu-id="4c9a3-115">Members</span></span>

<span data-ttu-id="4c9a3-116">L'interfaccia **IAMTimeline** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4c9a3-116">The **IAMTimeline** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4c9a3-117">**IAMTimeline** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4c9a3-117">**IAMTimeline** also has these types of members:</span></span>

-   [<span data-ttu-id="4c9a3-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="4c9a3-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4c9a3-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="4c9a3-119">Methods</span></span>

<span data-ttu-id="4c9a3-120">L'interfaccia **IAMTimeline** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-120">The **IAMTimeline** interface has these methods.</span></span>



| <span data-ttu-id="4c9a3-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="4c9a3-121">Method</span></span>                                                             | <span data-ttu-id="4c9a3-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c9a3-122">Description</span></span>                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c9a3-123">**AddGroup**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-123">**AddGroup**</span></span>](iamtimeline-addgroup.md)                           | <span data-ttu-id="4c9a3-124">Aggiunge un gruppo alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-124">Adds a group to the timeline.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4c9a3-125">**ClearAllGroups**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-125">**ClearAllGroups**</span></span>](iamtimeline-clearallgroups.md)               | <span data-ttu-id="4c9a3-126">Rimuove tutti i gruppi dalla sequenza temporale, insieme a tutti gli oggetti contenuti in tali gruppi.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-126">Removes all groups from the timeline, along with all objects contained in those groups.</span></span><br/>                                |
| [<span data-ttu-id="4c9a3-127">**CreateEmptyNode**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-127">**CreateEmptyNode**</span></span>](iamtimeline-createemptynode.md)             | <span data-ttu-id="4c9a3-128">Crea un nuovo oggetto sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-128">Creates a new timeline object.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4c9a3-129">**EffectsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-129">**EffectsEnabled**</span></span>](iamtimeline-effectsenabled.md)               | <span data-ttu-id="4c9a3-130">Determina se gli effetti sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-130">Determines whether effects are enabled.</span></span><br/>                                                                                |
| [<span data-ttu-id="4c9a3-131">**EnableEffects**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-131">**EnableEffects**</span></span>](iamtimeline-enableeffects.md)                 | <span data-ttu-id="4c9a3-132">Abilita o Disabilita tutti gli effetti nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-132">Enables or disables all effects in the timeline.</span></span><br/>                                                                       |
| [<span data-ttu-id="4c9a3-133">**EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-133">**EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)         | <span data-ttu-id="4c9a3-134">Abilita o Disabilita tutte le transizioni nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-134">Enables or disables all transitions in the timeline.</span></span><br/>                                                                   |
| [<span data-ttu-id="4c9a3-135">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-135">**GetCountOfType**</span></span>](iamtimeline-getcountoftype.md)               | <span data-ttu-id="4c9a3-136">Recupera il numero di oggetti del tipo specificato contenuti in un gruppo specificato e in tutti i relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-136">Retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span><br/> |
| [<span data-ttu-id="4c9a3-137">**GetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-137">**GetDefaultEffect**</span></span>](iamtimeline-getdefaulteffect.md)           | <span data-ttu-id="4c9a3-138">Recupera l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-138">Retrieves the default effect.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4c9a3-139">**GetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-139">**GetDefaultEffectB**</span></span>](iamtimeline-getdefaulteffectb.md)         | <span data-ttu-id="4c9a3-140">Recupera l'effetto predefinito come valore **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4c9a3-140">Retrieves the default effect as a **BSTR** value.</span></span><br/>                                                                      |
| [<span data-ttu-id="4c9a3-141">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-141">**GetDefaultFPS**</span></span>](iamtimeline-getdefaultfps.md)                 | <span data-ttu-id="4c9a3-142">Recupera la frequenza dei fotogrammi di output predefinita, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-142">Retrieves the default output frame rate, in frames per second.</span></span><br/>                                                         |
| [<span data-ttu-id="4c9a3-143">**GetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-143">**GetDefaultTransition**</span></span>](iamtimeline-getdefaulttransition.md)   | <span data-ttu-id="4c9a3-144">Recupera la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-144">Retrieves the default transition.</span></span><br/>                                                                                      |
| [<span data-ttu-id="4c9a3-145">**GetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-145">**GetDefaultTransitionB**</span></span>](iamtimeline-getdefaulttransitionb.md) | <span data-ttu-id="4c9a3-146">Recupera la transizione predefinita come valore **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4c9a3-146">Retrieves the default transition as a **BSTR** value.</span></span><br/>                                                                  |
| [<span data-ttu-id="4c9a3-147">**GetDirtyRange**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-147">**GetDirtyRange**</span></span>](iamtimeline-getdirtyrange.md)                 | <span data-ttu-id="4c9a3-148">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-148">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4c9a3-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-149">**GetDuration**</span></span>](iamtimeline-getduration.md)                     | <span data-ttu-id="4c9a3-150">Recupera la durata della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-150">Retrieves the timeline duration.</span></span><br/>                                                                                       |
| [<span data-ttu-id="4c9a3-151">**GetDuration2**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-151">**GetDuration2**</span></span>](iamtimeline-getduration2.md)                   | <span data-ttu-id="4c9a3-152">Recupera la durata della sequenza temporale come **valore Double**.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-152">Retrieves the timeline duration as a **double**.</span></span><br/>                                                                       |
| [<span data-ttu-id="4c9a3-153">**GetGroup**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-153">**GetGroup**</span></span>](iamtimeline-getgroup.md)                           | <span data-ttu-id="4c9a3-154">Recupera un gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-154">Retrieves a specified group.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4c9a3-155">**GetGroupCount**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-155">**GetGroupCount**</span></span>](iamtimeline-getgroupcount.md)                 | <span data-ttu-id="4c9a3-156">Recupera il numero di gruppi contenuti nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-156">Retrieves the number of groups that are contained in the timeline.</span></span><br/>                                                     |
| [<span data-ttu-id="4c9a3-157">**GetInsertMode**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-157">**GetInsertMode**</span></span>](iamtimeline-getinsertmode.md)                 | <span data-ttu-id="4c9a3-158">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-158">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4c9a3-159">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-159">**IsDirty**</span></span>](iamtimeline-isdirty.md)                             | <span data-ttu-id="4c9a3-160">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-160">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4c9a3-161">**RemGroupFromList**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-161">**RemGroupFromList**</span></span>](iamtimeline-remgroupfromlist.md)           | <span data-ttu-id="4c9a3-162">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-162">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4c9a3-163">**SetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-163">**SetDefaultEffect**</span></span>](iamtimeline-setdefaulteffect.md)           | <span data-ttu-id="4c9a3-164">Imposta l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-164">Sets the default effect.</span></span><br/>                                                                                               |
| [<span data-ttu-id="4c9a3-165">**SetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-165">**SetDefaultEffectB**</span></span>](iamtimeline-setdefaulteffectb.md)         | <span data-ttu-id="4c9a3-166">Imposta l'effetto predefinito come valore **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4c9a3-166">Sets the default effect as a **BSTR** value.</span></span><br/>                                                                           |
| [<span data-ttu-id="4c9a3-167">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-167">**SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)                 | <span data-ttu-id="4c9a3-168">Imposta la frequenza dei fotogrammi di output predefinita, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-168">Sets the default output frame rate, in frames per second.</span></span><br/>                                                              |
| [<span data-ttu-id="4c9a3-169">**SetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-169">**SetDefaultTransition**</span></span>](iamtimeline-setdefaulttransition.md)   | <span data-ttu-id="4c9a3-170">Imposta la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-170">Sets the default transition.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4c9a3-171">**SetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-171">**SetDefaultTransitionB**</span></span>](iamtimeline-setdefaulttransitionb.md) | <span data-ttu-id="4c9a3-172">Imposta la transizione predefinita come valore BSTR.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-172">Sets the default transition as a BSTR value.</span></span><br/>                                                                           |
| [<span data-ttu-id="4c9a3-173">**SetInsertMode**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-173">**SetInsertMode**</span></span>](iamtimeline-setinsertmode.md)                 | <span data-ttu-id="4c9a3-174">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-174">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4c9a3-175">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-175">**SetInterestRange**</span></span>](iamtimeline-setinterestrange.md)           | <span data-ttu-id="4c9a3-176">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-176">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4c9a3-177">**TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-177">**TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)       | <span data-ttu-id="4c9a3-178">Determina se le transizioni sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-178">Determines whether transitions are enabled.</span></span><br/>                                                                            |
| [<span data-ttu-id="4c9a3-179">**ValidateSourceNames**</span><span class="sxs-lookup"><span data-stu-id="4c9a3-179">**ValidateSourceNames**</span></span>](iamtimeline-validatesourcenames.md)     | <span data-ttu-id="4c9a3-180">Convalida i nomi di origine nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-180">Validates source names in the timeline.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="4c9a3-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c9a3-181">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c9a3-182">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-182">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c9a3-183">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c9a3-183">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c9a3-184">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4c9a3-184">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c9a3-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c9a3-185">Requirements</span></span>



| <span data-ttu-id="4c9a3-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c9a3-186">Requirement</span></span> | <span data-ttu-id="4c9a3-187">Valore</span><span class="sxs-lookup"><span data-stu-id="4c9a3-187">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9a3-188">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c9a3-188">Header</span></span><br/>  | <dl> <span data-ttu-id="4c9a3-189"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9a3-189"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c9a3-190">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c9a3-190">Library</span></span><br/> | <dl> <span data-ttu-id="4c9a3-191"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c9a3-191"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 

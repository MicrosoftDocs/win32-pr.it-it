---
description: Gestisce i collegamenti della shell. Questo oggetto rende disponibile gran parte delle funzionalità dell'interfaccia IShellLink alle applicazioni di scripting.
title: Oggetto ShellLinkObject (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 5862ae3c9b7bf1262edbc28b06f2963f2e577275
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842632"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="07a32-104">Oggetto ShellLinkObject</span><span class="sxs-lookup"><span data-stu-id="07a32-104">ShellLinkObject object</span></span>

<span data-ttu-id="07a32-105">Gestisce i collegamenti della shell.</span><span class="sxs-lookup"><span data-stu-id="07a32-105">Manages Shell links.</span></span> <span data-ttu-id="07a32-106">Questo oggetto rende disponibile gran parte delle funzionalità [**dell'interfaccia IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) alle applicazioni di scripting.</span><span class="sxs-lookup"><span data-stu-id="07a32-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="07a32-107">Membri</span><span class="sxs-lookup"><span data-stu-id="07a32-107">Members</span></span>

<span data-ttu-id="07a32-108">**L'oggetto ShellLinkObject** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="07a32-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="07a32-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="07a32-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="07a32-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07a32-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07a32-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="07a32-111">Methods</span></span>

<span data-ttu-id="07a32-112">**L'oggetto ShellLinkObject** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="07a32-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="07a32-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="07a32-113">Method</span></span>                                                     | <span data-ttu-id="07a32-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07a32-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07a32-115">**GetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="07a32-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="07a32-116">Ottiene il percorso dell'icona assegnata al collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="07a32-117">**Risolvi**</span><span class="sxs-lookup"><span data-stu-id="07a32-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="07a32-118">Cerca la destinazione di un collegamento shell, anche se la destinazione è stata spostata o rinominata.</span><span class="sxs-lookup"><span data-stu-id="07a32-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="07a32-119">**Salva**</span><span class="sxs-lookup"><span data-stu-id="07a32-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="07a32-120">Salva tutte le modifiche apportate al collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="07a32-121">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="07a32-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="07a32-122">Imposta la posizione dell'icona assegnata al collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="07a32-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07a32-123">Properties</span></span>

<span data-ttu-id="07a32-124">**L'oggetto ShellLinkObject** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="07a32-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="07a32-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07a32-125">Property</span></span>                                                                | <span data-ttu-id="07a32-126">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="07a32-126">Access type</span></span>           | <span data-ttu-id="07a32-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07a32-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07a32-128">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="07a32-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="07a32-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07a32-129">Read/write</span></span><br/> | <span data-ttu-id="07a32-130">Contiene gli argomenti di un collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="07a32-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="07a32-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="07a32-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07a32-132">Read/write</span></span><br/> | <span data-ttu-id="07a32-133">Ottiene o imposta la descrizione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="07a32-134">**Tasto di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="07a32-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="07a32-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07a32-135">Read/write</span></span><br/> | <span data-ttu-id="07a32-136">Ottiene o imposta il tasto di scelta rapida per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="07a32-137">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="07a32-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="07a32-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07a32-138">Read/write</span></span><br/> | <span data-ttu-id="07a32-139">Ottiene o imposta il percorso dell'oggetto collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="07a32-140">**ShowCommand**</span><span class="sxs-lookup"><span data-stu-id="07a32-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="07a32-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07a32-141">Read/write</span></span><br/> | <span data-ttu-id="07a32-142">Ottiene o imposta lo stato di visualizzazione iniziale (ridimensionato, ridotto a icona o ingrandito) del comando del collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="07a32-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="07a32-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="07a32-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07a32-144">Read/write</span></span><br/> | <span data-ttu-id="07a32-145">Ottiene o imposta la directory di lavoro specificata nel collegamento.</span><span class="sxs-lookup"><span data-stu-id="07a32-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="07a32-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07a32-146">Requirements</span></span>



| <span data-ttu-id="07a32-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="07a32-147">Requirement</span></span> | <span data-ttu-id="07a32-148">Valore</span><span class="sxs-lookup"><span data-stu-id="07a32-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a32-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a32-149">Minimum supported client</span></span><br/> | <span data-ttu-id="07a32-150">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="07a32-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07a32-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a32-151">Minimum supported server</span></span><br/> | <span data-ttu-id="07a32-152">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="07a32-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="07a32-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07a32-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="07a32-154"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="07a32-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="07a32-155">Idl</span><span class="sxs-lookup"><span data-stu-id="07a32-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07a32-156"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="07a32-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="07a32-157">DLL</span><span class="sxs-lookup"><span data-stu-id="07a32-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07a32-158"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="07a32-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07a32-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07a32-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a32-160">Collegamenti alla shell</span><span class="sxs-lookup"><span data-stu-id="07a32-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 

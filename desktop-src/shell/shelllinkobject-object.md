---
description: Gestisce i collegamenti della shell. Questo oggetto rende la maggior parte delle funzionalità dell'interfaccia IShellLink disponibili per le applicazioni di scripting.
title: Oggetto ShellLinkObject (shldisp. h)
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
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980730"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="496d0-104">Oggetto ShellLinkObject</span><span class="sxs-lookup"><span data-stu-id="496d0-104">ShellLinkObject object</span></span>

<span data-ttu-id="496d0-105">Gestisce i collegamenti della shell.</span><span class="sxs-lookup"><span data-stu-id="496d0-105">Manages Shell links.</span></span> <span data-ttu-id="496d0-106">Questo oggetto rende la maggior parte delle funzionalità dell'interfaccia [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) disponibili per le applicazioni di scripting.</span><span class="sxs-lookup"><span data-stu-id="496d0-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="496d0-107">Membri</span><span class="sxs-lookup"><span data-stu-id="496d0-107">Members</span></span>

<span data-ttu-id="496d0-108">L'oggetto **ShellLinkObject** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="496d0-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="496d0-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="496d0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="496d0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="496d0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="496d0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="496d0-111">Methods</span></span>

<span data-ttu-id="496d0-112">L'oggetto **ShellLinkObject** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="496d0-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="496d0-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="496d0-113">Method</span></span>                                                     | <span data-ttu-id="496d0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="496d0-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="496d0-115">**GetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="496d0-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="496d0-116">Ottiene la posizione dell'icona assegnata al collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="496d0-117">**Risolvi**</span><span class="sxs-lookup"><span data-stu-id="496d0-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="496d0-118">Cerca la destinazione di un collegamento della shell, anche se la destinazione è stata spostata o rinominata.</span><span class="sxs-lookup"><span data-stu-id="496d0-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="496d0-119">**Salva**</span><span class="sxs-lookup"><span data-stu-id="496d0-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="496d0-120">Salva tutte le modifiche apportate al collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="496d0-121">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="496d0-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="496d0-122">Imposta la posizione dell'icona assegnata al collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="496d0-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="496d0-123">Properties</span></span>

<span data-ttu-id="496d0-124">L'oggetto **ShellLinkObject** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="496d0-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="496d0-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="496d0-125">Property</span></span>                                                                | <span data-ttu-id="496d0-126">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="496d0-126">Access type</span></span>           | <span data-ttu-id="496d0-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="496d0-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="496d0-128">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="496d0-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="496d0-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="496d0-129">Read/write</span></span><br/> | <span data-ttu-id="496d0-130">Contiene gli argomenti di un collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="496d0-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="496d0-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="496d0-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="496d0-132">Read/write</span></span><br/> | <span data-ttu-id="496d0-133">Ottiene o imposta la descrizione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="496d0-134">**Tasto di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="496d0-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="496d0-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="496d0-135">Read/write</span></span><br/> | <span data-ttu-id="496d0-136">Ottiene o imposta il tasto di scelta rapida per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="496d0-137">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="496d0-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="496d0-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="496d0-138">Read/write</span></span><br/> | <span data-ttu-id="496d0-139">Ottiene o imposta il percorso dell'oggetto collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="496d0-140">**ShowCommand**</span><span class="sxs-lookup"><span data-stu-id="496d0-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="496d0-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="496d0-141">Read/write</span></span><br/> | <span data-ttu-id="496d0-142">Ottiene o imposta lo stato di visualizzazione iniziale (ridimensionato, ridotto a icona o ingrandito) del comando del collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="496d0-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="496d0-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="496d0-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="496d0-144">Read/write</span></span><br/> | <span data-ttu-id="496d0-145">Ottiene o imposta la directory di lavoro specificata nel collegamento.</span><span class="sxs-lookup"><span data-stu-id="496d0-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="496d0-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="496d0-146">Requirements</span></span>



| <span data-ttu-id="496d0-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="496d0-147">Requirement</span></span> | <span data-ttu-id="496d0-148">Valore</span><span class="sxs-lookup"><span data-stu-id="496d0-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="496d0-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="496d0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="496d0-150">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="496d0-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="496d0-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="496d0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="496d0-152">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="496d0-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="496d0-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="496d0-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="496d0-154"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="496d0-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="496d0-155">IDL</span><span class="sxs-lookup"><span data-stu-id="496d0-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="496d0-156"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="496d0-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="496d0-157">DLL</span><span class="sxs-lookup"><span data-stu-id="496d0-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="496d0-158"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="496d0-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="496d0-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="496d0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496d0-160">Collegamenti Shell</span><span class="sxs-lookup"><span data-stu-id="496d0-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 

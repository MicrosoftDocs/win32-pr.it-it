---
description: Rappresenta gli oggetti in una visualizzazione e fornisce le proprietà e i metodi utilizzati per ottenere informazioni sul contenuto della visualizzazione.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Oggetto ShellFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994997"
---
# <a name="shellfolderview-object"></a><span data-ttu-id="62c6a-103">Oggetto ShellFolderView</span><span class="sxs-lookup"><span data-stu-id="62c6a-103">ShellFolderView object</span></span>

<span data-ttu-id="62c6a-104">Rappresenta gli oggetti in una visualizzazione e fornisce le proprietà e i metodi utilizzati per ottenere informazioni sul contenuto della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="62c6a-104">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span>

## <a name="members"></a><span data-ttu-id="62c6a-105">Membri</span><span class="sxs-lookup"><span data-stu-id="62c6a-105">Members</span></span>

<span data-ttu-id="62c6a-106">L'oggetto **ShellFolderView** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="62c6a-106">The **ShellFolderView** object has these types of members:</span></span>

-   [<span data-ttu-id="62c6a-107">Eventi</span><span class="sxs-lookup"><span data-stu-id="62c6a-107">Events</span></span>](#events)
-   [<span data-ttu-id="62c6a-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="62c6a-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="62c6a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="62c6a-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="62c6a-110">Eventi</span><span class="sxs-lookup"><span data-stu-id="62c6a-110">Events</span></span>

<span data-ttu-id="62c6a-111">L'oggetto **ShellFolderView** presenta questi eventi.</span><span class="sxs-lookup"><span data-stu-id="62c6a-111">The **ShellFolderView** object has these events.</span></span>



| <span data-ttu-id="62c6a-112">Event</span><span class="sxs-lookup"><span data-stu-id="62c6a-112">Event</span></span>                                                        | <span data-ttu-id="62c6a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62c6a-113">Description</span></span>                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="62c6a-114">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="62c6a-114">**SelectionChanged**</span></span>](shellfolderview-selectionchanged.md) | <span data-ttu-id="62c6a-115">Si verifica quando viene modificato lo stato di selezione di un elemento o di elementi nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="62c6a-115">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="62c6a-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="62c6a-116">Methods</span></span>

<span data-ttu-id="62c6a-117">L'oggetto **ShellFolderView** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="62c6a-117">The **ShellFolderView** object has these methods.</span></span>



| <span data-ttu-id="62c6a-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="62c6a-118">Method</span></span>                                                 | <span data-ttu-id="62c6a-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62c6a-119">Description</span></span>                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62c6a-120">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="62c6a-120">**PopupItemMenu**</span></span>](shellfolderview-popupitemmenu.md) | <span data-ttu-id="62c6a-121">Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.</span><span class="sxs-lookup"><span data-stu-id="62c6a-121">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                 |
| [<span data-ttu-id="62c6a-122">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="62c6a-122">**SelectedItems**</span></span>](shellfolderview-selecteditems.md) | <span data-ttu-id="62c6a-123">Ottiene un oggetto [**FolderItems**](folderitems.md) che rappresenta tutti gli elementi selezionati nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="62c6a-123">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="62c6a-124">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="62c6a-124">**SelectItem**</span></span>](shellfolderview-selectitem.md)       | <span data-ttu-id="62c6a-125">Imposta lo stato di selezione di un elemento nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="62c6a-125">Sets the selection state of an item in the view.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="62c6a-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="62c6a-126">Properties</span></span>

<span data-ttu-id="62c6a-127">L'oggetto **ShellFolderView** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="62c6a-127">The **ShellFolderView** object has these properties.</span></span>



| <span data-ttu-id="62c6a-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="62c6a-128">Property</span></span>                                                      | <span data-ttu-id="62c6a-129">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="62c6a-129">Access type</span></span>          | <span data-ttu-id="62c6a-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62c6a-130">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62c6a-131">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="62c6a-131">**Application**</span></span>](shellfolderview-application.md)<br/> | <span data-ttu-id="62c6a-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="62c6a-132">Read-only</span></span><br/> | <span data-ttu-id="62c6a-133">Contiene l'oggetto applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="62c6a-133">Contains the object's Application object.</span></span><br/>                                                         |
| [<span data-ttu-id="62c6a-134">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="62c6a-134">**FocusedItem**</span></span>](shellfolderview-focuseditem.md)<br/> | <span data-ttu-id="62c6a-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="62c6a-135">Read-only</span></span><br/> | <span data-ttu-id="62c6a-136">Ottiene un oggetto [**FolderItem**](folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="62c6a-136">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span><br/> |
| [<span data-ttu-id="62c6a-137">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="62c6a-137">**Folder**</span></span>](shellfolderview-folder.md)<br/>           | <span data-ttu-id="62c6a-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="62c6a-138">Read-only</span></span><br/> | <span data-ttu-id="62c6a-139">Ottiene un oggetto [**cartella**](folder.md) che rappresenta la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="62c6a-139">Gets a [**Folder**](folder.md) object that represents the view.</span></span><br/>                                  |
| [<span data-ttu-id="62c6a-140">**Padre**</span><span class="sxs-lookup"><span data-stu-id="62c6a-140">**Parent**</span></span>](shellfolderview-parent.md)<br/>           | <span data-ttu-id="62c6a-141">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="62c6a-141">Read-only</span></span><br/> | <span data-ttu-id="62c6a-142">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="62c6a-142">Not implemented.</span></span><br/>                                                                                  |
| [<span data-ttu-id="62c6a-143">**Script**</span><span class="sxs-lookup"><span data-stu-id="62c6a-143">**Script**</span></span>](shellfolderview-script.md)<br/>           | <span data-ttu-id="62c6a-144">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="62c6a-144">Read-only</span></span><br/> | <span data-ttu-id="62c6a-145">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="62c6a-145">Deprecated.</span></span><br/>                                                                                       |
| [<span data-ttu-id="62c6a-146">**ViewOptions**</span><span class="sxs-lookup"><span data-stu-id="62c6a-146">**ViewOptions**</span></span>](shellfolderview-viewoptions.md)<br/> | <span data-ttu-id="62c6a-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="62c6a-147">Read-only</span></span><br/> | <span data-ttu-id="62c6a-148">Ottiene un set di flag che indicano le opzioni correnti della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="62c6a-148">Gets a set of flags that indicate the current options of the view.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="62c6a-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62c6a-149">Requirements</span></span>



| <span data-ttu-id="62c6a-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c6a-150">Requirement</span></span> | <span data-ttu-id="62c6a-151">Valore</span><span class="sxs-lookup"><span data-stu-id="62c6a-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c6a-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c6a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="62c6a-153">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="62c6a-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="62c6a-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c6a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="62c6a-155">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62c6a-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="62c6a-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62c6a-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c6a-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c6a-157"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="62c6a-158">IDL</span><span class="sxs-lookup"><span data-stu-id="62c6a-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62c6a-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62c6a-159"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="62c6a-160">DLL</span><span class="sxs-lookup"><span data-stu-id="62c6a-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c6a-161"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="62c6a-161"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |
| <span data-ttu-id="62c6a-162">IID</span><span class="sxs-lookup"><span data-stu-id="62c6a-162">IID</span></span><br/>                      | <span data-ttu-id="62c6a-163">\_SHELLFOLDERVIEW CLSID</span><span class="sxs-lookup"><span data-stu-id="62c6a-163">CLSID\_ShellFolderView</span></span><br/>                                                                              |



## <a name="see-also"></a><span data-ttu-id="62c6a-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62c6a-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c6a-165">**Flag ShellFolderViewOptions**</span><span class="sxs-lookup"><span data-stu-id="62c6a-165">**ShellFolderViewOptions Flags**</span></span>](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 





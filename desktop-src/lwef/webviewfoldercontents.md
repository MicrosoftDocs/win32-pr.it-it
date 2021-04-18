---
title: Oggetto WebViewFolderContents (Shldisp.h)
description: Implementato dalla Shell per l'utilizzo all'interno di una visualizzazione WebView.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents
- Funzionalità dell'ambiente Windows legacy dell'oggetto WebViewFolderContents, descritte
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301032"
---
# <a name="webviewfoldercontents-object"></a><span data-ttu-id="97aa3-105">Oggetto WebViewFolderContents</span><span class="sxs-lookup"><span data-stu-id="97aa3-105">WebViewFolderContents object</span></span>

<span data-ttu-id="97aa3-106">Implementato dalla Shell per l'utilizzo all'interno di una *visualizzazione WebView*.</span><span class="sxs-lookup"><span data-stu-id="97aa3-106">Implemented by the Shell for use inside a *WebView*.</span></span> <span data-ttu-id="97aa3-107">**WebViewFolderContents** si inizializza automaticamente nella cartella corrente di WebView.</span><span class="sxs-lookup"><span data-stu-id="97aa3-107">**WebViewFolderContents** automatically initializes itself to WebView's current folder.</span></span> <span data-ttu-id="97aa3-108">Viene creata una visualizzazione di cartelle della shell che Visualizza il contenuto della cartella in uno dei cinque formati seguenti: icona piccola, icona grande, elenco, dettagli o anteprima.</span><span class="sxs-lookup"><span data-stu-id="97aa3-108">It creates a Shell folder view that displays the contents of the folder in one of five formats: Small Icon, Large Icon, List, Details, or Thumbnail.</span></span> <span data-ttu-id="97aa3-109">Non è valido all'esterno di una WebView.</span><span class="sxs-lookup"><span data-stu-id="97aa3-109">It is not valid outside of a WebView.</span></span>

<span data-ttu-id="97aa3-110">I metodi e le proprietà esposte da **WebViewFolderContents** sono identici a quelli dell'oggetto [**ShellFolderView**](/windows/desktop/shell/shellfolderview) .</span><span class="sxs-lookup"><span data-stu-id="97aa3-110">The methods and properties exposed by **WebViewFolderContents** are identical to those of the [**ShellFolderView**](/windows/desktop/shell/shellfolderview) object.</span></span>

## <a name="members"></a><span data-ttu-id="97aa3-111">Membri</span><span class="sxs-lookup"><span data-stu-id="97aa3-111">Members</span></span>

<span data-ttu-id="97aa3-112">L'oggetto **WebViewFolderContents** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="97aa3-112">The **WebViewFolderContents** object has these types of members:</span></span>

-   [<span data-ttu-id="97aa3-113">Eventi</span><span class="sxs-lookup"><span data-stu-id="97aa3-113">Events</span></span>](#events)
-   [<span data-ttu-id="97aa3-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="97aa3-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="97aa3-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97aa3-115">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="97aa3-116">Eventi</span><span class="sxs-lookup"><span data-stu-id="97aa3-116">Events</span></span>

<span data-ttu-id="97aa3-117">L'oggetto **WebViewFolderContents** presenta questi eventi.</span><span class="sxs-lookup"><span data-stu-id="97aa3-117">The **WebViewFolderContents** object has these events.</span></span>



| <span data-ttu-id="97aa3-118">Event</span><span class="sxs-lookup"><span data-stu-id="97aa3-118">Event</span></span>                                                              | <span data-ttu-id="97aa3-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97aa3-119">Description</span></span>                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="97aa3-120">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="97aa3-120">**SelectionChanged**</span></span>](webviewfoldercontents-selectionchanged.md) | <span data-ttu-id="97aa3-121">Si verifica quando viene modificato lo stato di selezione di un elemento o di elementi nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97aa3-121">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="97aa3-122">Metodi</span><span class="sxs-lookup"><span data-stu-id="97aa3-122">Methods</span></span>

<span data-ttu-id="97aa3-123">L'oggetto **WebViewFolderContents** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="97aa3-123">The **WebViewFolderContents** object has these methods.</span></span>



| <span data-ttu-id="97aa3-124">Metodo</span><span class="sxs-lookup"><span data-stu-id="97aa3-124">Method</span></span>                                                       | <span data-ttu-id="97aa3-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97aa3-125">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97aa3-126">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="97aa3-126">**PopupItemMenu**</span></span>](webviewfoldercontents-popupitemmenu.md) | <span data-ttu-id="97aa3-127">Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.</span><span class="sxs-lookup"><span data-stu-id="97aa3-127">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                   |
| [<span data-ttu-id="97aa3-128">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="97aa3-128">**SelectedItems**</span></span>](webviewfoldercontents-selecteditems.md) | <span data-ttu-id="97aa3-129">Ottiene un oggetto [**FolderItems**](../shell/folderitems.md) che rappresenta tutti gli elementi selezionati nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97aa3-129">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="97aa3-130">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="97aa3-130">**SelectItem**</span></span>](webviewfoldercontents-selectitem.md)       | <span data-ttu-id="97aa3-131">Imposta lo stato di selezione di un elemento nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97aa3-131">Sets the selection state of an item in the view.</span></span><br/>                                                          |



 

### <a name="properties"></a><span data-ttu-id="97aa3-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97aa3-132">Properties</span></span>

<span data-ttu-id="97aa3-133">L'oggetto **WebViewFolderContents** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="97aa3-133">The **WebViewFolderContents** object has these properties.</span></span>



| <span data-ttu-id="97aa3-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97aa3-134">Property</span></span>                                                            | <span data-ttu-id="97aa3-135">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="97aa3-135">Access type</span></span>          | <span data-ttu-id="97aa3-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97aa3-136">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97aa3-137">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="97aa3-137">**Application**</span></span>](webviewfoldercontents-application.md)<br/> | <span data-ttu-id="97aa3-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97aa3-138">Read-only</span></span><br/> | <span data-ttu-id="97aa3-139">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="97aa3-139">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="97aa3-140">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="97aa3-140">**FocusedItem**</span></span>](webviewfoldercontents-focuseditem.md)<br/> | <span data-ttu-id="97aa3-141">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97aa3-141">Read-only</span></span><br/> | <span data-ttu-id="97aa3-142">Ottiene un oggetto [**FolderItem**](../shell/folderitem.md) che rappresenta l'elemento con lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="97aa3-142">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span><br/>                           |
| [<span data-ttu-id="97aa3-143">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="97aa3-143">**Folder**</span></span>](webviewfoldercontents-folder.md)<br/>           | <span data-ttu-id="97aa3-144">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97aa3-144">Read-only</span></span><br/> | <span data-ttu-id="97aa3-145">Ottiene un oggetto [**cartella**](../shell/folder.md) che rappresenta la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97aa3-145">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span><br/>                                                            |
| [<span data-ttu-id="97aa3-146">**Padre**</span><span class="sxs-lookup"><span data-stu-id="97aa3-146">**Parent**</span></span>](webviewfoldercontents-parent.md)<br/>           | <span data-ttu-id="97aa3-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97aa3-147">Read-only</span></span><br/> | <span data-ttu-id="97aa3-148">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="97aa3-148">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="97aa3-149">**Script**</span><span class="sxs-lookup"><span data-stu-id="97aa3-149">**Script**</span></span>](webviewfoldercontents-script.md)<br/>           | <span data-ttu-id="97aa3-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97aa3-150">Read-only</span></span><br/> | <span data-ttu-id="97aa3-151">Ottiene l'oggetto di scripting per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97aa3-151">Gets the scripting object for the view.</span></span><br/>                                                                                       |
| [<span data-ttu-id="97aa3-152">**ViewOptions**</span><span class="sxs-lookup"><span data-stu-id="97aa3-152">**ViewOptions**</span></span>](webviewfoldercontents-viewoptions.md)<br/> | <span data-ttu-id="97aa3-153">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="97aa3-153">Read-only</span></span><br/> | <span data-ttu-id="97aa3-154">Ottiene un set di flag [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) che indicano le opzioni correnti della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97aa3-154">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="97aa3-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97aa3-155">Requirements</span></span>



| <span data-ttu-id="97aa3-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="97aa3-156">Requirement</span></span> | <span data-ttu-id="97aa3-157">Valore</span><span class="sxs-lookup"><span data-stu-id="97aa3-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97aa3-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97aa3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="97aa3-159">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="97aa3-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="97aa3-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97aa3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="97aa3-161">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97aa3-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="97aa3-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97aa3-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="97aa3-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97aa3-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="97aa3-164">IDL</span><span class="sxs-lookup"><span data-stu-id="97aa3-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97aa3-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97aa3-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="97aa3-166">DLL</span><span class="sxs-lookup"><span data-stu-id="97aa3-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97aa3-167"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="97aa3-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 


---
description: Inoltra gli eventi generati da un oggetto ShellFolderView specificato ai gestori eventi ShellFolderViewOC corrispondenti.
title: Oggetto ShellFolderViewOC (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: 2670578417dc616d30f319887f5281fa5d0615f5
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840872"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="e84c8-103">Oggetto ShellFolderViewOC</span><span class="sxs-lookup"><span data-stu-id="e84c8-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="e84c8-104">Inoltra gli eventi generati da un oggetto [**ShellFolderView**](shellfolderview.md) specificato ai gestori **eventi ShellFolderViewOC** corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="e84c8-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="e84c8-105">Membri</span><span class="sxs-lookup"><span data-stu-id="e84c8-105">Members</span></span>

<span data-ttu-id="e84c8-106">**L'oggetto ShellFolderViewOC** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e84c8-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="e84c8-107">Eventi</span><span class="sxs-lookup"><span data-stu-id="e84c8-107">Events</span></span>](#events)
-   [<span data-ttu-id="e84c8-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="e84c8-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="e84c8-109">Eventi</span><span class="sxs-lookup"><span data-stu-id="e84c8-109">Events</span></span>

<span data-ttu-id="e84c8-110">**L'oggetto ShellFolderViewOC** include questi eventi.</span><span class="sxs-lookup"><span data-stu-id="e84c8-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="e84c8-111">Event</span><span class="sxs-lookup"><span data-stu-id="e84c8-111">Event</span></span>                                                          | <span data-ttu-id="e84c8-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e84c8-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e84c8-113">**EnumDone**</span><span class="sxs-lookup"><span data-stu-id="e84c8-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="e84c8-114">Indica che [**l'oggetto ShellFolderView**](shellfolderview.md) ha terminato l'enumerazione del contenuto della cartella.</span><span class="sxs-lookup"><span data-stu-id="e84c8-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="e84c8-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="e84c8-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="e84c8-116">Indica che lo stato di selezione di uno o più elementi nella visualizzazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="e84c8-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="e84c8-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="e84c8-117">Methods</span></span>

<span data-ttu-id="e84c8-118">**L'oggetto ShellFolderViewOC** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e84c8-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="e84c8-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="e84c8-119">Method</span></span>                                                   | <span data-ttu-id="e84c8-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e84c8-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e84c8-121">**SetFolderView**</span><span class="sxs-lookup"><span data-stu-id="e84c8-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="e84c8-122">Inoltra gli eventi dell'oggetto [**ShellFolderView**](shellfolderview.md) specificato al gestore eventi **ShellFolderViewOC** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e84c8-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e84c8-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e84c8-123">Remarks</span></span>

<span data-ttu-id="e84c8-124">[**L'oggetto ShellFolderView**](shellfolderview.md) genera due eventi, [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged,**](shellfolderviewoc-selectionchanged.md)in genere gestiti dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e84c8-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="e84c8-125">Tuttavia, alcune applicazioni devono gestire gli eventi da una serie di **oggetti ShellFolderView.**</span><span class="sxs-lookup"><span data-stu-id="e84c8-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="e84c8-126">Ad esempio, un'applicazione potrebbe ospitare un controllo WebBrowser che consente agli utenti di spostarsi tra una serie di cartelle.</span><span class="sxs-lookup"><span data-stu-id="e84c8-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="e84c8-127">Ogni cartella ha il proprio **oggetto ShellFolderView** con gli eventi associati.</span><span class="sxs-lookup"><span data-stu-id="e84c8-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="e84c8-128">La gestione di questi eventi può essere difficile.</span><span class="sxs-lookup"><span data-stu-id="e84c8-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="e84c8-129">**L'oggetto ShellFolderViewOC** semplifica la gestione degli eventi per tali scenari.</span><span class="sxs-lookup"><span data-stu-id="e84c8-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="e84c8-130">Consente alle applicazioni di gestire gli eventi per tutti [**gli oggetti ShellFolderView**](shellfolderview.md) con una singola coppia di gestori di eventi **ShellFolderViewOC.**</span><span class="sxs-lookup"><span data-stu-id="e84c8-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="e84c8-131">Ogni volta che l'utente passa a una nuova cartella, l'applicazione passa l'oggetto **ShellFolderView** associato **all'oggetto ShellFolderViewOC** chiamando [**SetFolderView.**](shellfolderviewoc-setfolderview.md)</span><span class="sxs-lookup"><span data-stu-id="e84c8-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="e84c8-132">Quindi, quando viene generato un evento [**EnumDone**](shellfolderviewoc-enumdone.md) o [**SelectionChanged,**](shellfolderviewoc-selectionchanged.md) l'oggetto **ShellFolderViewOC** inoltra l'evento al proprio gestore per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e84c8-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84c8-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e84c8-133">Requirements</span></span>



| <span data-ttu-id="e84c8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e84c8-134">Requirement</span></span> | <span data-ttu-id="e84c8-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e84c8-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e84c8-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e84c8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e84c8-137">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e84c8-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e84c8-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e84c8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e84c8-139">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e84c8-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e84c8-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e84c8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e84c8-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="e84c8-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e84c8-142">Idl</span><span class="sxs-lookup"><span data-stu-id="e84c8-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e84c8-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="e84c8-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e84c8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e84c8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e84c8-145"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e84c8-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e84c8-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e84c8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84c8-147">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="e84c8-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 





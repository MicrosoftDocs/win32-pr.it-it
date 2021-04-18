---
description: Implementazione delle estensioni del menu di scelta rapida
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementazione delle estensioni del menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312466"
---
# <a name="implementing-context-menu-extensions"></a><span data-ttu-id="690e6-103">Implementazione delle estensioni del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="690e6-103">Implementing Context Menu Extensions</span></span>

<span data-ttu-id="690e6-104">L'estensione dello spazio dei nomi WPD supporta i menu di scelta rapida (o collegamento) estensibile.</span><span class="sxs-lookup"><span data-stu-id="690e6-104">The WPD Namespace Extension supports extensible context (or shortcut) menus.</span></span> <span data-ttu-id="690e6-105">Questi sono i menu che vengono visualizzati quando un utente fa clic con il pulsante destro del mouse su un oggetto, ad esempio un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="690e6-105">These are the menus that appear when a user right-clicks on an object such as a file or a folder.</span></span> <span data-ttu-id="690e6-106">Alcune applicazioni WPD sfruttano i vantaggi di questi menu estendibili per supportare operazioni sul contenuto sul lato dispositivo o sugli oggetti che risiedono nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="690e6-106">Some WPD applications will take advantage of these extensible menus to support operations on device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="690e6-107">I menu di scelta rapida estendibili sono supportati dalle interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="690e6-107">Extensible context menus are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="690e6-108">Per ulteriori informazioni su una di queste interfacce, vedere la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="690e6-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="690e6-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="690e6-109">Interface</span></span>           | <span data-ttu-id="690e6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="690e6-110">Description</span></span>                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="690e6-111">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="690e6-111">IContextMenu</span></span>        | <span data-ttu-id="690e6-112">La shell di Windows Vista chiama i metodi in questa interfaccia per creare o unire il nuovo menu di scelta rapida con l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="690e6-112">The Windows Vista Shell calls the methods in this interface to create or merge the new context menu with the given object.</span></span> |
| <span data-ttu-id="690e6-113">IDataObject</span><span class="sxs-lookup"><span data-stu-id="690e6-113">IDataObject</span></span>         | <span data-ttu-id="690e6-114">Utilizzato per passare la matrice PIDL del menu di scelta rapida al gestore del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="690e6-114">Used to pass the context menu's PIDL array to the context menu handler.</span></span>                                                    |
| <span data-ttu-id="690e6-115">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="690e6-115">IPropertySetStorage</span></span> | <span data-ttu-id="690e6-116">Questa interfaccia viene utilizzata per recuperare le proprietà WPD per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="690e6-116">This interface is used to retrieve WPD properties for the given object.</span></span>                                                    |
| <span data-ttu-id="690e6-117">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="690e6-117">IPropertyStorage</span></span>    | <span data-ttu-id="690e6-118">Questa interfaccia viene utilizzata anche per recuperare le proprietà WPD per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="690e6-118">This interface is also used to retrieve WPD properties for the given object.</span></span>                                               |
| <span data-ttu-id="690e6-119">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="690e6-119">IShellExtInit</span></span>       | <span data-ttu-id="690e6-120">Inizializza le estensioni della shell di Windows Vista per il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="690e6-120">Initializes the Windows Vista Shell extensions for the context menu.</span></span>                                                       |
| <span data-ttu-id="690e6-121">IStream</span><span class="sxs-lookup"><span data-stu-id="690e6-121">IStream</span></span>             | <span data-ttu-id="690e6-122">Da fornire.</span><span class="sxs-lookup"><span data-stu-id="690e6-122">To be supplied.</span></span>                                                                                                            |



 

<span data-ttu-id="690e6-123">I menu di scelta rapida per WPD vengono implementati come qualsiasi altro menu di scelta rapida in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="690e6-123">Context menus for WPD are implemented like any other context menu in Windows Vista.</span></span> <span data-ttu-id="690e6-124">Se è già stato implementato un gestore di menu di scelta rapida, è possibile modificare il codice esistente in modo che supporti il contenuto lato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="690e6-124">If you've already implemented a context menu handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="690e6-125">Se non è mai stato creato un gestore di menu di scelta rapida, vedere l'argomento Creazione di gestori di menu di scelta rapida nella Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="690e6-125">If you have never created a context menu handler, see the Creating Context Menu Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="690e6-126">I due punti in cui il gestore del menu di scelta rapida WPD differisce da qualsiasi altro gestore si trova nella registrazione del gestore e il supporto del contenuto sul lato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="690e6-126">The two points at which a WPD context menu handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 




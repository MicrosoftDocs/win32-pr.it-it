---
description: Implementazione delle estensioni della finestra delle proprietà
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementazione delle estensioni della finestra delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319088"
---
# <a name="implementing-property-sheet-extensions"></a><span data-ttu-id="8d52c-103">Implementazione delle estensioni della finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8d52c-103">Implementing Property Sheet Extensions</span></span>

<span data-ttu-id="8d52c-104">L'estensione dello spazio dei nomi WPD supporta le finestre delle proprietà estendibili.</span><span class="sxs-lookup"><span data-stu-id="8d52c-104">The WPD Namespace Extension supports extensible property sheets.</span></span> <span data-ttu-id="8d52c-105">Si tratta delle finestre di dialogo delle proprietà visualizzate quando un utente fa clic con il pulsante destro del mouse su un oggetto, ad esempio un file o una cartella, e seleziona **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="8d52c-105">These are the property dialogs that appear when a user right-clicks on an object, such as a file or a folder, and selects **Properties**.</span></span> <span data-ttu-id="8d52c-106">Alcune applicazioni WPD sfruttano i vantaggi di queste finestre delle proprietà estendibili per visualizzare le proprietà del contenuto sul lato dispositivo o gli oggetti che risiedono nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d52c-106">Some WPD applications will take advantage of these extensible property sheets to display properties for device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="8d52c-107">Le finestre delle proprietà estendibili sono supportate dalle interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8d52c-107">Extensible property sheets are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="8d52c-108">Per ulteriori informazioni su una di queste interfacce, vedere la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d52c-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="8d52c-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="8d52c-109">Interface</span></span>           | <span data-ttu-id="8d52c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d52c-110">Description</span></span>                                                                  |
|---------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8d52c-111">IDataObject</span><span class="sxs-lookup"><span data-stu-id="8d52c-111">IDataObject</span></span>         | <span data-ttu-id="8d52c-112">Utilizzato per passare la matrice PIDL del menu di scelta rapida al gestore del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8d52c-112">Used to pass the context menu's PIDL array to the context menu handler.</span></span>      |
| <span data-ttu-id="8d52c-113">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="8d52c-113">IPropertySetStorage</span></span> | <span data-ttu-id="8d52c-114">Questa interfaccia viene utilizzata per recuperare le proprietà WPD per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="8d52c-114">This interface is used to retrieve WPD properties for the given object.</span></span>      |
| <span data-ttu-id="8d52c-115">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="8d52c-115">IPropertyStorage</span></span>    | <span data-ttu-id="8d52c-116">Questa interfaccia viene utilizzata anche per recuperare le proprietà WPD per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="8d52c-116">This interface is also used to retrieve WPD properties for the given object.</span></span> |
| <span data-ttu-id="8d52c-117">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="8d52c-117">IShellExtInit</span></span>       | <span data-ttu-id="8d52c-118">Inizializza le estensioni della shell di Windows Vista per il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8d52c-118">Initializes the Windows Vista Shell extensions for the context menu.</span></span>         |
| <span data-ttu-id="8d52c-119">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="8d52c-119">IShellPropSheetExt</span></span>  | <span data-ttu-id="8d52c-120">Supporta l'aggiunta di estensioni della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d52c-120">Supports addition of property sheet extensions.</span></span>                              |



 

<span data-ttu-id="8d52c-121">Le finestre delle proprietà per WPD vengono implementate come qualsiasi altra finestra delle proprietà in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8d52c-121">Property sheets for WPD are implemented like any other property sheet in Windows Vista.</span></span> <span data-ttu-id="8d52c-122">Se è già stato implementato un gestore della finestra delle proprietà, è possibile modificare il codice esistente in modo che supporti il contenuto lato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d52c-122">If you've already implemented a property sheet handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="8d52c-123">Se non è mai stato creato un gestore di menu di scelta rapida, vedere l'argomento Creazione di gestori della finestra delle proprietà nell'Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d52c-123">If you've never created a context menu handler, see the Creating Property Sheet Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="8d52c-124">I due punti in cui un gestore della finestra delle proprietà di WPD è diverso da qualsiasi altro gestore si trova nella registrazione del gestore e il supporto del contenuto sul lato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d52c-124">The two points at which a WPD property sheet handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 




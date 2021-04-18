---
title: Considerazioni sulla programmazione (Utilità di pianificazione)
description: Quando si sviluppano applicazioni che usano la Utilità di pianificazione 1,0, tenere presenti i seguenti problemi di programmazione. L'applicazione deve verificare che il servizio Utilità di pianificazione sia in esecuzione prima di eseguire qualsiasi chiamata usando l'API Utilità di pianificazione. Quando si recuperano le stringhe, assicurarsi di chiamare CoTaskMemFree per rilasciare ogni stringa dopo che non è più necessaria. Quando si recuperano matrici di stringhe, assicurarsi prima di tutto di rilasciare ogni stringa nella matrice e quindi rilasciare la matrice stessa. Quando si crea o si modifica un elemento di lavoro, inclusi i trigger associati a un elemento di lavoro, assicurarsi di chiamare IPersistFile Save per salvare l'elemento di lavoro su disco. Dopo aver usato le interfacce fornite dall'API Utilità di pianificazione, assicurarsi di chiamare la versione IUnknown per rilasciare l'interfaccia. IUnknown è supportato da ogni oggetto Utilità di pianificazione.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- avvio Utilità di pianificazione
- Considerazioni sulla programmazione Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300754"
---
# <a name="programming-considerations-task-scheduler"></a><span data-ttu-id="dde4f-107">Considerazioni sulla programmazione (Utilità di pianificazione)</span><span class="sxs-lookup"><span data-stu-id="dde4f-107">Programming Considerations (Task Scheduler)</span></span>

<span data-ttu-id="dde4f-108">Quando si sviluppano applicazioni che usano la Utilità di pianificazione 1,0, tenere presenti i seguenti problemi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="dde4f-108">When developing applications that use the Task Scheduler 1.0, keep the following programming issues in mind.</span></span>

-   <span data-ttu-id="dde4f-109">L'applicazione deve verificare che il servizio Utilità di pianificazione sia in esecuzione prima di eseguire qualsiasi chiamata usando l'API Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="dde4f-109">Your application must ensure the Task Scheduler service is running before attempting to make any calls using the Task Scheduler API.</span></span>
-   <span data-ttu-id="dde4f-110">Quando si recuperano le stringhe, assicurarsi di chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare ogni stringa dopo che non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="dde4f-110">When retrieving strings, make sure that you call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release each string after it is no longer needed.</span></span> <span data-ttu-id="dde4f-111">Quando si recuperano matrici di stringhe, assicurarsi prima di tutto di rilasciare ogni stringa nella matrice e quindi rilasciare la matrice stessa.</span><span class="sxs-lookup"><span data-stu-id="dde4f-111">When retrieving arrays of strings, make sure you first release each string in the array and then release the array itself.</span></span>
-   <span data-ttu-id="dde4f-112">Quando si crea o si modifica un elemento di lavoro, inclusi i trigger associati a un elemento di lavoro, assicurarsi di chiamare [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare l'elemento di lavoro su disco.</span><span class="sxs-lookup"><span data-stu-id="dde4f-112">When creating or modifying a work item, including triggers associated with a work item, make sure you call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the work item to disk.</span></span>
-   <span data-ttu-id="dde4f-113">Dopo aver usato le interfacce fornite dall'API di Utilità di pianificazione, assicurarsi di chiamare [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="dde4f-113">After using any of the interfaces that are provided by the Task Scheduler API, make sure you call [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the interface.</span></span> <span data-ttu-id="dde4f-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) è supportato da ogni oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="dde4f-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is supported by each Task Scheduler object.</span></span>

<span data-ttu-id="dde4f-115">Nella sezione using della documentazione Utilità di pianificazione sono disponibili numerosi esempi che seguono queste linee guida.</span><span class="sxs-lookup"><span data-stu-id="dde4f-115">The Using section of the Task Scheduler documentation provides numerous examples that follow these guidelines.</span></span> <span data-ttu-id="dde4f-116">Nella tabella seguente vengono forniti alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="dde4f-116">The table below provides jumps to some of these examples.</span></span>

| <span data-ttu-id="dde4f-117">Per un esempio di</span><span class="sxs-lookup"><span data-stu-id="dde4f-117">For an example of</span></span>         | <span data-ttu-id="dde4f-118">Vedere</span><span class="sxs-lookup"><span data-stu-id="dde4f-118">See</span></span>                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde4f-119">Rilascio di stringhe</span><span class="sxs-lookup"><span data-stu-id="dde4f-119">Releasing strings</span></span>         | [<span data-ttu-id="dde4f-120">Recupero degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="dde4f-120">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="dde4f-121">Salvataggio degli elementi di lavoro su disco</span><span class="sxs-lookup"><span data-stu-id="dde4f-121">Saving work items to disk</span></span> | [<span data-ttu-id="dde4f-122">Impostazione degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="dde4f-122">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |
| <span data-ttu-id="dde4f-123">Rilascio di interfacce</span><span class="sxs-lookup"><span data-stu-id="dde4f-123">Releasing interfaces</span></span>      | [<span data-ttu-id="dde4f-124">Esempio di creazione di un'attività con NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="dde4f-124">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |



 

 

 

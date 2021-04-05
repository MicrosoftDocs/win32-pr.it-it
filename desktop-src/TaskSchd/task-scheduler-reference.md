---
title: Riferimento Utilità di pianificazione
description: In questa sezione vengono descritte le API, gli oggetti di scripting e XML Schema forniti dall'Utilità di pianificazione.
ms.assetid: e3b5a1e1-4d18-44b7-aaa6-ebec11892bec
keywords:
- Utilità di pianificazione Utilità di pianificazione, riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb22306266054b8ec19a90f188c43e5eb7e4393b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710558"
---
# <a name="task-scheduler-reference"></a><span data-ttu-id="7f584-104">Riferimento Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7f584-104">Task Scheduler Reference</span></span>

<span data-ttu-id="7f584-105">In questa sezione vengono descritte le API, gli oggetti di scripting e XML Schema forniti dall'Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7f584-105">This section describes the APIs, scripting objects, and XML schema that are provided by the Task Scheduler.</span></span>

<span data-ttu-id="7f584-106">Gli argomenti dell'API includono una descrizione dell'API, la sintassi di dichiarazione dell'API, osservazioni che descrivono condizioni speciali per l'API e un blocco di requisiti che descrive la piattaforma, i file di intestazione e le librerie necessarie.</span><span class="sxs-lookup"><span data-stu-id="7f584-106">API topics include a description of the API, the declaration syntax of the API, remarks that describe special conditions for the API, and a requirements block that describes what platform, header files, and libraries are required.</span></span>

<span data-ttu-id="7f584-107">Gli argomenti degli oggetti di scripting includono una descrizione dell'oggetto, la sintassi di dichiarazione dell'oggetto, le osservazioni che descrivono condizioni speciali per l'oggetto e un blocco di requisiti che descrive le librerie di piattaforma e di tipi richieste.</span><span class="sxs-lookup"><span data-stu-id="7f584-107">Scripting object topics include a description of the object, the declaration syntax of the object, remarks that describe special conditions for the object, and a requirements block that describes what platform and type libraries are required.</span></span>

<span data-ttu-id="7f584-108">XML Schema argomenti includono una descrizione delle informazioni sugli elementi, i padri, i figli e gli attributi e le osservazioni che descrivono condizioni speciali.</span><span class="sxs-lookup"><span data-stu-id="7f584-108">XML schema topics include a description of the element, parent, child, and attribute information, and remarks that describe special conditions.</span></span>



| <span data-ttu-id="7f584-109">Vedere</span><span class="sxs-lookup"><span data-stu-id="7f584-109">See</span></span>                                                                                          | <span data-ttu-id="7f584-110">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="7f584-110">For information on</span></span>                                                                                                                            |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f584-111">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7f584-111">Task Scheduler Objects</span></span>](task-scheduler-objects.md)                                         | <span data-ttu-id="7f584-112">Scripting di oggetti e relativi metodi e proprietà.</span><span class="sxs-lookup"><span data-stu-id="7f584-112">Scripting objects and their methods and properties.</span></span>                                                                                           |
| [<span data-ttu-id="7f584-113">Interfacce di Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7f584-113">Task Scheduler Interfaces</span></span>](task-scheduler-interfaces.md)                                   | <span data-ttu-id="7f584-114">Interfacce e relativi metodi e proprietà.</span><span class="sxs-lookup"><span data-stu-id="7f584-114">Interfaces and their methods and properties.</span></span>                                                                                                  |
| [<span data-ttu-id="7f584-115">Strutture e unioni Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7f584-115">Task Scheduler Structures and Unions</span></span>](task-scheduler-structures-and-unions.md)             | <span data-ttu-id="7f584-116">Strutture e unioni.</span><span class="sxs-lookup"><span data-stu-id="7f584-116">Structures and unions.</span></span>                                                                                                                        |
| [<span data-ttu-id="7f584-117">Utilità di pianificazione tipi enumerati</span><span class="sxs-lookup"><span data-stu-id="7f584-117">Task Scheduler Enumerated Types</span></span>](task-scheduler-enumerated-types.md)                       | <span data-ttu-id="7f584-118">Costanti definite dagli enumeratori.</span><span class="sxs-lookup"><span data-stu-id="7f584-118">Constants defined by enumerators.</span></span>                                                                                                             |
| [<span data-ttu-id="7f584-119">Schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7f584-119">Task Scheduler Schema</span></span>](task-scheduler-schema.md)                                           | <span data-ttu-id="7f584-120">Elementi, tipi semplici, tipi complessi e gruppi di attributi definiti dallo schema.</span><span class="sxs-lookup"><span data-stu-id="7f584-120">Elements, simple types, complex types, and attribute groups defined by the schema.</span></span>                                                            |
| [<span data-ttu-id="7f584-121">Utilità di pianificazione le costanti Error e Success</span><span class="sxs-lookup"><span data-stu-id="7f584-121">Task Scheduler Error and Success Constants</span></span>](task-scheduler-error-and-success-constants.md) | <span data-ttu-id="7f584-122">Costanti di errore e di esito positivo restituite dalle API Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7f584-122">Error and success constants returned by Task Scheduler APIs.</span></span>                                                                                  |
| [<span data-ttu-id="7f584-123">**Schtasks.exe**</span><span class="sxs-lookup"><span data-stu-id="7f584-123">**Schtasks.exe**</span></span>](schtasks.md)                                                             | <span data-ttu-id="7f584-124">Lo strumento da riga di comando Schtasks.exe utilizzato per creare, eliminare, eseguire query, modificare, eseguire e terminare attività pianificate in un computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="7f584-124">The Schtasks.exe command line tool that is used to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7f584-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f584-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f584-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7f584-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





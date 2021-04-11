---
description: Gestire la condivisione degli assembly e il controllo delle versioni delle DLL nell'archivio di assembly affiancato dei sistemi dai programmi. Scrivere manifesti di assembly e descrivere in autonomia le applicazioni per la condivisione degli assembly e il reindirizzamento delle dll.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Applicazioni isolate e assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128822"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="4bb01-104">Applicazioni isolate e assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="4bb01-104">Isolated Applications and Side-by-side Assemblies</span></span>

## <a name="purpose"></a><span data-ttu-id="4bb01-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="4bb01-105">Purpose</span></span>

<span data-ttu-id="4bb01-106">Le applicazioni isolate e gli assembly affiancati sono una soluzione Microsoft Windows che consente di ridurre i conflitti di controllo delle versioni nelle applicazioni client Windows.</span><span class="sxs-lookup"><span data-stu-id="4bb01-106">Isolated Applications and Side-by-side Assemblies is a Microsoft Windows solution that reduces versioning conflicts in Windows-client applications.</span></span> <span data-ttu-id="4bb01-107">Con Windows, gli sviluppatori di applicazioni possono compilare applicazioni isolate completamente autodescrittive e non interessate dalle modifiche apportate al registro di sistema, ad altre applicazioni o ad altre versioni di assembly in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4bb01-107">With Windows, application developers can build isolated applications that are fully self-describing and unaffected by changes to the registry, other applications, or other versions of assemblies running on the system.</span></span> <span data-ttu-id="4bb01-108">Gli autori e gli amministratori di applicazioni possono utilizzare i manifesti per gestire la condivisione di assembly affiancati dopo la distribuzione in base a un'applicazione o globale.</span><span class="sxs-lookup"><span data-stu-id="4bb01-108">Application authors and administrators can use manifests to manage the sharing of side-by-side assemblies after deployment on either a global or per-application basis.</span></span> <span data-ttu-id="4bb01-109">I clienti traggono vantaggio da applicazioni isolate più stabili e aggiornate in modo più affidabile.</span><span class="sxs-lookup"><span data-stu-id="4bb01-109">Customers benefit from isolated applications that are more stable and more reliably updated.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="4bb01-110">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="4bb01-110">Where applicable</span></span>

<span data-ttu-id="4bb01-111">Per lo sviluppo di applicazioni che condividono in modo sicuro gli assembly del sistema operativo, è possibile usare applicazioni isolate e condivisione di assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="4bb01-111">Isolated applications and side-by-side assembly sharing can be used to develop applications that safely share operating system assemblies.</span></span> <span data-ttu-id="4bb01-112">Gli sviluppatori possono utilizzare questa tecnologia per correggere i conflitti di controllo delle versioni DLL causati da una versione incompatibile di un assembly condiviso.</span><span class="sxs-lookup"><span data-stu-id="4bb01-112">Developers can use this technology to correct DLL versioning conflicts caused by an incompatible version of a shared assembly.</span></span>

<span data-ttu-id="4bb01-113">Se l'applicazione deve ottenere costantemente la versione di un componente testato, è possibile isolare l'applicazione in modo che venga sempre eseguita con la versione testata del componente nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4bb01-113">If your application must consistently get the version of a component you have tested, it is possible to isolate your application so that it will always be run with the tested version of the component on the user's computer.</span></span>

<span data-ttu-id="4bb01-114">Le applicazioni isolate e gli assembly affiancati sono progettati per lo sviluppo di applicazioni di tipo desktop.</span><span class="sxs-lookup"><span data-stu-id="4bb01-114">Isolated Applications and Side-by-side Assemblies is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4bb01-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="4bb01-115">Developer audience</span></span>

<span data-ttu-id="4bb01-116">Questa documentazione è destinata principalmente a sviluppatori di software, sviluppatori di applicazioni e amministratori di rete:</span><span class="sxs-lookup"><span data-stu-id="4bb01-116">This documentation is primarily intended for software developers, application developers, and network administrators:</span></span>

-   <span data-ttu-id="4bb01-117">Sviluppatori di software che desiderano creare applicazioni isolate che utilizzeranno gli assembly affiancati resi disponibili da Microsoft e altri autori di assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="4bb01-117">Software developers who want to create isolated applications that will use the side-by-side assemblies made available by Microsoft and other side-by-side assembly publishers.</span></span>
-   <span data-ttu-id="4bb01-118">Sviluppatori di applicazioni interessati alla creazione di assembly affiancati per isolare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4bb01-118">Application developers who are interested in creating their own side-by-side assemblies to isolate their applications.</span></span>
-   <span data-ttu-id="4bb01-119">Amministratori di rete che desiderano ulteriori informazioni sulle applicazioni isolate.</span><span class="sxs-lookup"><span data-stu-id="4bb01-119">Network administrators who want more information about isolated applications.</span></span>

<span data-ttu-id="4bb01-120">Come riferimento principale per la condivisione di assembly affiancati e le applicazioni isolate, in questa documentazione vengono fornite informazioni generali sulla creazione di manifesti e assembly affiancati, sull'installazione di applicazioni isolate e assembly affiancati e sull'utilizzo dell'API del contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="4bb01-120">As the primary reference for side-by-side assembly sharing and isolated applications, this documentation provides general background information about authoring manifests and side-by-side assemblies, installing isolated applications and side-by-side assemblies, and using the Activation Context API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4bb01-121">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="4bb01-121">Run-time requirements</span></span>

<span data-ttu-id="4bb01-122">Windows Server 2003 e versioni successive o Windows XP e versioni successive sono necessari per usare gli assembly affiancati e i manifesti per isolare le applicazioni e usare l'API del contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="4bb01-122">Windows Server 2003 and later or Windows XP and later is required to use side-by-side assemblies and manifests to isolate applications and to use the Activation Context API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4bb01-123">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4bb01-123">In this section</span></span>



| <span data-ttu-id="4bb01-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="4bb01-124">Topic</span></span>                                                         | <span data-ttu-id="4bb01-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bb01-125">Description</span></span>                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="4bb01-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4bb01-126">Reference</span></span>](side-by-side-assemblies-reference.md)<br/> | <span data-ttu-id="4bb01-127">Documentazione delle applicazioni isolate e degli assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="4bb01-127">Documentation of Isolated Applications and Side-by-side Assemblies.</span></span><br/> |



 

 

 





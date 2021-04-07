---
title: Uso di Active Directory interfacce del servizio
description: Active Directory Service Interfaces (ADSI) fornisce i mezzi per le applicazioni client dei servizi directory per l'utilizzo di un set di interfacce per comunicare con qualsiasi spazio dei nomi che fornisce un'implementazione ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Uso di ADSI Active Directory interfacce di servizio
- ADSI ADSI, utilizzo
- Interfacce di servizio Active Directory ADSI, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855234"
---
# <a name="using-active-directory-service-interfaces"></a><span data-ttu-id="8bbbb-106">Uso di Active Directory interfacce del servizio</span><span class="sxs-lookup"><span data-stu-id="8bbbb-106">Using Active Directory Service Interfaces</span></span>

<span data-ttu-id="8bbbb-107">Active Directory Service Interfaces (ADSI) fornisce i mezzi per le applicazioni client dei servizi directory per l'utilizzo di un set di interfacce per comunicare con qualsiasi spazio dei nomi che fornisce un'implementazione ADSI.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-107">Active Directory Service Interfaces (ADSI) provides the means for client applications of directory services to use one set of interfaces to communicate with any namespace that provides an ADSI implementation.</span></span> <span data-ttu-id="8bbbb-108">I client ADSI utilizzano le interfacce del servizio Active Directory ben definite al posto delle chiamate API specifiche della rete per ottenere un accesso più semplice ai servizi per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-108">ADSI clients use the well-defined Active Directory Service Interfaces in place of the network-specific API calls to gain simpler access to the services for a namespace.</span></span>

<span data-ttu-id="8bbbb-109">Active Directory le interfacce del servizio sono conformi al Component Object Model (COM) e supportano le funzionalità COM standard.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-109">Active Directory Service Interfaces conform to the Component Object Model (COM) and support standard COM features.</span></span>

<span data-ttu-id="8bbbb-110">ADSI fornisce le interfacce conformi all'automazione per i controller associati al nome, ad esempio Java, Microsoft Visual Basic Development System e Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="8bbbb-110">ADSI supplies interfaces that are compliant with Automation for name-bound controllers like Java, Microsoft Visual Basic development system, and Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="8bbbb-111">ADSI può inoltre fornire un'interfaccia in grado di ottimizzare le prestazioni per le interfacce non conformi all'automazione, da utilizzare con ambienti di linguaggio come C e C++.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-111">ADSI can also provide an interface that can optimize performance for interfaces that are not compliant with Automation, to use with language environments like C and C++.</span></span>

<span data-ttu-id="8bbbb-112">ADSI fornisce anche le interfacce non di automazione, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), per supportare la gestione e le query degli oggetti directory.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-112">ADSI also provides the non-automation interfaces, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), to support directory object management and queries.</span></span>

<span data-ttu-id="8bbbb-113">Inoltre, ADSI fornisce il proprio provider di OLE DB, in modo che tutti i client che usano già OLE DB, inclusi quelli che usano ActiveX Data Objects, possano eseguire query direttamente nei servizi directory.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-113">In addition, ADSI supplies its own OLE DB provider, so that any client already using OLE DB, including those using ActiveX Data Objects, can query directory services directly.</span></span>

<span data-ttu-id="8bbbb-114">Anche le applicazioni Web che utilizzano Active Server pagine possono programmare l'accesso ai servizi directory tramite ADSI.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-114">Web applications using Active Server Pages also can program access to directory services through ADSI.</span></span>

<span data-ttu-id="8bbbb-115">I client ADSI possono individuare a livello di programmazione tutti i provider ADSI in un sito e utilizzare le stesse interfacce per comunicare con ogni spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-115">ADSI clients can programmatically discover all the ADSI providers at a site and use the same interfaces to communicate with each namespace.</span></span> <span data-ttu-id="8bbbb-116">Quando vengono installati provider aggiuntivi, i client ADSI possono comunicare, senza ricompilare, anche con i nuovi spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-116">As additional providers are installed, the ADSI clients can communicate, without recompiling, with the new namespaces as well.</span></span>

<span data-ttu-id="8bbbb-117">In questa guida di programmazione viene descritto il funzionamento di ADSI e vengono fornite informazioni per l'esecuzione di attività specifiche in ADSI.</span><span class="sxs-lookup"><span data-stu-id="8bbbb-117">This programming guide describes how ADSI works and provides information for performing specific tasks in ADSI.</span></span> <span data-ttu-id="8bbbb-118">Vengono trattati i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="8bbbb-118">The following topics are discussed:</span></span>

-   [<span data-ttu-id="8bbbb-119">Associazione a un oggetto ADSI</span><span class="sxs-lookup"><span data-stu-id="8bbbb-119">Binding to an ADSI Object</span></span>](binding-to-an-adsi-object.md)
-   [<span data-ttu-id="8bbbb-120">Creazione ed eliminazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="8bbbb-120">Creating and Deleting Objects</span></span>](creating-and-deleting-objects.md)
-   [<span data-ttu-id="8bbbb-121">Accesso e manipolazione di dati con ADSI</span><span class="sxs-lookup"><span data-stu-id="8bbbb-121">Accessing and Manipulating Data with ADSI</span></span>](accessing-and-manipulating-data-with-adsi.md)
-   [<span data-ttu-id="8bbbb-122">Utilizzo dello schema ADSI</span><span class="sxs-lookup"><span data-stu-id="8bbbb-122">Using the ADSI Schema</span></span>](using-the-adsi-schema.md)
-   [<span data-ttu-id="8bbbb-123">Raccolte e gruppi</span><span class="sxs-lookup"><span data-stu-id="8bbbb-123">Collections and Groups</span></span>](collections-and-groups.md)
-   [<span data-ttu-id="8bbbb-124">Enumerazione di oggetti ADSI</span><span class="sxs-lookup"><span data-stu-id="8bbbb-124">Enumerating ADSI Objects</span></span>](enumerating-adsi-objects.md)
-   [<span data-ttu-id="8bbbb-125">Ricerca di Active Directory</span><span class="sxs-lookup"><span data-stu-id="8bbbb-125">Searching Active Directory</span></span>](searching-active-directory.md)
-   [<span data-ttu-id="8bbbb-126">Modello di sicurezza ADSI</span><span class="sxs-lookup"><span data-stu-id="8bbbb-126">ADSI Security Model</span></span>](adsi-security-model.md)
-   [<span data-ttu-id="8bbbb-127">Estensioni ADSI</span><span class="sxs-lookup"><span data-stu-id="8bbbb-127">ADSI Extensions</span></span>](adsi-extensions.md)
-   [<span data-ttu-id="8bbbb-128">Uso di ADSI con Exchange</span><span class="sxs-lookup"><span data-stu-id="8bbbb-128">Using ADSI with Exchange</span></span>](using-adsi-with-exchange.md)
-   [<span data-ttu-id="8bbbb-129">Interfacce di utilità ADSI</span><span class="sxs-lookup"><span data-stu-id="8bbbb-129">ADSI Utility Interfaces</span></span>](adsi-utility-interfaces.md)
-   [<span data-ttu-id="8bbbb-130">Programmazione di ADSI con Java/COM</span><span class="sxs-lookup"><span data-stu-id="8bbbb-130">Programming ADSI with Java/COM</span></span>](programming-adsi-with-javacom.md)

 

 





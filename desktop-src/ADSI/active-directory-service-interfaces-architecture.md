---
title: Architettura delle interfacce del servizio Active Directory
description: Molti servizi directory sono gerarchici e quindi si prestano a un modello a oggetti gerarchico. In questa sezione vengono utilizzate le rappresentazioni di oggetti COM per illustrare diverse funzionalità ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory architettura di interfacce di servizio ADSI
- ADSI ADSI, informazioni su, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707495"
---
# <a name="active-directory-service-interfaces-architecture"></a><span data-ttu-id="a4ea2-106">Architettura delle interfacce del servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="a4ea2-106">Active Directory Service Interfaces Architecture</span></span>

<span data-ttu-id="a4ea2-107">Molti servizi directory sono gerarchici e quindi si prestano a un modello a oggetti gerarchico.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-107">Many directory services are hierarchical and thus lend themselves to a hierarchical object model.</span></span> <span data-ttu-id="a4ea2-108">In questa sezione vengono utilizzate le rappresentazioni di oggetti COM per illustrare diverse funzionalità ADSI.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-108">This section uses COM object representations to illustrate various ADSI features.</span></span>

<span data-ttu-id="a4ea2-109">Nella figura seguente del modello a oggetti, un oggetto di sistema di primo livello contiene un oggetto spazio dei nomi per ogni provider ADSI installato.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-109">In the following object model figure, a top-level system object contains one Namespace object for every installed ADSI provider.</span></span>

![oggetto contenitore spazi dei nomi](images/ds2top.png)

<span data-ttu-id="a4ea2-111">Ogni oggetto spazio dei nomi è a sua volta un contenitore che contiene i nodi radice di primo livello di ogni server, dominio o qualsiasi altro tipo di oggetti di sistema di directory definito come radice in ogni servizio directory.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-111">Each of the Namespace objects is itself a container that contains the top-level root nodes of every server, domain, or whatever other kinds of directory-system objects are defined as roots in each directory service.</span></span>

<span data-ttu-id="a4ea2-112">ADSI fornisce un set di oggetti e interfacce predefiniti che consentono alle applicazioni client di interagire con i servizi di directory utilizzando un set uniforme di metodi.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-112">ADSI supplies a set of predefined objects and interfaces so that client applications can interact with directory services using a uniform set of methods.</span></span> <span data-ttu-id="a4ea2-113">Tuttavia, ADSI potrebbe non consentire l'accesso a tutte le funzionalità di un servizio directory.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-113">However, ADSI may not provide access to all features of a directory service.</span></span> <span data-ttu-id="a4ea2-114">Per utilizzare al meglio il set completo di funzionalità di ogni servizio directory, ADSI fornisce un modello di schema che i provider di servizi di directory e i fornitori di software di terze parti possono utilizzare per estendere le funzionalità oltre le interfacce fornite in ADSI.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-114">To better use the full feature set of each directory service, ADSI supplies a schema model that directory service providers and third-party software vendors can use to extend features beyond the interfaces provided in ADSI.</span></span>

<span data-ttu-id="a4ea2-115">Gli oggetti contenitore del nodo radice, disponibili all'interno di ogni oggetto spazio dei nomi del provider, includono un oggetto contenitore dello schema ADSI.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-115">The root-node container objects, found within each provider Namespace object, include an ADSI schema container object.</span></span> <span data-ttu-id="a4ea2-116">Questo oggetto contiene la definizione di tutte le funzionalità per quel provider.</span><span class="sxs-lookup"><span data-stu-id="a4ea2-116">This object contains the definition of all features for that provider.</span></span> <span data-ttu-id="a4ea2-117">Per altre informazioni, vedere [modello di schema ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="a4ea2-117">For more information, see [ADSI Schema Model](adsi-schema-model.md).</span></span>

<span data-ttu-id="a4ea2-118">Questa sezione include gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4ea2-118">This section includes the following topics:</span></span>

-   [<span data-ttu-id="a4ea2-119">Oggetti interfacce del servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="a4ea2-119">Active Directory Service Interfaces Objects</span></span>](active-directory-service-interfaces-objects.md)
-   <span data-ttu-id="a4ea2-120">[Namespaces](namespaces.md) (Spazi dei nomi)</span><span class="sxs-lookup"><span data-stu-id="a4ea2-120">[Namespaces](namespaces.md)</span></span>
-   [<span data-ttu-id="a4ea2-121">Provider di interfacce del servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="a4ea2-121">Active Directory Service Interfaces Provider</span></span>](active-directory-service-interfaces-provider.md)
-   [<span data-ttu-id="a4ea2-122">Modello di schema ADSI</span><span class="sxs-lookup"><span data-stu-id="a4ea2-122">ADSI Schema Model</span></span>](adsi-schema-model.md)

 

 





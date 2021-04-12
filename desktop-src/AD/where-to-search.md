---
title: Scelta della posizione in cui eseguire la ricerca
description: In questo argomento vengono illustrate le diverse ricerche che possono essere eseguite in Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Decidere dove eseguire la ricerca in Active Directory
- Active Directory AD, ricerca, scelta della posizione in cui eseguire la ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336758"
---
# <a name="deciding-where-to-search"></a><span data-ttu-id="11011-105">Scelta della posizione in cui eseguire la ricerca</span><span class="sxs-lookup"><span data-stu-id="11011-105">Deciding Where to Search</span></span>

<span data-ttu-id="11011-106">In questo argomento vengono illustrate le diverse ricerche che possono essere eseguite in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="11011-106">This topic explains the different searches that can be performed in Active Directory Domain Services.</span></span>

<span data-ttu-id="11011-107">Tutte le ricerche vengono eseguite in uno dei seguenti contesti di denominazione:</span><span class="sxs-lookup"><span data-stu-id="11011-107">All searches are performed in one of the following naming contexts:</span></span>

-   <span data-ttu-id="11011-108">Dominio, incluse le partizioni di directory applicative</span><span class="sxs-lookup"><span data-stu-id="11011-108">Domain, including application directory partitions</span></span>
-   <span data-ttu-id="11011-109">Contenitore dello schema</span><span class="sxs-lookup"><span data-stu-id="11011-109">Schema container</span></span>
-   <span data-ttu-id="11011-110">Contenitore di configurazione</span><span class="sxs-lookup"><span data-stu-id="11011-110">Configuration container</span></span>
-   <span data-ttu-id="11011-111">Catalogo globale</span><span class="sxs-lookup"><span data-stu-id="11011-111">Global catalog</span></span>

## <a name="searching-a-domain"></a><span data-ttu-id="11011-112">Ricerca in un dominio</span><span class="sxs-lookup"><span data-stu-id="11011-112">Searching a Domain</span></span>

<span data-ttu-id="11011-113">I domini contengono la maggior parte degli oggetti altamente usati, ad esempio utenti, contatti, gruppi, unità organizzative, computer e così via.</span><span class="sxs-lookup"><span data-stu-id="11011-113">Domains contain most of the highly used objects such as users, contacts, groups, organizational units, computers, and so on.</span></span> <span data-ttu-id="11011-114">La maggior parte delle query cercherà un dominio.</span><span class="sxs-lookup"><span data-stu-id="11011-114">Most queries will search a domain.</span></span> <span data-ttu-id="11011-115">Per ulteriori informazioni sulla ricerca di un dominio, vedere [ricerca di contenuto del dominio](searching-domain-contents.md).</span><span class="sxs-lookup"><span data-stu-id="11011-115">For more information about searching a domain, see [Searching Domain Contents](searching-domain-contents.md).</span></span>

## <a name="searching-the-schema-container"></a><span data-ttu-id="11011-116">Ricerca nel contenitore dello schema</span><span class="sxs-lookup"><span data-stu-id="11011-116">Searching the Schema Container</span></span>

<span data-ttu-id="11011-117">Il contenitore dello schema contiene gli oggetti [**classSchema**](/windows/desktop/ADSchema/c-classschema) e [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) che forniscono la definizione formale di ogni classe e attributo che può esistere in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="11011-117">The schema container contains the [**classSchema**](/windows/desktop/ADSchema/c-classschema) and [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects that provide the formal definition of every class and attribute that can exist in Active Directory Domain Services.</span></span> <span data-ttu-id="11011-118">Per cercare gli oggetti nel contenitore dello schema, associare il contenitore dello schema in qualsiasi controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="11011-118">To search for objects in the schema container, bind to the schema container on any domain controller.</span></span> <span data-ttu-id="11011-119">Il contenitore dello schema è disponibile in tutti i controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="11011-119">The schema container is available on all domain controllers.</span></span> <span data-ttu-id="11011-120">Il nome distinto del contenitore dello schema viene ottenuto dall'attributo **schemaNamingContext** di RootDSE.</span><span class="sxs-lookup"><span data-stu-id="11011-120">The distinguished name of the schema container is obtained from the **schemaNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="11011-121">Per ulteriori informazioni su rootDSE e sull'attributo **schemaNamingContext** , vedere [binding senza server e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="11011-121">For more information about rootDSE and the **schemaNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="11011-122">Per ulteriori informazioni sulla lettura dallo schema o dal contenitore dello schema astratto, vedere [linee guida per l'associazione allo schema](guidelines-for-binding-to-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="11011-122">For more information about reading from the schema or abstract schema container, see [Guidelines for Binding to the Schema](guidelines-for-binding-to-the-schema.md).</span></span>

## <a name="searching-the-configuration-container"></a><span data-ttu-id="11011-123">Ricerca nel contenitore di configurazione</span><span class="sxs-lookup"><span data-stu-id="11011-123">Searching the Configuration Container</span></span>

<span data-ttu-id="11011-124">Il contenitore di configurazione contiene informazioni di configurazione, ad esempio siti, servizi e identificatori di visualizzazione, per l'intera foresta.</span><span class="sxs-lookup"><span data-stu-id="11011-124">The configuration container contains configuration information, such as sites, services and display specifiers, for the entire forest.</span></span> <span data-ttu-id="11011-125">Per cercare gli oggetti nel contenitore di configurazione, eseguire l'associazione al contenitore di configurazione in qualsiasi controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="11011-125">To search for objects in the configuration container, bind to the configuration container on any domain controller.</span></span> <span data-ttu-id="11011-126">Il contenitore di configurazione è disponibile in tutti i controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="11011-126">The configuration container is available on all domain controllers.</span></span> <span data-ttu-id="11011-127">Il nome distinto del contenitore di configurazione è ottenuto dall'attributo **configurationNamingContext** di RootDSE.</span><span class="sxs-lookup"><span data-stu-id="11011-127">The distinguished name of the configuration container is obtained from the **configurationNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="11011-128">Per ulteriori informazioni su rootDSE e sull'attributo **configurationNamingContext** , vedere [binding senza server e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="11011-128">For more information about rootDSE and the **configurationNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

## <a name="searching-the-global-catalog"></a><span data-ttu-id="11011-129">Ricerca nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="11011-129">Searching the Global Catalog</span></span>

<span data-ttu-id="11011-130">Il catalogo globale include una replica di ogni oggetto in Active Directory Domain Services, ma con un numero ridotto di attributi.</span><span class="sxs-lookup"><span data-stu-id="11011-130">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="11011-131">Gli attributi nel catalogo globale sono quelli usati più di frequente nelle operazioni di ricerca, ad esempio il nome e il cognome di un utente, i nomi di accesso e così via.</span><span class="sxs-lookup"><span data-stu-id="11011-131">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="11011-132">Per ulteriori informazioni sulla ricerca nel catalogo globale, vedere la pagina relativa alla [ricerca nel catalogo globale](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="11011-132">For more information about searching the global catalog, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 
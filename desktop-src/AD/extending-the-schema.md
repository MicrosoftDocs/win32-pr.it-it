---
title: Estensione dello schema
description: Lo schema del servizio directory Active Directory definisce gli attributi e le classi utilizzati nel Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo di, schema, estensione dello schema
- ANNUNCIO dello schema, estensione dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299575"
---
# <a name="extending-the-schema"></a><span data-ttu-id="9802c-105">Estensione dello schema</span><span class="sxs-lookup"><span data-stu-id="9802c-105">Extending the Schema</span></span>

<span data-ttu-id="9802c-106">Lo schema del servizio directory Active Directory definisce gli attributi e le classi utilizzati nel Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9802c-106">The Active Directory directory service schema defines the attributes and classes used in Active Directory Domain Services.</span></span> <span data-ttu-id="9802c-107">Lo schema di base incluso nel sistema contiene un set completo di definizioni di classe, ad esempio **User**, **computer** e **OrganizationalUnit**, e le definizioni degli attributi, ad esempio **userPrincipalName**, **telephoneNumber** e **objectSID**.</span><span class="sxs-lookup"><span data-stu-id="9802c-107">The base schema that is included the system contains a rich set of class definitions, such as **user**, **computer**, and **organizationalUnit**, and attribute definitions, such as **userPrincipalName**, **telephoneNumber**, and **objectSid**.</span></span> <span data-ttu-id="9802c-108">Il set di classi e attributi esistente sarà sufficiente per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9802c-108">The existing set of classes and attributes will be sufficient for most applications.</span></span> <span data-ttu-id="9802c-109">Tuttavia, lo schema è estensibile, il che significa che è possibile definire nuove classi e attributi.</span><span class="sxs-lookup"><span data-stu-id="9802c-109">However, the schema is extensible, which means that you can define new classes and attributes.</span></span> <span data-ttu-id="9802c-110">In questa sezione viene illustrato come estendere lo schema di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9802c-110">This section discusses how to extend the Active Directory schema.</span></span>

## <a name="when-to-extend-the-schema"></a><span data-ttu-id="9802c-111">Quando estendere lo schema</span><span class="sxs-lookup"><span data-stu-id="9802c-111">When to Extend the Schema</span></span>

<span data-ttu-id="9802c-112">Se gli attributi e le classi esistenti non rientrano nel tipo di dati che si desidera archiviare, è necessario estendere lo schema.</span><span class="sxs-lookup"><span data-stu-id="9802c-112">If the existing classes and attributes do not fit with the type of data you want to store, you should extend the schema.</span></span> <span data-ttu-id="9802c-113">È importante notare che le aggiunte dello schema sono permanenti; è possibile disabilitare classi e attributi, ma non è possibile rimuoverli dallo schema.</span><span class="sxs-lookup"><span data-stu-id="9802c-113">It is important to note that schema additions are permanent; you can disable classes and attributes, but you can never remove them from the schema.</span></span> <span data-ttu-id="9802c-114">Tenere presente questo aspetto quando si esegue il test del codice.</span><span class="sxs-lookup"><span data-stu-id="9802c-114">Keep this in mind when you are testing code.</span></span>

<span data-ttu-id="9802c-115">Prendere in considerazione anche le dimensioni dei dati che si desidera archiviare.</span><span class="sxs-lookup"><span data-stu-id="9802c-115">Also consider the size of the data that you want to store.</span></span> <span data-ttu-id="9802c-116">Microsoft consiglia che nessun valore di attributo superi 500 kilobyte, inclusa la somma degli attributi multivalore.</span><span class="sxs-lookup"><span data-stu-id="9802c-116">Microsoft recommends that no attribute value exceed 500 kilobytes, including the sum of multivalued attributes.</span></span> <span data-ttu-id="9802c-117">Inoltre, le dimensioni degli oggetti non devono superare 1 megabyte.</span><span class="sxs-lookup"><span data-stu-id="9802c-117">Also, objects should not exceed 1 megabyte in size.</span></span> <span data-ttu-id="9802c-118">Prendere in considerazione anche il numero di istanze dei dati; Se si aggiunge un nuovo attributo alla classe [**utente**](/windows/desktop/ADSchema/c-user) in un sistema con 100.000 utenti, è possibile che venga utilizzato un notevole spazio.</span><span class="sxs-lookup"><span data-stu-id="9802c-118">Consider also the number of instances of the data; if you add a new attribute to the [**User**](/windows/desktop/ADSchema/c-user) class on a system that has 100,000 users, this can use up considerable space.</span></span>

<span data-ttu-id="9802c-119">Gli argomenti di questa sezione includono:</span><span class="sxs-lookup"><span data-stu-id="9802c-119">Topics in this section include:</span></span>

-   <span data-ttu-id="9802c-120">Come eseguire l'associazione al contenitore dello schema e leggere le proprietà delle classi e degli attributi esistenti.</span><span class="sxs-lookup"><span data-stu-id="9802c-120">How to bind to the schema container and read the properties of existing classes and attributes.</span></span>
-   <span data-ttu-id="9802c-121">Come e quando estendere lo schema definendo nuove classi e attributi.</span><span class="sxs-lookup"><span data-stu-id="9802c-121">How and when to extend the schema by defining new attributes and classes.</span></span>
-   <span data-ttu-id="9802c-122">Come installare le estensioni dello schema usando LDIFDE, CSVDE o a livello di codice con ADSI.</span><span class="sxs-lookup"><span data-stu-id="9802c-122">How to install schema extensions using LDIFDE, CSVDE, or programmatically with ADSI.</span></span>

<span data-ttu-id="9802c-123">Per ulteriori informazioni e una panoramica dello schema di Active Directory, incluse informazioni sull'implementazione dello schema, le definizioni delle classi e le definizioni degli attributi, vedere [Active Directory schema](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="9802c-123">For more information and an overview of the Active Directory schema, including information about the schema implementation, class definitions, and attribute definitions, see [Active Directory Schema](active-directory-schema.md).</span></span>

<span data-ttu-id="9802c-124">Per ulteriori informazioni, incluse le pagine di riferimento per le classi di schema predefinite, gli attributi e le sintassi degli attributi, vedere il riferimento allo schema Active Directory nel [riferimento Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9802c-124">For more information, including reference pages for the predefined schema classes, attributes, and attribute syntaxes, see the Active Directory Schema Reference in the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

 

 
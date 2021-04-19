---
title: Quando estendere lo schema
description: Estendere lo schema solo se nessuna classe di oggetti esistente soddisfa i requisiti dell'applicazione. L'estensione dello schema è un'operazione complessa; le modifiche dello schema vengono replicate in ogni controller di dominio della foresta aziendale. Considerare attentamente questo problema.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Quando estendere l'annuncio dello schema
- ANNUNCIO dello schema, quando estenderlo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297713"
---
# <a name="when-to-extend-the-schema"></a><span data-ttu-id="fb603-107">Quando estendere lo schema</span><span class="sxs-lookup"><span data-stu-id="fb603-107">When to Extend the Schema</span></span>

<span data-ttu-id="fb603-108">Estendere lo schema solo se nessuna classe di oggetti esistente soddisfa i requisiti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb603-108">Extend the schema only if no existing object class fulfills the requirements of your application.</span></span> <span data-ttu-id="fb603-109">L'estensione dello schema è un'operazione complessa; le modifiche dello schema vengono replicate in ogni controller di dominio della foresta aziendale.</span><span class="sxs-lookup"><span data-stu-id="fb603-109">Extending the schema is a complex operation; schema changes are replicated to every domain controller in the enterprise forest.</span></span> <span data-ttu-id="fb603-110">Considerare attentamente questo problema.</span><span class="sxs-lookup"><span data-stu-id="fb603-110">Consider this carefully.</span></span>

<span data-ttu-id="fb603-111">Lo schema può essere esteso in tre modi:</span><span class="sxs-lookup"><span data-stu-id="fb603-111">The schema can be extended in three ways:</span></span>

-   <span data-ttu-id="fb603-112">Derivare una nuova sottoclasse da una classe esistente: la sottoclasse dispone di tutti gli attributi della superclasse e di tutti gli attributi specificati.</span><span class="sxs-lookup"><span data-stu-id="fb603-112">Derive a new subclass from an existing class - the subclass has all of the attributes of the superclass and any attributes you specify.</span></span> <span data-ttu-id="fb603-113">Derivare da una classe esistente:</span><span class="sxs-lookup"><span data-stu-id="fb603-113">Derive from an existing class:</span></span>
    -   <span data-ttu-id="fb603-114">Quando la classe esistente richiede attributi aggiuntivi, ma in caso contrario è accettabile.</span><span class="sxs-lookup"><span data-stu-id="fb603-114">When the existing class requires additional attributes, but otherwise is acceptable.</span></span>
    -   <span data-ttu-id="fb603-115">Quando la possibilità di trasformare gli oggetti esistenti della classe in una nuova classe non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="fb603-115">When the ability to transform existing objects of the class into a new class is not required.</span></span> <span data-ttu-id="fb603-116">Non è possibile aggiungere una sottoclasse a un oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="fb603-116">It is not possible to add a subclass to an existing object.</span></span>
    -   <span data-ttu-id="fb603-117">Per utilizzare lo snap-in di gestione directory esistente per gestire gli attributi estesi degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="fb603-117">To use the existing Directory Manager snap-in to manage the extended attributes of the objects.</span></span>
-   <span data-ttu-id="fb603-118">Aggiungere gli attributi a una classe esistente e/o aggiungere oggetti padre per la classe.</span><span class="sxs-lookup"><span data-stu-id="fb603-118">Add attributes to an existing class and/or add parent objects for the class.</span></span> <span data-ttu-id="fb603-119">Quando si aggiungono più attributi, eseguire questa operazione in modo strutturato definendo una classe ausiliaria e aggiungendo tale classe ausiliaria alla classe esistente.</span><span class="sxs-lookup"><span data-stu-id="fb603-119">When adding multiple attributes, perform this operation in a structured manner by defining an auxiliary class and adding that auxiliary class to the existing class.</span></span>
-   <span data-ttu-id="fb603-120">La modifica di una classe esistente è obbligatoria quando un'applicazione richiede la possibilità di estendere gli oggetti esistenti della classe.</span><span class="sxs-lookup"><span data-stu-id="fb603-120">Modification of an existing class is required when an application requires the ability to extend existing objects of the class.</span></span> <span data-ttu-id="fb603-121">Ad esempio, per aggiungere i dati specifici dell'applicazione all'oggetto utente, estendere normalmente l'utente della classe, perché è necessario gestire gli utenti esistenti e non solo gli utenti speciali creati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb603-121">For example, to add application-specific data to the User object, extend the class User normally, because you must handle existing Users and not just special Users created by your application.</span></span>
-   <span data-ttu-id="fb603-122">Creare una nuova classe con gli attributi obbligatori.</span><span class="sxs-lookup"><span data-stu-id="fb603-122">Create a new class with the required attributes.</span></span> <span data-ttu-id="fb603-123">Creare una nuova classe; ovvero una classe derivata da "Top" quando nessuna classe esistente soddisfa i requisiti operativi.</span><span class="sxs-lookup"><span data-stu-id="fb603-123">Create a new class; that is, a class derived from "Top" when no existing class fulfills the operational requirements.</span></span>

<span data-ttu-id="fb603-124">Quando si crea una sottoclasse di una classe esistente, qualsiasi elemento dell'interfaccia utente associato alla classe originale non verrà ereditato dalla sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="fb603-124">When you subclass an existing class, any user interface items associated to the original class will not be inherited by the subclass.</span></span> <span data-ttu-id="fb603-125">Se ad esempio si esegue la sottoclasse di un oggetto utente, le pagine delle proprietà e le voci di menu associate all'utente non vengono ereditate.</span><span class="sxs-lookup"><span data-stu-id="fb603-125">For example, if you subclass a user object, the property pages and menu items associated to user are not inherited.</span></span> <span data-ttu-id="fb603-126">Per questo motivo, è preferibile estendere un oggetto esistente o creare una classe ausiliaria anziché creare una sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="fb603-126">For this reason, it is preferable to extend an existing object or create an auxiliary class rather than create a subclass.</span></span>

<span data-ttu-id="fb603-127">Se si esegue la sottoclasse di una classe esistente o si modifica una classe esistente, sarà necessario estendere strumenti come lo snap-in Active Directory utenti e computer per gestire gli attributi estesi degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="fb603-127">Whether you subclass an existing class or modify an existing class, you will want to extend tools such as the Active Directory Users and Computers snap-in to manage the extended attributes of the objects.</span></span> <span data-ttu-id="fb603-128">Per ulteriori informazioni, vedere [estensione dell'interfaccia utente per gli oggetti directory](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fb603-128">For more information, see [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

 

 





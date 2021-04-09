---
description: Gli archivi, le applicazioni e gli ambiti dei criteri di autorizzazione rappresentano diversi livelli di organizzazione dei criteri di gestione autorizzazioni.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Archivi, applicazioni e ambiti dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879670"
---
# <a name="policy-stores-applications-and-scopes"></a><span data-ttu-id="9662b-103">Archivi, applicazioni e ambiti dei criteri</span><span class="sxs-lookup"><span data-stu-id="9662b-103">Policy Stores, Applications, and Scopes</span></span>

<span data-ttu-id="9662b-104">Gli archivi, le applicazioni e gli ambiti dei criteri di autorizzazione rappresentano diversi livelli di organizzazione dei criteri di gestione autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="9662b-104">Authorization policy stores, applications, and scopes represent different levels of organization of Authorization Manager policy.</span></span> <span data-ttu-id="9662b-105">Un archivio criteri può contenere una o più applicazioni e un'applicazione può contenere uno o più ambiti.</span><span class="sxs-lookup"><span data-stu-id="9662b-105">A policy store can contain one or more applications, and an application can contain one or more scopes.</span></span>

-   [<span data-ttu-id="9662b-106">Archivi dei criteri di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="9662b-106">Authorization Policy Stores</span></span>](#authorization-policy-stores)
-   [<span data-ttu-id="9662b-107">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="9662b-107">Applications</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="9662b-108">Ambiti</span><span class="sxs-lookup"><span data-stu-id="9662b-108">Scopes</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="9662b-109">Delegation</span><span class="sxs-lookup"><span data-stu-id="9662b-109">Delegation</span></span>](#delegation)
-   [<span data-ttu-id="9662b-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9662b-110">Related topics</span></span>](#related-topics)

## <a name="authorization-policy-stores"></a><span data-ttu-id="9662b-111">Archivi dei criteri di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="9662b-111">Authorization Policy Stores</span></span>

<span data-ttu-id="9662b-112">Nell'API di gestione autorizzazioni, un archivio dei criteri di autorizzazione è rappresentato da un oggetto [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="9662b-112">In the Authorization Manager API, an authorization policy store is represented by an [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="9662b-113">L'archivio dei criteri di autorizzazione contiene le definizioni e le assegnazioni di applicazioni, ambiti, operazioni, attività, ruoli e gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="9662b-113">The authorization policy store contains definitions and assignments of applications, scopes, operations, tasks, roles, and user groups.</span></span>

<span data-ttu-id="9662b-114">Un archivio dei criteri di autorizzazione può essere archiviato come file XML o in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9662b-114">An authorization policy store can be stored either as an XML file or in Active Directory.</span></span>

<span data-ttu-id="9662b-115">Un'applicazione deve inizializzare un archivio dei criteri di autorizzazione prima di modificare le informazioni nell'archivio o usare i criteri di archiviazione per controllare l'accesso client alle risorse.</span><span class="sxs-lookup"><span data-stu-id="9662b-115">An application must initialize an authorization policy store before changing information in the store or using the store policy to check client access to resources.</span></span>

<span data-ttu-id="9662b-116">Un archivio dei criteri di autorizzazione può contenere uno o più oggetti [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) che rappresentano i criteri di autorizzazione per un'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="9662b-116">An authorization policy store can contain one or more [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) objects that each represent authorization policy for a specific application.</span></span>

## <a name="applications"></a><span data-ttu-id="9662b-117">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="9662b-117">Applications</span></span>

<span data-ttu-id="9662b-118">Nell'API di gestione autorizzazioni, un'applicazione viene rappresentata da un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) .</span><span class="sxs-lookup"><span data-stu-id="9662b-118">In the Authorization Manager API, an application is represented by an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object.</span></span> <span data-ttu-id="9662b-119">Un archivio dei criteri di autorizzazione può contenere informazioni sui criteri di autorizzazione per molte applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9662b-119">An authorization policy store can contain authorization policy information for many applications.</span></span> <span data-ttu-id="9662b-120">L'uso di oggetti **IAzApplication** consente di archiviare criteri di autorizzazione diversi per applicazioni diverse in un singolo archivio criteri.</span><span class="sxs-lookup"><span data-stu-id="9662b-120">Using **IAzApplication** objects allows you to store different authorization policy for different applications in a single policy store.</span></span>

<span data-ttu-id="9662b-121">Un archivio dei criteri di autorizzazione deve contenere almeno un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9662b-121">An authorization policy store must contain at least one application.</span></span>

## <a name="scopes"></a><span data-ttu-id="9662b-122">Ambiti</span><span class="sxs-lookup"><span data-stu-id="9662b-122">Scopes</span></span>

<span data-ttu-id="9662b-123">Nell'API di gestione autorizzazioni, un ambito è rappresentato da un oggetto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="9662b-123">In the Authorization Manager API, a scope is represented by an [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span> <span data-ttu-id="9662b-124">Gli ambiti forniscono un livello di organizzazione aggiuntivo facoltativo per i criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="9662b-124">Scopes provide an additional, optional level of organization for an authorization policy.</span></span> <span data-ttu-id="9662b-125">Un'applicazione può contenere uno o più ambiti, ma non deve contenere alcun (gestione autorizzazioni fornisce un ambito predefinito a livello di applicazione).</span><span class="sxs-lookup"><span data-stu-id="9662b-125">An application can contain one or more scopes, but need not contain any (Authorization Manager provides a default, application-wide scope).</span></span>

<span data-ttu-id="9662b-126">Un ambito è una suddivisione in un'applicazione che separa le risorse da altre risorse utilizzate da tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="9662b-126">A scope is a subdivision within an application that separates resources from other resources that are used by that application.</span></span> <span data-ttu-id="9662b-127">Se si dispone di gruppi di gestione autorizzazioni, assegnazioni di ruolo, definizioni di ruoli o definizioni di attività che non si desidera applicare a un'intera applicazione, è possibile crearle a livello di ambito.</span><span class="sxs-lookup"><span data-stu-id="9662b-127">If you have Authorization Manager groups, role assignments, role definitions, or task definitions that you do not want to apply to an entire application, you can create them at the scope level.</span></span>

## <a name="delegation"></a><span data-ttu-id="9662b-128">Delegation</span><span class="sxs-lookup"><span data-stu-id="9662b-128">Delegation</span></span>

<span data-ttu-id="9662b-129">Gli archivi dei criteri di autorizzazione archiviati in Active Directory supportano la delega dell'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="9662b-129">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="9662b-130">L'amministrazione può essere delegata a utenti e gruppi a livello di punto vendita, applicazione o ambito.</span><span class="sxs-lookup"><span data-stu-id="9662b-130">Administration can be delegated to users and groups at the store, application, or scope level.</span></span> <span data-ttu-id="9662b-131">Ogni livello definisce i ruoli amministrativi per i criteri a tale livello.</span><span class="sxs-lookup"><span data-stu-id="9662b-131">Each level defines administrative roles for the policy at that level.</span></span> <span data-ttu-id="9662b-132">Per delegare il controllo a un utente o a un gruppo, assegnarlo al ruolo di amministratore. per consentire a un utente o a un gruppo di leggere il criterio, assegnarlo al ruolo Reader.</span><span class="sxs-lookup"><span data-stu-id="9662b-132">To delegate control to a user or group, assign them to the administrator role; to allow a user or group to read the policy, assign them to the reader role.</span></span>

<span data-ttu-id="9662b-133">Gli amministratori di un archivio, di un'applicazione o di un ambito possono leggere e modificare l'archivio criteri a livello delegato.</span><span class="sxs-lookup"><span data-stu-id="9662b-133">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="9662b-134">I lettori possono leggere l'archivio criteri a livello delegato, ma non modificare l'archivio.</span><span class="sxs-lookup"><span data-stu-id="9662b-134">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9662b-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9662b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9662b-136">Creazione di un oggetto archivio criteri di autorizzazione in C++</span><span class="sxs-lookup"><span data-stu-id="9662b-136">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="9662b-137">Creazione di un oggetto applicazione in C++</span><span class="sxs-lookup"><span data-stu-id="9662b-137">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="9662b-138">Delega della definizione di autorizzazioni in C++</span><span class="sxs-lookup"><span data-stu-id="9662b-138">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 




---
description: ACE per controllare l'accesso alle proprietà di un oggetto
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACE per controllare l'accesso alle proprietà di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227186"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a><span data-ttu-id="15ef9-103">ACE per controllare l'accesso alle proprietà di un oggetto</span><span class="sxs-lookup"><span data-stu-id="15ef9-103">ACEs to Control Access to an Object's Properties</span></span>

<span data-ttu-id="15ef9-104">L' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di un oggetto servizio directory (DS) può contenere una gerarchia di [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE), come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="15ef9-104">The [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of a directory service (DS) object can contain a hierarchy of [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), as follows:</span></span>

1.  <span data-ttu-id="15ef9-105">ACE che proteggono l'oggetto stesso</span><span class="sxs-lookup"><span data-stu-id="15ef9-105">ACEs that protect the object itself</span></span>
2.  <span data-ttu-id="15ef9-106">[Voci ACE specifiche dell'oggetto](object-specific-aces.md) che proteggono una proprietà specificata impostata nell'oggetto</span><span class="sxs-lookup"><span data-stu-id="15ef9-106">[Object-specific ACEs](object-specific-aces.md) that protect a specified property set on the object</span></span>
3.  <span data-ttu-id="15ef9-107">Voci ACE specifiche dell'oggetto che proteggono una proprietà specificata nell'oggetto</span><span class="sxs-lookup"><span data-stu-id="15ef9-107">Object-specific ACEs that protect a specified property on the object</span></span>

<span data-ttu-id="15ef9-108">All'interno di questa gerarchia, i diritti concessi o negati a un livello superiore sono validi anche per i livelli inferiori.</span><span class="sxs-lookup"><span data-stu-id="15ef9-108">Within this hierarchy, the rights granted or denied at a higher level apply also to the lower levels.</span></span> <span data-ttu-id="15ef9-109">Se, ad esempio, una voce ACE specifica dell'oggetto in un set di proprietà consente a un trustee il diritto di \_ \_ lettura di un dominio ADS \_ \_ , il trustee ha accesso in lettura implicito a tutte le proprietà di tale set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="15ef9-109">For example, if an object-specific ACE on a property set allows a trustee the ADS\_RIGHT\_DS\_READ\_PROP right, the trustee has implicit read access to all of the properties of that property set.</span></span> <span data-ttu-id="15ef9-110">Analogamente, una voce ACE nell'oggetto stesso che consente ADS \_ Rights \_ DS \_ Read \_ prop Access fornisce al trustee l'accesso in lettura a tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="15ef9-110">Similarly, an ACE on the object itself that allows ADS\_RIGHT\_DS\_READ\_PROP access gives the trustee read access to all of the object's properties.</span></span>

<span data-ttu-id="15ef9-111">Nella figura seguente viene illustrata la struttura ad albero di un oggetto DS ipotetico e dei relativi set di proprietà e proprietà.</span><span class="sxs-lookup"><span data-stu-id="15ef9-111">The following illustration shows the tree of a hypothetical DS object and its property sets and properties.</span></span>

![gerarchia di oggetti del servizio directory](images/accctrl2.png)

<span data-ttu-id="15ef9-113">Si supponga di voler consentire il seguente accesso alle proprietà di questo oggetto DS:</span><span class="sxs-lookup"><span data-stu-id="15ef9-113">Suppose you want to allow the following access to the properties of this DS object:</span></span>

-   <span data-ttu-id="15ef9-114">Consenti al gruppo un'autorizzazione di lettura/scrittura per tutte le proprietà dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="15ef9-114">Allow Group A read/write permission to all of the object's properties</span></span>
-   <span data-ttu-id="15ef9-115">Consenti a tutti gli utenti l'autorizzazione di lettura/scrittura per tutte le proprietà ad eccezione della proprietà D</span><span class="sxs-lookup"><span data-stu-id="15ef9-115">Allow everyone else read/write permission to all properties except Property D</span></span>

<span data-ttu-id="15ef9-116">A tale scopo, impostare le voci ACE nel DACL dell'oggetto, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="15ef9-116">To do this, set the ACEs in the object's DACL as shown in the following table.</span></span>



| <span data-ttu-id="15ef9-117">Fiduciario</span><span class="sxs-lookup"><span data-stu-id="15ef9-117">Trustee</span></span>  | <span data-ttu-id="15ef9-118">GUID oggetto</span><span class="sxs-lookup"><span data-stu-id="15ef9-118">Object GUID</span></span>    | <span data-ttu-id="15ef9-119">Tipo ACE</span><span class="sxs-lookup"><span data-stu-id="15ef9-119">ACE type</span></span>                  | <span data-ttu-id="15ef9-120">Diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="15ef9-120">Access rights</span></span>                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="15ef9-121">Gruppo A</span><span class="sxs-lookup"><span data-stu-id="15ef9-121">Group A</span></span>  | <span data-ttu-id="15ef9-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="15ef9-122">None</span></span>           | <span data-ttu-id="15ef9-123">ACE consentito per l'accesso</span><span class="sxs-lookup"><span data-stu-id="15ef9-123">Access-allowed ACE</span></span>        | <span data-ttu-id="15ef9-124">ADS \_ Rights \_ DS \_ Read \_ prop \| Ads \_ right \_ DS \_ scrivere \_ prop</span><span class="sxs-lookup"><span data-stu-id="15ef9-124">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="15ef9-125">Tutti</span><span class="sxs-lookup"><span data-stu-id="15ef9-125">Everyone</span></span> | <span data-ttu-id="15ef9-126">Set di proprietà 1</span><span class="sxs-lookup"><span data-stu-id="15ef9-126">Property Set 1</span></span> | <span data-ttu-id="15ef9-127">ACE oggetto consentito Access</span><span class="sxs-lookup"><span data-stu-id="15ef9-127">Access-allowed object ACE</span></span> | <span data-ttu-id="15ef9-128">ADS \_ Rights \_ DS \_ Read \_ prop \| Ads \_ right \_ DS \_ scrivere \_ prop</span><span class="sxs-lookup"><span data-stu-id="15ef9-128">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="15ef9-129">Tutti</span><span class="sxs-lookup"><span data-stu-id="15ef9-129">Everyone</span></span> | <span data-ttu-id="15ef9-130">Proprietà C</span><span class="sxs-lookup"><span data-stu-id="15ef9-130">Property C</span></span>     | <span data-ttu-id="15ef9-131">ACE oggetto consentito Access</span><span class="sxs-lookup"><span data-stu-id="15ef9-131">Access-allowed object ACE</span></span> | <span data-ttu-id="15ef9-132">ADS \_ Rights \_ DS \_ Read \_ prop \| Ads \_ right \_ DS \_ scrivere \_ prop</span><span class="sxs-lookup"><span data-stu-id="15ef9-132">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |



 

<span data-ttu-id="15ef9-133">La voce ACE per il gruppo A non ha un GUID oggetto, il che significa che consente l'accesso a tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="15ef9-133">The ACE for Group A does not have an object GUID, which means that it allows access to all the object's properties.</span></span> <span data-ttu-id="15ef9-134">La voce ACE specifica dell'oggetto per il set di proprietà 1 consente a tutti gli utenti di accedere alle proprietà A e B. L'altra voce ACE specifica dell'oggetto consente a tutti gli utenti di accedere alla proprietà C. si noti che, sebbene questo DACL non disponga di Ace con accesso negato, nega in modo implicito l'accesso alla proprietà D a tutti gli utenti tranne il gruppo A.</span><span class="sxs-lookup"><span data-stu-id="15ef9-134">The object-specific ACE for Property Set 1 allows everyone access to Properties A and B. The other object-specific ACE allows everyone access to Property C. Note that although this DACL does not have any access-denied ACEs, it implicitly denies Property D access to everyone except Group A.</span></span>

<span data-ttu-id="15ef9-135">Quando un utente tenta di accedere alla proprietà di un oggetto, il sistema controlla le voci ACE, in ordine, fino a quando l'accesso richiesto non viene concesso o negato in modo esplicito o non ci sono più voci ACE, nel qual caso l'accesso viene negato in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="15ef9-135">When a user tries to access an object's property, the system checks the ACEs, in order, until the requested access is explicitly granted, denied, or there are no more ACEs, in which case, access is implicitly denied.</span></span>

<span data-ttu-id="15ef9-136">Il sistema valuta:</span><span class="sxs-lookup"><span data-stu-id="15ef9-136">The system evaluates:</span></span>

-   <span data-ttu-id="15ef9-137">Ace applicabili all'oggetto stesso</span><span class="sxs-lookup"><span data-stu-id="15ef9-137">ACEs that apply to the object itself</span></span>
-   <span data-ttu-id="15ef9-138">Voci ACE specifiche dell'oggetto applicabili al set di proprietà che contiene la proprietà a cui si accede</span><span class="sxs-lookup"><span data-stu-id="15ef9-138">Object-specific ACEs that apply to the property set that contains the property being accessed</span></span>
-   <span data-ttu-id="15ef9-139">Voci ACE specifiche dell'oggetto applicabili alla proprietà a cui si accede</span><span class="sxs-lookup"><span data-stu-id="15ef9-139">Object-specific ACEs that apply to the property being accessed</span></span>

<span data-ttu-id="15ef9-140">Il sistema ignora le voci ACE specifiche dell'oggetto applicabili ad altri set di proprietà o proprietà.</span><span class="sxs-lookup"><span data-stu-id="15ef9-140">The system ignores object-specific ACEs that apply to other property sets or properties.</span></span>

 

 

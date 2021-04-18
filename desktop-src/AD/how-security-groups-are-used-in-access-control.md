---
title: Modalità di utilizzo di gruppi di sicurezza nel controllo di accesso
description: L'ID di sicurezza (SID) è l'identificatore di oggetto dell'utente o del gruppo di sicurezza quando l'utente o il gruppo viene utilizzato per motivi di sicurezza.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Modalità di utilizzo di gruppi di sicurezza nel controllo di accesso
- controllo di accesso, gruppi di sicurezza usati in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297732"
---
# <a name="how-security-groups-are-used-in-access-control"></a><span data-ttu-id="46d83-105">Modalità di utilizzo di gruppi di sicurezza nel controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="46d83-105">How Security Groups are Used in Access Control</span></span>

<span data-ttu-id="46d83-106">L'ID di sicurezza (SID) è l'identificatore di oggetto dell'utente o del gruppo di sicurezza quando l'utente o il gruppo viene utilizzato per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="46d83-106">The security identifier (SID) is the object identifier of the user or security group when the user or group is used for security purposes.</span></span> <span data-ttu-id="46d83-107">Il nome dell'utente o del gruppo non viene utilizzato come identificatore univoco all'interno del sistema.</span><span class="sxs-lookup"><span data-stu-id="46d83-107">The name of the user or group is not used as the unique identifier within the system.</span></span> <span data-ttu-id="46d83-108">Il SID viene archiviato nell'attributo **objectSID** degli oggetti utente e dei gruppi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="46d83-108">The SID is stored in the **objectSid** attribute of user objects and security group objects.</span></span> <span data-ttu-id="46d83-109">Il server di Active Directory genera il **objectSID** quando viene creato l'utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="46d83-109">The Active Directory server generates the **objectSid** when the user or group is created.</span></span> <span data-ttu-id="46d83-110">Il sistema garantisce che i SID siano univoci in una foresta.</span><span class="sxs-lookup"><span data-stu-id="46d83-110">The system ensures that the SIDs are unique across a forest.</span></span> <span data-ttu-id="46d83-111">Tenere presente che **objectGUID** è l'identificatore univoco di un utente, di un gruppo o di qualsiasi altro oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="46d83-111">Be aware that the **objectGuid** is the unique identifier of a user, group, or any other directory object.</span></span> <span data-ttu-id="46d83-112">Il SID viene modificato se un utente o un gruppo viene spostato in un altro dominio; il **objectGUID** rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="46d83-112">The SID changes if a user or group is moved to another domain; the **objectGuid** remains the same.</span></span>

<span data-ttu-id="46d83-113">Quando a un utente o a un gruppo viene assegnata l'autorizzazione per accedere a una risorsa, ad esempio una stampante o una condivisione file, il SID dell'utente o del gruppo viene aggiunto alla voce di controllo di accesso (ACE) che definisce l'autorizzazione concessa nell'elenco di controllo di accesso discrezionale (DACL) della risorsa.</span><span class="sxs-lookup"><span data-stu-id="46d83-113">When a user or group is given permission to access a resource, such as a printer or a file share, the SID of the user or group is added to the access control entry (ACE) defining the granted permission in the resource's discretionary access control list (DACL).</span></span> <span data-ttu-id="46d83-114">In Active Directory Domain Services, ogni oggetto dispone di un attributo **ntSecurityDescriptor** che archivia un DACL che definisce l'accesso a quell'oggetto o gli attributi specifici su tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="46d83-114">In Active Directory Domain Services, each object has an **nTSecurityDescriptor** attribute that stores a DACL defining the access to that particular object or attributes on that object.</span></span> <span data-ttu-id="46d83-115">Per ulteriori informazioni sull'impostazione del controllo di accesso per gli oggetti in Active Directory Domain Services, vedere [controllo dell'accesso agli oggetti in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="46d83-115">For more information about setting access control on objects in Active Directory Domain Services, see [Controlling Access to Objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="46d83-116">Quando un utente accede a un dominio Windows 2000, il sistema operativo genera un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="46d83-116">When a user logs on to a Windows 2000 domain, the operating system generates an access token.</span></span> <span data-ttu-id="46d83-117">Questo token di accesso viene usato per determinare a quali risorse può accedere l'utente.</span><span class="sxs-lookup"><span data-stu-id="46d83-117">This access token is used to determine which resources the user may access.</span></span> <span data-ttu-id="46d83-118">Il token di accesso utente include i dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="46d83-118">The user access token includes the following data:</span></span>

-   <span data-ttu-id="46d83-119">SID utente.</span><span class="sxs-lookup"><span data-stu-id="46d83-119">User SID.</span></span>
-   <span data-ttu-id="46d83-120">SID di tutti i gruppi di sicurezza globali e universali di cui l'utente è membro.</span><span class="sxs-lookup"><span data-stu-id="46d83-120">SIDs of all global and universal security groups that the user is a member of.</span></span>
-   <span data-ttu-id="46d83-121">SID di tutti i gruppi di sicurezza globali e universali annidati.</span><span class="sxs-lookup"><span data-stu-id="46d83-121">SIDs of all nested global and universal security groups.</span></span>

<span data-ttu-id="46d83-122">Ogni processo eseguito per conto di questo utente ha una copia di questo token di accesso.</span><span class="sxs-lookup"><span data-stu-id="46d83-122">Every process executed on behalf of this user has a copy of this access token.</span></span>

<span data-ttu-id="46d83-123">Quando l'utente tenta di accedere alle risorse in un computer, il servizio tramite il quale l'utente accede alla risorsa rappresenterà l'utente creando un nuovo token di accesso in base al token di accesso creato al momento dell'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="46d83-123">When the user attempts to access resources on a computer, the service through which the user accesses the resource will impersonate the user by creating a new access token based on the access token created at user logon time.</span></span> <span data-ttu-id="46d83-124">Questo nuovo token di accesso conterrà anche i SID seguenti:</span><span class="sxs-lookup"><span data-stu-id="46d83-124">This new access token will also contain the following SIDs:</span></span>

-   <span data-ttu-id="46d83-125">SID per tutti i gruppi locali di dominio nel dominio di destinazione di cui l'utente è membro.</span><span class="sxs-lookup"><span data-stu-id="46d83-125">SIDs for all domain local groups in the target domain that the user is a member of.</span></span>
-   <span data-ttu-id="46d83-126">SID per tutti i gruppi locali del computer nel computer di destinazione di cui l'utente è membro.</span><span class="sxs-lookup"><span data-stu-id="46d83-126">SIDs for all machine local groups on the target computer that the user is a member of.</span></span>

<span data-ttu-id="46d83-127">Il servizio usa questo nuovo token di accesso per valutare l'accesso alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="46d83-127">The service uses this new access token to evaluate access to the resource.</span></span> <span data-ttu-id="46d83-128">Se un SID nel token di accesso viene visualizzato in tutte le voci ACE del DACL, il servizio fornisce all'utente le autorizzazioni specificate in tali ACE.</span><span class="sxs-lookup"><span data-stu-id="46d83-128">If a SID in the access token appears in any ACEs in the DACL, the service gives the user the permissions specified in those ACEs.</span></span>

 

 





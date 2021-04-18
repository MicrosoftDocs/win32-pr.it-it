---
description: Viene illustrata la definizione di utenti e gruppi nell'API di gestione autorizzazioni.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Utenti e gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319396"
---
# <a name="users-and-groups"></a><span data-ttu-id="78093-103">Utenti e gruppi</span><span class="sxs-lookup"><span data-stu-id="78093-103">Users and Groups</span></span>

<span data-ttu-id="78093-104">In Gestione autorizzazioni, i destinatari dei criteri di autorizzazione sono rappresentati dai gruppi seguenti:</span><span class="sxs-lookup"><span data-stu-id="78093-104">In Authorization Manager, recipients of authorization policy are represented by the following groups:</span></span>

-   <span data-ttu-id="78093-105">Utenti e gruppi di Windows</span><span class="sxs-lookup"><span data-stu-id="78093-105">Windows Users and Groups</span></span>

    <span data-ttu-id="78093-106">Questi gruppi includono utenti, computer e gruppi predefiniti per le entità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="78093-106">These groups include users, computers, and built-in groups for security principals.</span></span>

-   <span data-ttu-id="78093-107">Gruppi di query LDAP</span><span class="sxs-lookup"><span data-stu-id="78093-107">LDAP Query Groups</span></span>

    <span data-ttu-id="78093-108">L'appartenenza a questi gruppi viene calcolata in modo dinamico in base alle esigenze delle query LDAP (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="78093-108">Membership in these groups is dynamically calculated as needed from Lightweight Directory Access Protocol (LDAP) queries.</span></span> <span data-ttu-id="78093-109">Un gruppo di query LDAP è un tipo di gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="78093-109">An LDAP query group is a type of application group.</span></span>

-   <span data-ttu-id="78093-110">Gruppi di applicazioni di base</span><span class="sxs-lookup"><span data-stu-id="78093-110">Basic Application Groups</span></span>

    <span data-ttu-id="78093-111">Questi gruppi sono costituiti da gruppi di query LDAP, utenti e gruppi di Windows e altri gruppi di applicazioni di base.</span><span class="sxs-lookup"><span data-stu-id="78093-111">These groups consist of LDAP query groups, Windows users and groups, and other basic application groups.</span></span>

## <a name="windows-users-and-groups"></a><span data-ttu-id="78093-112">Utenti e gruppi di Windows</span><span class="sxs-lookup"><span data-stu-id="78093-112">Windows Users and Groups</span></span>

<span data-ttu-id="78093-113">Questi sono gli stessi utenti e gruppi utilizzati in tutto il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="78093-113">These are the same as the users and groups used throughout the Windows operating system.</span></span>

## <a name="ldap-query-groups"></a><span data-ttu-id="78093-114">Gruppi di query LDAP</span><span class="sxs-lookup"><span data-stu-id="78093-114">LDAP Query Groups</span></span>

<span data-ttu-id="78093-115">In Gestione autorizzazioni è possibile utilizzare le query LDAP in modo che corrispondano agli attributi dell'utente con quelli dell'oggetto dell'utente in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78093-115">In Authorization Manager, you can use LDAP queries to match the user's attributes with those of the user's object in Active Directory.</span></span>

<span data-ttu-id="78093-116">Ad esempio, la query seguente trova tutti tranne Andy.</span><span class="sxs-lookup"><span data-stu-id="78093-116">For example, the following query finds everyone except Andy.</span></span>


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



<span data-ttu-id="78093-117">La query seguente consente di trovare tutti i membri dell'alias di un utente in www.fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="78093-117">The following query finds all members of the someone alias at www.fabrikam.com.</span></span>


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a><span data-ttu-id="78093-118">Gruppi di applicazioni di base</span><span class="sxs-lookup"><span data-stu-id="78093-118">Basic Application Groups</span></span>

<span data-ttu-id="78093-119">Nell'API di gestione autorizzazioni, un gruppo di applicazioni è rappresentato da un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="78093-119">In the Authorization Manager API, an application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span> <span data-ttu-id="78093-120">Un gruppo di applicazioni di base è un tipo di gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="78093-120">A basic application group is a type of application group.</span></span>

<span data-ttu-id="78093-121">Per definire l'appartenenza a un gruppo di applicazioni di base, definire chi è un membro e definire chi non è un membro.</span><span class="sxs-lookup"><span data-stu-id="78093-121">To define basic application group membership, define who is a member and define who is not a member.</span></span> <span data-ttu-id="78093-122">Entrambi questi passaggi vengono eseguiti nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="78093-122">Both of these steps are carried out in the same way.</span></span> <span data-ttu-id="78093-123">Specificare zero o più utenti e gruppi di Windows, gruppi di applicazioni di base definiti in precedenza o gruppi di query LDAP.</span><span class="sxs-lookup"><span data-stu-id="78093-123">Specify zero or more Windows users and groups, previously defined basic application groups, or LDAP query groups.</span></span> <span data-ttu-id="78093-124">L'appartenenza del gruppo di applicazioni di base viene calcolata rimuovendo tutti i membri non appartenenti al gruppo.</span><span class="sxs-lookup"><span data-stu-id="78093-124">The membership of the basic application group is calculated by removing any nonmembers from the group.</span></span> <span data-ttu-id="78093-125">Gestione autorizzazioni esegue questa operazione automaticamente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="78093-125">Authorization Manager does this automatically at run time.</span></span>

<span data-ttu-id="78093-126">Il non membro di un gruppo di applicazioni di base ha la precedenza sull'appartenenza.</span><span class="sxs-lookup"><span data-stu-id="78093-126">Nonmembership in a basic application group takes precedence over membership.</span></span>

<span data-ttu-id="78093-127">Le definizioni di appartenenza circolari non sono consentite. generano il messaggio di errore seguente: "Impossibile aggiungere GroupName.</span><span class="sxs-lookup"><span data-stu-id="78093-127">Circular membership definitions are not allowed; they result in the following error message: "Cannot add GroupName.</span></span> <span data-ttu-id="78093-128">Si è verificato il seguente problema: è stato rilevato un ciclo ".</span><span class="sxs-lookup"><span data-stu-id="78093-128">The following problem occurred: A loop has been detected."</span></span>

## <a name="related-topics"></a><span data-ttu-id="78093-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78093-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78093-130">Definizione di gruppi di utenti in C++</span><span class="sxs-lookup"><span data-stu-id="78093-130">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 




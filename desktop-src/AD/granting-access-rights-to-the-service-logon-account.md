---
title: Concessione dei diritti di accesso all'account di accesso al servizio
description: Una considerazione principale dell'installazione di un'istanza del servizio consiste nel garantire che il servizio installato possa accedere alle risorse necessarie.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Concessione dei diritti di accesso all'account di accesso del servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299573"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a><span data-ttu-id="0773f-104">Concessione dei diritti di accesso all'account di accesso al servizio</span><span class="sxs-lookup"><span data-stu-id="0773f-104">Granting Access Rights to the Service Logon Account</span></span>

<span data-ttu-id="0773f-105">Una considerazione principale dell'installazione di un'istanza del servizio consiste nel garantire che il servizio installato possa accedere alle risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="0773f-105">A primary consideration of installing a service instance is to ensure that the installed service can access the necessary resources.</span></span> <span data-ttu-id="0773f-106">A tale scopo, impostare le voci ACE nei descrittori di sicurezza degli oggetti a cui il servizio deve accedere.</span><span class="sxs-lookup"><span data-stu-id="0773f-106">To do this, set ACEs in the security descriptors of objects that the service must access.</span></span> <span data-ttu-id="0773f-107">Una voce ACE può concedere o negare i diritti di accesso a un'entità di sicurezza specificata, ad esempio l'account utente del servizio o l'account computer per un servizio LocalSystem, oppure un gruppo a cui appartiene l'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="0773f-107">An ACE can grant or deny access rights to a specified security principal, such as the service user account, or the computer account for a LocalSystem service, or a group to which the service's account belongs.</span></span> <span data-ttu-id="0773f-108">Per altre informazioni su Ace, descrittori di sicurezza e controllo di accesso, vedere controllo [dell'accesso agli oggetti in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) e [controllo di accesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="0773f-108">For more information about ACEs, security descriptors, and access control, see [Controlling Access to objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="0773f-109">Per altre informazioni e un esempio di codice che può essere usato per impostare una voce ACE che consente al servizio di modificare il punto di connessione del servizio, vedere [Abilitazione dell'account del servizio per l'accesso alle proprietà SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0773f-109">For more information and a code example that can be used to set an ACE that enables the service to modify its service connection point, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>

<span data-ttu-id="0773f-110">In alcuni casi, è necessario aggiungere l'account utente del servizio come membro di uno o più gruppi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0773f-110">In some cases, you must add your service user account as a member of one or more security groups.</span></span> <span data-ttu-id="0773f-111">Se, ad esempio, si crea un gruppo Administrators per il servizio, è possibile rendere il servizio un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="0773f-111">For example, if you create an administrators group for your service, you might make the service a member of the group.</span></span> <span data-ttu-id="0773f-112">È quindi possibile concedere diritti di accesso al gruppo anziché concederli in modo esplicito all'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="0773f-112">You can then grant access rights to the group rather than granting them explicitly to the service account.</span></span> <span data-ttu-id="0773f-113">Per ulteriori informazioni sui gruppi di sicurezza, vedere [gestione dei gruppi](managing-groups.md).</span><span class="sxs-lookup"><span data-stu-id="0773f-113">For more information about security groups, see [Managing Groups](managing-groups.md).</span></span>

 

 
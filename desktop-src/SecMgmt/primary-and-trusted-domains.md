---
description: I termini seguenti descrivono i domini presenti nei sistemi remoti.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Domini primari e Trusted
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525717"
---
# <a name="primary-and-trusted-domains"></a><span data-ttu-id="9aced-103">Domini primari e Trusted</span><span class="sxs-lookup"><span data-stu-id="9aced-103">Primary and Trusted Domains</span></span>

<span data-ttu-id="9aced-104">I termini seguenti descrivono i domini presenti nei sistemi remoti.</span><span class="sxs-lookup"><span data-stu-id="9aced-104">The following terms describe domains that exist on remote systems.</span></span>

-   [<span data-ttu-id="9aced-105">Dominio primario</span><span class="sxs-lookup"><span data-stu-id="9aced-105">Primary Domain</span></span>](#primary-domain)
-   [<span data-ttu-id="9aced-106">Dominio trusted</span><span class="sxs-lookup"><span data-stu-id="9aced-106">Trusted Domain</span></span>](#primary-and-trusted-domains)

## <a name="primary-domain"></a><span data-ttu-id="9aced-107">Dominio primario</span><span class="sxs-lookup"><span data-stu-id="9aced-107">Primary Domain</span></span>

<span data-ttu-id="9aced-108">Un dominio primario è il dominio responsabile della creazione di relazioni di trust aggiuntive e l'esecuzione dell'autenticazione (o per il passaggio di una richiesta di autenticazione a un dominio trusted appropriato).</span><span class="sxs-lookup"><span data-stu-id="9aced-108">A primary domain is the domain that is responsible for establishing further trust relationships and performing authentication (or for passing an authentication request on to an appropriate trusted domain).</span></span> <span data-ttu-id="9aced-109">I controller di dominio nel dominio primario gestiscono o passano le richieste di autenticazione che provengono dalla workstation.</span><span class="sxs-lookup"><span data-stu-id="9aced-109">The domain controllers in the primary domain handle or pass along authentication requests that originate at the workstation.</span></span>

<span data-ttu-id="9aced-110">Quando si verifica l'accesso, LSA controlla i domini di account e predefiniti per le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9aced-110">When logon occurs, the LSA checks the built-in and account domains for authentication information.</span></span> <span data-ttu-id="9aced-111">Se l'account a cui si è connessi non è in uno di questi domini, la richiesta di accesso viene passata al dominio primario del sistema.</span><span class="sxs-lookup"><span data-stu-id="9aced-111">If the account being logged on to is not in either of these domains, the logon request is handed off to the system's primary domain.</span></span>

## <a name="trusted-domain"></a><span data-ttu-id="9aced-112">Dominio trusted</span><span class="sxs-lookup"><span data-stu-id="9aced-112">Trusted Domain</span></span>

<span data-ttu-id="9aced-113">Un dominio trusted è un dominio considerato attendibile dal sistema locale per autenticare gli utenti.</span><span class="sxs-lookup"><span data-stu-id="9aced-113">A trusted domain is a domain that the local system trusts to authenticate users.</span></span> <span data-ttu-id="9aced-114">In altre parole, se un utente o un'applicazione viene autenticata da un dominio trusted, questa autenticazione viene accettata da tutti i domini che considerano attendibile il dominio di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9aced-114">In other words, if a user or application is authenticated by a trusted domain, this authentication is accepted by all domains that trust the authenticating domain.</span></span>

<span data-ttu-id="9aced-115">Ogni dominio subordinato dispone automaticamente di una relazione di trust bidirezionale con il dominio principale.</span><span class="sxs-lookup"><span data-stu-id="9aced-115">Each subordinate domain automatically has a two-way trust relationship with the main domain.</span></span> <span data-ttu-id="9aced-116">Per impostazione predefinita, questa relazione di trust è transitiva, vale a dire che se un sistema considera attendibile il dominio A, considera attendibili anche tutti i domini A cui viene associato un trust.</span><span class="sxs-lookup"><span data-stu-id="9aced-116">By default, this trust is transitive, meaning that if a system trusts Domain A, it also trusts all domains that Domain A trusts.</span></span> <span data-ttu-id="9aced-117">I trust unidirezionali sono supportati anche per i sistemi operativi precedenti a Windows 2000, che non supportano i trust transitivi bidirezionali.</span><span class="sxs-lookup"><span data-stu-id="9aced-117">One-way trusts are also supported for operating systems earlier than Windows 2000, which do not support transitive, two-way trusts.</span></span>

<span data-ttu-id="9aced-118">L' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) ha un tipo di oggetto, [**trustedDomain**](the-trusteddomain-object-type.md), usato per archiviare le informazioni sulle relazioni di trust, inclusi il nome e l' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) del dominio trusted, l'account nel dominio da usare per le richieste di autenticazione, le richieste di conversione di nome e SID e i nomi dei controller di dominio nel dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="9aced-118">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) has an object type, [**TrustedDomain**](the-trusteddomain-object-type.md), that is used to store information about trust relationships, including the name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the trusted domain, the account in the domain to use for authentication requests, name and SID translation requests, and the names of domain controllers in the trusted domain.</span></span>

<span data-ttu-id="9aced-119">Nei controller di dominio, LSA crea un'istanza di un oggetto [**trustedDomain**](the-trusteddomain-object-type.md) per ogni dominio considerato attendibile dal sistema locale.</span><span class="sxs-lookup"><span data-stu-id="9aced-119">On domain controllers, the LSA creates an instance of a [**TrustedDomain**](the-trusteddomain-object-type.md) object for each domain trusted by the local system.</span></span>

<span data-ttu-id="9aced-120">Se, ad esempio, una workstation Windows XP considera attendibile un controller di dominio di Windows 2000 che a sua volta considera attendibili altri quattro sistemi, la workstation, connessa con attendibilità transitiva, avrà cinque oggetti [**trustedDomain**](the-trusteddomain-object-type.md) nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="9aced-120">For example, if a Windows XP workstation trusts a Windows 2000 domain controller that in turn trusts four other systems, the workstation, connected using transitive trust, will have five [**TrustedDomain**](the-trusteddomain-object-type.md) objects on its local system.</span></span>

 

 

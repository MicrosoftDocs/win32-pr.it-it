---
title: Binding senza server e RootDSE
description: Se possibile, non impostare come hardcoded un nome di server.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Binding senza server e RootDSE AD
- AD binding senza server
- RootDSE AD
- Active Directory, utilizzo, associazione, binding senza server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472483"
---
# <a name="serverless-binding-and-rootdse"></a><span data-ttu-id="8b6d6-107">Binding senza server e RootDSE</span><span class="sxs-lookup"><span data-stu-id="8b6d6-107">Serverless Binding and RootDSE</span></span>

<span data-ttu-id="8b6d6-108">Se possibile, non impostare come hardcoded un nome di server.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-108">If possible, do not hard-code a server name.</span></span> <span data-ttu-id="8b6d6-109">Inoltre, nella maggior parte dei casi, l'associazione non deve essere necessariamente legata a un singolo server.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-109">Furthermore, under most circumstances, binding should not be unnecessarily tied to a single server.</span></span> <span data-ttu-id="8b6d6-110">Active Directory Domain Services supportano il binding senza server, il che significa che Active Directory può essere associato a nel dominio predefinito senza specificare il nome di un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-110">Active Directory Domain Services support serverless binding, which means that Active Directory can be bound to on the default domain without specifying the name of a domain controller.</span></span> <span data-ttu-id="8b6d6-111">Per le applicazioni ordinarie, si tratta in genere del dominio dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-111">For ordinary applications, this is typically the domain of the logged-on user.</span></span> <span data-ttu-id="8b6d6-112">Per le applicazioni di servizio, si tratta del dominio dell'account di accesso al servizio o del client rappresentato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-112">For service applications, this is either the domain of the service logon account or that of the client that the service impersonates.</span></span>

<span data-ttu-id="8b6d6-113">In LDAP 3,0, rootDSE è definito come la radice dell'albero dei dati di directory in un server di directory.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-113">In LDAP 3.0, rootDSE is defined as the root of the directory data tree on a directory server.</span></span> <span data-ttu-id="8b6d6-114">RootDSE non fa parte di alcuno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-114">The rootDSE is not part of any namespace.</span></span> <span data-ttu-id="8b6d6-115">Lo scopo di rootDSE è fornire i dati sul server di directory.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-115">The purpose of the rootDSE is to provide data about the directory server.</span></span> <span data-ttu-id="8b6d6-116">Di seguito è riportata la stringa di associazione utilizzata per l'associazione a rootDSE.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-116">The following is the binding string that is used to bind to rootDSE.</span></span>


```C++
LDAP://<servername>/rootDSE
```



<span data-ttu-id="8b6d6-117"><servername>È il nome DNS di un server.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-117">The <servername> is the DNS name of a server.</span></span> <span data-ttu-id="8b6d6-118"><servername>È facoltativo, come illustrato nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-118">The <servername> is optional, as shown in the following format.</span></span>


```C++
LDAP://rootDSE
```



<span data-ttu-id="8b6d6-119">In questo caso, verrà utilizzato un controller di dominio predefinito del dominio in cui si trova il contesto di sicurezza del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-119">In this case, a default domain controller from the domain that the security context of the calling thread is in will be used.</span></span> <span data-ttu-id="8b6d6-120">Se non è possibile accedere a un controller di dominio all'interno del sito, verrà utilizzato il primo controller di dominio che è possibile individuare.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-120">If a domain controller cannot be accessed within the site, the first domain controller that can be found will be used.</span></span>

<span data-ttu-id="8b6d6-121">RootDSE è una posizione nota e affidabile in ogni server di directory per ottenere nomi distinti del dominio, dello schema e dei contenitori di configurazione e di altri dati sul server e il contenuto dell'albero dei dati di directory.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-121">The rootDSE is a well-known and reliable location on every directory server to get distinguished names of the domain, schema, and configuration containers, and other data about the server and the contents of its directory data tree.</span></span> <span data-ttu-id="8b6d6-122">Queste proprietà cambiano raramente in un particolare server.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-122">These properties rarely change on a particular server.</span></span> <span data-ttu-id="8b6d6-123">Un'applicazione può leggere queste proprietà all'avvio e usarle in tutta la sessione.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-123">An application can read these properties at startup and use them throughout the session.</span></span>

<span data-ttu-id="8b6d6-124">In sintesi, un'applicazione deve usare un'associazione senza server per eseguire l'associazione alla directory nel dominio corrente, usare rootDSE per ottenere il nome distinto per uno spazio dei nomi e usare tale nome distinto per l'associazione agli oggetti nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-124">In summary, an application should use serverless binding to bind to the directory on the current domain, use rootDSE to get the distinguished name for a namespace, and use that distinguished name to bind to objects in the namespace.</span></span>

<span data-ttu-id="8b6d6-125">Per ulteriori informazioni sugli attributi supportati da rootDSE, vedere [RootDSE](/windows/desktop/ADSchema/rootdse) nella documentazione dello Schema di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8b6d6-125">For more information about attributes supported by rootDSE, see [RootDSE](/windows/desktop/ADSchema/rootdse) in the Active Directory Schema documentation.</span></span>

<span data-ttu-id="8b6d6-126">Per ulteriori informazioni e un esempio di codice che illustra come utilizzare binding senza server e rootDSE, vedere [il codice di esempio per ottenere il nome distinto del dominio](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span><span class="sxs-lookup"><span data-stu-id="8b6d6-126">For more information and a code example that shows how to use serverless binding and rootDSE, see [Example Code for Getting the Distinguished Name of the Domain](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span></span>

 

 
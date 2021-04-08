---
title: Uso di Active Directory Domain Services
description: In questa sezione vengono fornite le linee guida per la scrittura di applicazioni che utilizzano o pubblicano dati in un servizio directory Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory utilizzando
- Active Directory Domain Services Active Directory utilizzando
- Esempi di Active Directory Active Directory
- Esempi di Active Directory Domain Services Active Directory
- esempi Active Directory
- Active Directory Active Directory, esempi vedere Active Directory Domain Services esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734546"
---
# <a name="using-active-directory-domain-services"></a><span data-ttu-id="147c3-109">Uso di Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="147c3-109">Using Active Directory Domain Services</span></span>

<span data-ttu-id="147c3-110">In questa sezione vengono fornite le linee guida per la scrittura di applicazioni che utilizzano o pubblicano dati in un servizio directory Active Directory.</span><span class="sxs-lookup"><span data-stu-id="147c3-110">This section provides guidelines for writing applications that use or publish data in an Active Directory directory service.</span></span>

> [!Note]  
> <span data-ttu-id="147c3-111">La documentazione seguente è destinata ai programmatori di computer.</span><span class="sxs-lookup"><span data-stu-id="147c3-111">The following documentation is for computer programmers.</span></span> <span data-ttu-id="147c3-112">Se si sta tentando di risolvere un errore di stampa della Home Active Directory, vedere il [seguente suggerimento](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) dalle pagine della community Microsoft. Se ciò non è utile, provare questi consigli da [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span><span class="sxs-lookup"><span data-stu-id="147c3-112">If you are trying to resolve an Active Directory home printing error, see the [following suggestion](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) from the Microsoft community pages; if that doesn't help, try these recommendations from [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span></span>

 

<span data-ttu-id="147c3-113">Active Directory Domain Services sono conformi al protocollo Lightweight Directory Access Protocol 3,0, definito da RFC 2251 e altre RFC.</span><span class="sxs-lookup"><span data-stu-id="147c3-113">Active Directory Domain Services are compliant with Lightweight Directory Access Protocol 3.0, which is defined by RFC 2251 and other RFCs.</span></span> <span data-ttu-id="147c3-114">È possibile usare uno dei set di API seguenti per accedere a Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="147c3-114">Any of the following API sets can be used to access Active Directory Domain Services.</span></span> <span data-ttu-id="147c3-115">Ogni set di API presenta vantaggi e svantaggi che dipendono dal linguaggio di programmazione, dall'ambiente di programmazione e dal metodo di esecuzione previsto.</span><span class="sxs-lookup"><span data-stu-id="147c3-115">Each API set has advantages and disadvantages that depend on the programming language, programming environment, and intended method of execution.</span></span> <span data-ttu-id="147c3-116">La maggior parte degli esempi in questa guida utilizza ADSI, supportato da linguaggi quali C e C++, nonché linguaggi conformi all'automazione come Microsoft Visual Basic e Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="147c3-116">The majority of the examples in this guide use ADSI, which is supported by languages such as C and C++, as well as automation-compliant languages such as Microsoft Visual Basic and Visual Basic Scripting Edition.</span></span>

<span data-ttu-id="147c3-117">Per ulteriori informazioni sulle tecnologie Active Directory Domain Services specifiche, vedere:</span><span class="sxs-lookup"><span data-stu-id="147c3-117">For more information about specific Active Directory Domain Services technologies, see:</span></span>

-   [<span data-ttu-id="147c3-118">Lightweight Directory Access Protocol</span><span class="sxs-lookup"><span data-stu-id="147c3-118">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [<span data-ttu-id="147c3-119">Interfacce di servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="147c3-119">Active Directory Service Interfaces</span></span>](../adsi/active-directory-service-interfaces-adsi.md)
-   [<span data-ttu-id="147c3-120">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="147c3-120">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)

<span data-ttu-id="147c3-121">In questa sezione vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="147c3-121">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="147c3-122">Binding a Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="147c3-122">Binding to Active Directory Domain Services</span></span>](binding-to-active-directory-domain-services.md)
-   [<span data-ttu-id="147c3-123">Ricerca in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="147c3-123">Searching in Active Directory Domain Services</span></span>](searching-in-active-directory-domain-services.md)
-   [<span data-ttu-id="147c3-124">Creazione ed eliminazione di oggetti in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="147c3-124">Creating and Deleting Objects in Active Directory Domain Services</span></span>](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="147c3-125">Trasferimento di oggetti</span><span class="sxs-lookup"><span data-stu-id="147c3-125">Moving Objects</span></span>](moving-objects.md)
-   [<span data-ttu-id="147c3-126">Lettura e scrittura degli attributi degli oggetti in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="147c3-126">Reading and Writing Attributes of Objects in Active Directory Domain Services</span></span>](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="147c3-127">Controllo dell'accesso agli oggetti in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="147c3-127">Controlling Access to Objects in Active Directory Domain Services</span></span>](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="147c3-128">Estensione dello schema</span><span class="sxs-lookup"><span data-stu-id="147c3-128">Extending the Schema</span></span>](extending-the-schema.md)
-   [<span data-ttu-id="147c3-129">Estensione dell'interfaccia utente per gli oggetti directory</span><span class="sxs-lookup"><span data-stu-id="147c3-129">Extending the User Interface for Directory Objects</span></span>](extending-the-user-interface-for-directory-objects.md)
-   [<span data-ttu-id="147c3-130">Gestione degli utenti</span><span class="sxs-lookup"><span data-stu-id="147c3-130">Managing Users</span></span>](managing-users.md)
-   [<span data-ttu-id="147c3-131">Gestione dei gruppi</span><span class="sxs-lookup"><span data-stu-id="147c3-131">Managing Groups</span></span>](managing-groups.md)
-   [<span data-ttu-id="147c3-132">Rilevamento delle modifiche</span><span class="sxs-lookup"><span data-stu-id="147c3-132">Tracking Changes</span></span>](tracking-changes.md)
-   [<span data-ttu-id="147c3-133">Pubblicazione di un servizio</span><span class="sxs-lookup"><span data-stu-id="147c3-133">Service Publication</span></span>](service-publication.md)
-   [<span data-ttu-id="147c3-134">Account di accesso al servizio</span><span class="sxs-lookup"><span data-stu-id="147c3-134">Service Logon Accounts</span></span>](service-logon-accounts.md)
-   [<span data-ttu-id="147c3-135">Autenticazione reciproca tramite Kerberos</span><span class="sxs-lookup"><span data-stu-id="147c3-135">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
-   [<span data-ttu-id="147c3-136">Backup e ripristino Active Directory</span><span class="sxs-lookup"><span data-stu-id="147c3-136">Backing Up and Restoring Active Directory</span></span>](backing-up-and-restoring-an-active-directory-server.md)
-   [<span data-ttu-id="147c3-137">Archiviazione Dynamic Data</span><span class="sxs-lookup"><span data-stu-id="147c3-137">Storing Dynamic Data</span></span>](storing-dynamic-data.md)
-   [<span data-ttu-id="147c3-138">Partizioni di directory applicative</span><span class="sxs-lookup"><span data-stu-id="147c3-138">Application Directory Partitions</span></span>](application-directory-partitions.md)
-   [<span data-ttu-id="147c3-139">Rilevamento della modalità operativa di un dominio</span><span class="sxs-lookup"><span data-stu-id="147c3-139">Detecting the Operation Mode of a Domain</span></span>](detecting-the-operation-mode-of-a-domain.md)

 

 
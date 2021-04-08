---
title: Servizi di dominio di Active Directory
description: Microsoft Active Directory Domain Services sono la base per le reti distribuite basate sui sistemi operativi Windows 2000 Server, Windows Server 2003 e Microsoft Windows Server 2008 che usano i controller di dominio.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory, pagina iniziale
- Active Directory Domain Services Active Directory, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047564"
---
# <a name="active-directory-domain-services"></a><span data-ttu-id="ef6a1-106">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ef6a1-106">Active Directory Domain Services</span></span>

## <a name="purpose"></a><span data-ttu-id="ef6a1-107">Scopo</span><span class="sxs-lookup"><span data-stu-id="ef6a1-107">Purpose</span></span>

<span data-ttu-id="ef6a1-108">Microsoft Active Directory Domain Services sono la base per le reti distribuite basate sui sistemi operativi Windows 2000 Server, Windows Server 2003 e Microsoft Windows Server 2008 che usano i controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-108">Microsoft Active Directory Domain Services are the foundation for distributed networks built on Windows 2000 Server, Windows Server 2003 and Microsoft Windows Server 2008 operating systems that use domain controllers.</span></span> <span data-ttu-id="ef6a1-109">Active Directory Domain Services offrono archiviazione dati gerarchica e sicura, strutturata, per gli oggetti in una rete, ad esempio utenti, computer, stampanti e servizi.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-109">Active Directory Domain Services provide secure, structured, hierarchical data storage for objects in a network such as users, computers, printers, and services.</span></span> <span data-ttu-id="ef6a1-110">Active Directory Domain Services fornire supporto per l'individuazione e l'utilizzo di questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-110">Active Directory Domain Services provide support for locating and working with these objects.</span></span>

<span data-ttu-id="ef6a1-111">Questa guida fornisce una panoramica dell'Active Directory Domain Services e del codice di esempio per le attività di base, ad esempio la ricerca di oggetti e la lettura delle proprietà, per attività più avanzate, ad esempio la pubblicazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-111">This guide provides an overview of Active Directory Domain Services and sample code for basic tasks, such as searching for objects and reading properties, to more advanced tasks such as service publication.</span></span>

<span data-ttu-id="ef6a1-112">Windows 2000 Server e i sistemi operativi successivi forniscono un'interfaccia utente che consente a utenti e amministratori di utilizzare gli oggetti e i dati in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-112">Windows 2000 Server and later operating systems provide a user interface for users and administrators to work with the objects and data in Active Directory Domain Services.</span></span> <span data-ttu-id="ef6a1-113">Questa guida descrive come estendere e personalizzare l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-113">This guide describes how to extend and customize that user interface.</span></span> <span data-ttu-id="ef6a1-114">Viene inoltre descritto come estendere Active Directory Domain Services definendo nuove classi di oggetti e attributi.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-114">It also describes how to extend Active Directory Domain Services by defining new object classes and attributes.</span></span>

> [!Note]  
> <span data-ttu-id="ef6a1-115">La documentazione seguente è destinata ai programmatori di computer.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-115">The following documentation is for computer programmers.</span></span> <span data-ttu-id="ef6a1-116">Se si è un utente finale che tenta di eseguire il debug di un errore di stampa o di una rete domestica, vedere i [Forum della community Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ef6a1-116">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="ef6a1-117">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="ef6a1-117">Where applicable</span></span>

<span data-ttu-id="ef6a1-118">Gli amministratori di rete scrivono gli script e le applicazioni che accedono Active Directory Domain Services per automatizzare le attività amministrative comuni, ad esempio l'aggiunta di utenti e gruppi, la gestione delle stampanti e l'impostazione delle autorizzazioni per le risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-118">Network administrators write scripts and applications that access Active Directory Domain Services to automate common administrative tasks, such as adding users and groups, managing printers, and setting permissions for network resources.</span></span>

<span data-ttu-id="ef6a1-119">I fornitori di software indipendenti e gli sviluppatori di utenti finali possono utilizzare la programmazione Active Directory Domain Services per abilitare la directory di prodotti e applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-119">Independent software vendors and end-user developers can use Active Directory Domain Services programming to directory-enable their products and applications.</span></span> <span data-ttu-id="ef6a1-120">I servizi possono essere pubblicati in Active Directory Domain Services; i client possono utilizzare Active Directory Domain Services per trovare i servizi ed entrambi possono utilizzare Active Directory Domain Services per individuare e utilizzare altri oggetti in una rete.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-120">Services can publish themselves in Active Directory Domain Services; clients can use Active Directory Domain Services to find services, and both can use Active Directory Domain Services to locate and work with other objects on a network.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ef6a1-121">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="ef6a1-121">Developer audience</span></span>

<span data-ttu-id="ef6a1-122">Le applicazioni che accedono ai dati in Active Directory Domain Services possono essere scritte usando l'API [interfacce del servizio Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , l'API [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) o lo spazio dei nomi [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="ef6a1-122">Applications that access data in Active Directory Domain Services can be written using the [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md) API, [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) API, or the [System.DirectoryServices](/dotnet/api/system.directoryservices) namespace.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ef6a1-123">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="ef6a1-123">Run-time requirements</span></span>

<span data-ttu-id="ef6a1-124">Active Directory Domain Services eseguiti nei controller di dominio Windows 2000 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-124">Active Directory Domain Services run on Windows 2000 and later domain controllers.</span></span> <span data-ttu-id="ef6a1-125">Tuttavia, le applicazioni client possono essere scritte ed eseguite in Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-125">However, client applications can be written for and run on Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef6a1-126">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ef6a1-126">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ef6a1-127">Informazioni su Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ef6a1-127">About Active Directory Domain Services</span></span>](about-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="ef6a1-128">Informazioni generali sulla Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-128">General information about Active Directory Domain Services.</span></span>

</dd> <dt>

[<span data-ttu-id="ef6a1-129">Uso di Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ef6a1-129">Using Active Directory Domain Services</span></span>](using-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="ef6a1-130">Guida alla programmazione Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-130">Active Directory Domain Services programming guide.</span></span>

</dd> <dt>

[<span data-ttu-id="ef6a1-131">Riferimento Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ef6a1-131">Active Directory Domain Services Reference</span></span>](active-directory-domain-services-reference.md)
</dt> <dd>

<span data-ttu-id="ef6a1-132">Riferimento alla programmazione Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ef6a1-132">Active Directory Domain Services programming reference.</span></span>

</dd> </dl>

 

 
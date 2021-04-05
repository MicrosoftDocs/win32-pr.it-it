---
title: Informazioni su Active Directory Domain Services
description: Questa guida fornisce informazioni essenziali per l'integrazione di Microsoft Active Directory in applicazioni distribuite progettate per sistemi operativi che supportano Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, informazioni
- Active Directory Domain Services Active Directory, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046788"
---
# <a name="about-active-directory-domain-services"></a><span data-ttu-id="aae01-105">Informazioni su Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="aae01-105">About Active Directory Domain Services</span></span>

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a><span data-ttu-id="aae01-106">Scrittura di applicazioni potenti che utilizzano Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="aae01-106">Writing Powerful Applications that Use Active Directory Domain Services</span></span>

<span data-ttu-id="aae01-107">Questa guida fornisce informazioni essenziali per l'integrazione di Active Directory Domain Services in applicazioni distribuite progettate per sistemi operativi che supportano Active Directory Domain Services, tra cui:</span><span class="sxs-lookup"><span data-stu-id="aae01-107">This guide provides essential information for integrating Active Directory Domain Services in distributed applications designed for operating systems that support Active Directory Domain Services, including:</span></span>

-   <span data-ttu-id="aae01-108">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aae01-108">Windows Server 2008</span></span>
-   <span data-ttu-id="aae01-109">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aae01-109">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="aae01-110">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aae01-110">Windows Server 2012</span></span>
-   <span data-ttu-id="aae01-111">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="aae01-111">Windows Server 2012 R2</span></span>
-   <span data-ttu-id="aae01-112">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aae01-112">Windows Server 2016</span></span>

> [!Note]  
> <span data-ttu-id="aae01-113">Questi argomenti sono destinati agli sviluppatori di software.</span><span class="sxs-lookup"><span data-stu-id="aae01-113">These topics are for software developers.</span></span> <span data-ttu-id="aae01-114">Per i problemi di supporto, vedere [supporto tecnico Microsoft](https://windows.microsoft.com/windows/support#1tc).</span><span class="sxs-lookup"><span data-stu-id="aae01-114">For support issues, see [Microsoft Support](https://windows.microsoft.com/windows/support#1tc).</span></span> <span data-ttu-id="aae01-115">Per informazioni sull'amministrazione di Active Directory, vedere [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) in TechNet.</span><span class="sxs-lookup"><span data-stu-id="aae01-115">For information about administering Active Directory, see [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) at TechNet.</span></span>

 

## <a name="fundamental-directory-features"></a><span data-ttu-id="aae01-116">Funzionalità di directory fondamentali</span><span class="sxs-lookup"><span data-stu-id="aae01-116">Fundamental Directory Features</span></span>

<span data-ttu-id="aae01-117">Un servizio directory è un servizio fondamentale per le applicazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="aae01-117">A directory service is a fundamental service for distributed applications.</span></span> <span data-ttu-id="aae01-118">Un servizio directory deve fornire le funzionalità elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="aae01-118">A directory service must provide the features listed in the following table.</span></span>



| <span data-ttu-id="aae01-119">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="aae01-119">Feature</span></span>               | <span data-ttu-id="aae01-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aae01-120">Description</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae01-121">Trasparenza della posizione</span><span class="sxs-lookup"><span data-stu-id="aae01-121">Location transparency</span></span> | <span data-ttu-id="aae01-122">È possibile trovare dati di utenti, gruppi, servizi di rete o risorse senza l'indirizzo dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="aae01-122">Able to find user, group, networked service, or resource, data without the object address</span></span>           |
| <span data-ttu-id="aae01-123">Dati di oggetti</span><span class="sxs-lookup"><span data-stu-id="aae01-123">Object data</span></span>           | <span data-ttu-id="aae01-124">In grado di archiviare dati utente, gruppo, organizzazione e servizio in un albero gerarchico</span><span class="sxs-lookup"><span data-stu-id="aae01-124">Able to store user, group, organization, and service data in a hierarchical tree</span></span>                    |
| <span data-ttu-id="aae01-125">Query avanzata</span><span class="sxs-lookup"><span data-stu-id="aae01-125">Rich query</span></span>            | <span data-ttu-id="aae01-126">In grado di individuare un oggetto eseguendo una query per le proprietà dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="aae01-126">Able to locate an object by querying for object properties</span></span>                                          |
| <span data-ttu-id="aae01-127">Disponibilità elevata</span><span class="sxs-lookup"><span data-stu-id="aae01-127">High availability</span></span>     | <span data-ttu-id="aae01-128">In grado di individuare una replica della directory in una posizione efficiente per le operazioni di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="aae01-128">Able to locate a replica of the directory at a location that is efficient for read/write operations</span></span> |



 

## <a name="advanced-features-of-active-directory-domain-services"></a><span data-ttu-id="aae01-129">Funzionalità avanzate di Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="aae01-129">Advanced Features of Active Directory Domain Services</span></span>

<span data-ttu-id="aae01-130">Active Directory Domain Services fornisce le funzionalità elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="aae01-130">Active Directory Domain Services provides the features listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aae01-131">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="aae01-131">Feature</span></span></th>
<th><span data-ttu-id="aae01-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aae01-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aae01-133">Supporto per gli standard Internet</span><span class="sxs-lookup"><span data-stu-id="aae01-133">Support for Internet standards</span></span></td>
<td><span data-ttu-id="aae01-134">Active Directory Domain Services implementa le funzionalità in base agli standard Internet pubblicati, ad esempio LDAP e DNS.</span><span class="sxs-lookup"><span data-stu-id="aae01-134">Active Directory Domain Services implements its features in accordance with published Internet standards such as LDAP and DNS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aae01-135">Sicurezza strettamente integrata e flessibile</span><span class="sxs-lookup"><span data-stu-id="aae01-135">Tightly integrated and flexible security</span></span></td>
<td><span data-ttu-id="aae01-136">Alcuni vantaggi:</span><span class="sxs-lookup"><span data-stu-id="aae01-136">Advantages include:</span></span><br/>
<ul>
<li><span data-ttu-id="aae01-137">Scelta dei pacchetti di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="aae01-137">Choice of authentication packages.</span></span> <span data-ttu-id="aae01-138">Kerberos, Secure Sockets Layer (SSL) o una combinazione; ad esempio, stabilire un canale SSL per la crittografia e quindi usare Kerberos per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="aae01-138">Kerberos, Secure Sockets Layer (SSL), or a combination; for example, establish an SSL channel for encryption and then use Kerberos for authentication.</span></span></li>
<li><span data-ttu-id="aae01-139">Gestione centralizzata dell'accesso al servizio e alle risorse tramite utenti e gruppi in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="aae01-139">Central management of service and resource access by using the users and groups in Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="aae01-140">Delega dell'amministrazione in modo che gli amministratori centrali possano delegare attività amministrative quali la modifica della password o la creazione e l'eliminazione di oggetti specifici.</span><span class="sxs-lookup"><span data-stu-id="aae01-140">Delegation of administration so that central administrators can delegate administrative tasks such as password changing or specific object creation and deletion.</span></span></li>
<li><span data-ttu-id="aae01-141">Il server Active Directory utilizza gli stessi meccanismi di controllo degli accessi utilizzati nei file System nei sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="aae01-141">The Active Directory server uses the same access control mechanisms used on file systems in the Windows operating systems.</span></span> <span data-ttu-id="aae01-142">Di conseguenza, gli stessi strumenti che gestiscono il controllo di accesso su un file system funzionano per Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="aae01-142">Thus, the same tools that manage access control on a file system work for Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="aae01-143">Infrastruttura a chiave pubblica completa.</span><span class="sxs-lookup"><span data-stu-id="aae01-143">Comprehensive Public Key infrastructure.</span></span> <span data-ttu-id="aae01-144">Il supporto per le smart card e il server dei certificati Microsoft è integrato con Active Directory Domain Services per fornire l'accesso con smart card e la gestione dei certificati.</span><span class="sxs-lookup"><span data-stu-id="aae01-144">The Microsoft Certificate Server and Smart Card support are integrated with Active Directory Domain Services to provide Smart Card logon and Certificate management.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aae01-145">Facilmente programmabile</span><span class="sxs-lookup"><span data-stu-id="aae01-145">Easily programmable</span></span></td>
<td><span data-ttu-id="aae01-146">È possibile accedere a livello di codice e amministrare il server Active Directory usando l'API <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">interfacce del servizio Active Directory</a> , l'API <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> o lo spazio dei nomi <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</span><span class="sxs-lookup"><span data-stu-id="aae01-146">The Active Directory server can be programmatically accessed and administered using the <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Service Interfaces</a> API, <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> API, or the <a href="/dotnet/api/system.directoryservices">System.DirectoryServices</a> namespace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aae01-147">Servizi di sistema abilitati per la directory</span><span class="sxs-lookup"><span data-stu-id="aae01-147">Directory enabled system services</span></span></td>
<td><span data-ttu-id="aae01-148">L'applicazione client può essere facilmente distribuita nei desktop distribuiti creando un pacchetto di Windows Installer e utilizzando la funzionalità di distribuzione delle applicazioni disponibile nei sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="aae01-148">Your client application can be easily deployed to distributed desktops by creating a Windows Installer package and using the application deployment feature available in the Windows operating systems.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aae01-149">Integrazione di applicazioni chiave</span><span class="sxs-lookup"><span data-stu-id="aae01-149">Key application integration</span></span></td>
<td><span data-ttu-id="aae01-150">Le applicazioni distribuite principali, ad esempio Exchange, sono integrate con Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="aae01-150">Key distributed applications, such as Exchange, are integrated with Active Directory Domain Services.</span></span> <span data-ttu-id="aae01-151">In questo modo, le aziende possono ridurre il numero di servizi directory da gestire.</span><span class="sxs-lookup"><span data-stu-id="aae01-151">Thus, companies can reduce the number of directory services to be managed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aae01-152">Schema completo ed estendibile</span><span class="sxs-lookup"><span data-stu-id="aae01-152">Rich and extensible schema</span></span></td>
<td><span data-ttu-id="aae01-153">Lo schema definisce gli oggetti e le proprietà che possono essere scritti e letti da un servizio directory.</span><span class="sxs-lookup"><span data-stu-id="aae01-153">The schema defines what objects and properties can be written and read from a directory service.</span></span> <span data-ttu-id="aae01-154">Lo schema Active Directory è ricco.</span><span class="sxs-lookup"><span data-stu-id="aae01-154">The Active Directory Schema is rich.</span></span> <span data-ttu-id="aae01-155">La maggior parte degli oggetti e delle proprietà richiesti da un servizio sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="aae01-155">Most of the objects and properties a service requires are available.</span></span> <span data-ttu-id="aae01-156">In caso contrario, un'applicazione distribuita può estendere lo schema per supportare i requisiti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aae01-156">If not, a distributed application can extend the schema to support the application requirements.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="aae01-157">Per ulteriori informazioni su Active Directory Domain Services, vedere:</span><span class="sxs-lookup"><span data-stu-id="aae01-157">For more information about Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="aae01-158">Concetti di base di Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="aae01-158">Core Concepts of Active Directory Domain Services</span></span>](core-concepts-of-active-directory-domain-services.md)
-   [<span data-ttu-id="aae01-159">Architettura Active Directory</span><span class="sxs-lookup"><span data-stu-id="aae01-159">Active Directory Architecture</span></span>](active-directory-domain-services-architecture.md)
-   [<span data-ttu-id="aae01-160">Schema Active Directory</span><span class="sxs-lookup"><span data-stu-id="aae01-160">Active Directory Schema</span></span>](active-directory-schema.md)


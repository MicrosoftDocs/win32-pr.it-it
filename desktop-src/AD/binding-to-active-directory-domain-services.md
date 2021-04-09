---
title: Binding a Active Directory Domain Services
description: In Active Directory Domain Services, l'operazione di associazione di un oggetto programmatico a un oggetto Active Directory Domain Services specifico è nota come binding.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- associazione a Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, associazione a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965963"
---
# <a name="binding-to-active-directory-domain-services"></a><span data-ttu-id="a8171-105">Binding a Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="a8171-105">Binding to Active Directory Domain Services</span></span>

<span data-ttu-id="a8171-106">In Active Directory Domain Services, l'operazione di associazione di un oggetto programmatico a un oggetto Active Directory Domain Services specifico è nota come *Binding*.</span><span class="sxs-lookup"><span data-stu-id="a8171-106">In Active Directory Domain Services, the act of associating a programmatic object with a specific Active Directory Domain Services object is known as *binding*.</span></span> <span data-ttu-id="a8171-107">Quando un oggetto a livello di codice, ad esempio un oggetto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , è associato a un oggetto directory specifico, l'oggetto programmatico viene considerato *associato* all'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="a8171-107">When a programmatic object, such as an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) object, is associated with a specific directory object, the programmatic object is considered to be *bound to* the directory object.</span></span>

## <a name="binding-functions-and-methods"></a><span data-ttu-id="a8171-108">Funzioni e metodi di associazione</span><span class="sxs-lookup"><span data-stu-id="a8171-108">Binding Functions and Methods</span></span>

<span data-ttu-id="a8171-109">Il metodo per l'associazione a livello di codice a un oggetto Active Directory dipenderà dalla tecnologia di programmazione utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a8171-109">The method for programmatically binding to an Active Directory object will depend on the programming technology that is used.</span></span> <span data-ttu-id="a8171-110">Per ulteriori informazioni sull'associazione a oggetti in Active Directory Domain Services con una tecnologia di programmazione specifica, vedere gli argomenti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a8171-110">For more information about binding to objects in Active Directory Domain Services with a specific programming technology, see the topics listed in the following table.</span></span>



| <span data-ttu-id="a8171-111">Tecnologia di programmazione</span><span class="sxs-lookup"><span data-stu-id="a8171-111">Programming technology</span></span>                                                                       | <span data-ttu-id="a8171-112">Per ulteriori informazioni</span><span class="sxs-lookup"><span data-stu-id="a8171-112">For more information</span></span>                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="a8171-113">Interfacce di servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="a8171-113">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="a8171-114">Associazione a un oggetto ADSI</span><span class="sxs-lookup"><span data-stu-id="a8171-114">Binding to an ADSI Object</span></span>](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [<span data-ttu-id="a8171-115">Lightweight Directory Access Protocol</span><span class="sxs-lookup"><span data-stu-id="a8171-115">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="a8171-116">Creazione di una sessione LDAP</span><span class="sxs-lookup"><span data-stu-id="a8171-116">Establishing an LDAP Session</span></span>](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [<span data-ttu-id="a8171-117">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="a8171-117">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)                 | <span data-ttu-id="a8171-118">[Associazione a oggetti directory](/previous-versions/ms180840(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="a8171-118">[Binding to Directory Objects](/previous-versions/ms180840(v=vs.90))</span></span> |



 

## <a name="binding-strings"></a><span data-ttu-id="a8171-119">Binding di stringhe</span><span class="sxs-lookup"><span data-stu-id="a8171-119">Binding Strings</span></span>

<span data-ttu-id="a8171-120">Tutte le funzioni e i metodi di associazione richiedono una stringa di associazione.</span><span class="sxs-lookup"><span data-stu-id="a8171-120">All bind functions and methods require a binding string.</span></span> <span data-ttu-id="a8171-121">Il formato della stringa di associazione dipende dal provider.</span><span class="sxs-lookup"><span data-stu-id="a8171-121">The form of the binding string depends on the provider.</span></span> <span data-ttu-id="a8171-122">Active Directory Domain Services sono supportati da due provider, LDAP e WinNT.</span><span class="sxs-lookup"><span data-stu-id="a8171-122">Active Directory Domain Services are supported by two providers, LDAP and WinNT.</span></span>

<span data-ttu-id="a8171-123">A partire da Windows 2000, il provider LDAP viene usato per accedere Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a8171-123">Beginning with Windows 2000, the LDAP provider is used to access Active Directory Domain Services.</span></span> <span data-ttu-id="a8171-124">La stringa di binding LDAP può assumere uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="a8171-124">The LDAP binding string can take one of the following forms:</span></span>

-   <span data-ttu-id="a8171-125">"LDAP:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="a8171-125">"LDAP://<host name>/<object name>"</span></span>
-   <span data-ttu-id="a8171-126">"GC:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="a8171-126">"GC://<host name>/<object name>"</span></span>

<span data-ttu-id="a8171-127">Negli esempi precedenti, "LDAP:" specifica il provider LDAP.</span><span class="sxs-lookup"><span data-stu-id="a8171-127">In the examples above, "LDAP:" specifies the LDAP provider.</span></span> <span data-ttu-id="a8171-128">"GC:" utilizza il provider LDAP per l'associazione al servizio di catalogo globale per eseguire query veloci.</span><span class="sxs-lookup"><span data-stu-id="a8171-128">"GC:" uses the LDAP provider to bind to the Global Catalog service to execute fast queries.</span></span>

<span data-ttu-id="a8171-129">" &lt; nome host &gt; " specifica il server a cui eseguire il binding ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a8171-129">"&lt;host name&gt;" specifies the server to bind to and is optional.</span></span> <span data-ttu-id="a8171-130">Se possibile, non specificare un server.</span><span class="sxs-lookup"><span data-stu-id="a8171-130">If possible, do not specify a server.</span></span> <span data-ttu-id="a8171-131">È anche possibile eseguire l'associazione a un oggetto in un dominio diverso.</span><span class="sxs-lookup"><span data-stu-id="a8171-131">It is also possible to bind to an object in a different domain.</span></span> <span data-ttu-id="a8171-132">A tale scopo, passare il nome DNS (Domain Naming System) del dominio di destinazione per " &lt; host name &gt; ".</span><span class="sxs-lookup"><span data-stu-id="a8171-132">To do this pass the domain naming system (DNS) name of the target domain for "&lt;host name&gt;".</span></span> <span data-ttu-id="a8171-133">Ad esempio, per eseguire l'associazione al contenitore Users nel dominio domain2 di fabrikam.com, la stringa di associazione sarà "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span><span class="sxs-lookup"><span data-stu-id="a8171-133">For example, to bind to the Users container in the domain2 domain of fabrikam.com, the binding string would be "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span></span>

<span data-ttu-id="a8171-134">" &lt; nome oggetto &gt; " rappresenta un oggetto specifico in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a8171-134">"&lt;object name&gt;" represents a specific object in Active Directory Domain Services.</span></span> <span data-ttu-id="a8171-135">Il nome dell'oggetto può essere un nome distinto o un GUID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a8171-135">The object name can be a distinguished name or an object GUID.</span></span>

<span data-ttu-id="a8171-136">Per ulteriori informazioni sulle stringhe di binding LDAP, vedere [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span><span class="sxs-lookup"><span data-stu-id="a8171-136">For more information about LDAP binding strings, see [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span></span>

<span data-ttu-id="a8171-137">Per Windows NT 4,0, il provider WinNT viene usato per l'accesso ai dati della directory, ad esempio utenti, gruppi di utenti, computer, servizi e altri oggetti di rete in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a8171-137">For Windows NT 4.0, the WinNT provider is used for access to directory data such as users, user groups, computers, services, and other network objects in the Windows 2000.</span></span> <span data-ttu-id="a8171-138">Il provider WinNT nei sistemi Windows 2000 e versioni successive presenta funzionalità limitate rispetto al provider LDAP.</span><span class="sxs-lookup"><span data-stu-id="a8171-138">The WinNT provider on Windows 2000 and later systems has limited functionality compared to the LDAP provider.</span></span> <span data-ttu-id="a8171-139">Per ulteriori informazioni sulle stringhe di binding WinNT, vedere [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span><span class="sxs-lookup"><span data-stu-id="a8171-139">For more information about WinNT binding strings, see [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span></span>

<span data-ttu-id="a8171-140">Per eseguire il binding alla radice dello spazio dei nomi, è possibile usare un ADsPath di "LDAP://" o "GC://".</span><span class="sxs-lookup"><span data-stu-id="a8171-140">An ADsPath of "LDAP://" or "GC://" can be used to bind to the root of the namespace.</span></span> <span data-ttu-id="a8171-141">Quando viene associato alla radice dello spazio dei nomi, l'oggetto spazio dei nomi fornito non contiene proprietà e contiene l'oggetto dominio per LDAP e un oggetto contenitore contenente una replica parziale di tutti i domini nella foresta per GC.</span><span class="sxs-lookup"><span data-stu-id="a8171-141">When bound to the root of the namespace, the supplied namespace object contains no properties and contains the domain object for LDAP and a container object containing a partial replica of all domains in the forest for GC.</span></span>

<span data-ttu-id="a8171-142">Per ulteriori informazioni sull'associazione in Active Directory Domain Services, vedere:</span><span class="sxs-lookup"><span data-stu-id="a8171-142">For more information about binding in Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="a8171-143">Binding senza server e RootDSE</span><span class="sxs-lookup"><span data-stu-id="a8171-143">Serverless Binding and RootDSE</span></span>](serverless-binding-and-rootdse.md)
-   [<span data-ttu-id="a8171-144">Associazione al catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a8171-144">Binding to the Global Catalog</span></span>](binding-to-the-global-catalog.md)
-   [<span data-ttu-id="a8171-145">Utilizzo di objectGUID per l'associazione a un oggetto</span><span class="sxs-lookup"><span data-stu-id="a8171-145">Using objectGUID to Bind to an Object</span></span>](using-objectguid-to-bind-to-an-object.md)
-   [<span data-ttu-id="a8171-146">Associazione a oggetti Well-Known mediante WKGUID</span><span class="sxs-lookup"><span data-stu-id="a8171-146">Binding to Well-Known Objects Using WKGUID</span></span>](binding-to-well-known-objects-using-wkguid.md)
-   [<span data-ttu-id="a8171-147">Associazione a un oggetto tramite un SID</span><span class="sxs-lookup"><span data-stu-id="a8171-147">Binding to an Object Using a SID</span></span>](binding-to-an-object-using-a-sid.md)
-   [<span data-ttu-id="a8171-148">Abilitazione di Rename-Safe binding con la proprietà otherWellKnownObjects archiviato nel</span><span class="sxs-lookup"><span data-stu-id="a8171-148">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [<span data-ttu-id="a8171-149">autenticazione</span><span class="sxs-lookup"><span data-stu-id="a8171-149">Authentication</span></span>](authentication.md)

 

 

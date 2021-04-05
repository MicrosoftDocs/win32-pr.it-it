---
title: Associazione a oggetti Well-Known mediante WKGUID
description: In questo argomento viene illustrato come eseguire l'associazione a oggetti utilizzando la stringa di associazione WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Associazione a oggetti Well-Known con WKGUID AD
- Active Directory, utilizzo di, associazione, utilizzo di WKGUID per l'associazione a oggetti noti
- oggetti noti AD
- oggetti noti AD, associazione all'uso di WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724647"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a><span data-ttu-id="78d6b-107">Associazione a oggetti Well-Known mediante WKGUID</span><span class="sxs-lookup"><span data-stu-id="78d6b-107">Binding to Well-Known Objects Using WKGUID</span></span>

<span data-ttu-id="78d6b-108">I contenitori possono avere uno o più oggetti importanti che possono essere rinominati o spostati.</span><span class="sxs-lookup"><span data-stu-id="78d6b-108">Containers can have one, or more, important subobjects that can be renamed or moved.</span></span> <span data-ttu-id="78d6b-109">Può essere difficile tenere traccia di questi oggetti e compilare stringhe di binding corrette, soprattutto se vengono rinominati o spostati.</span><span class="sxs-lookup"><span data-stu-id="78d6b-109">It can be difficult to track these subobjects and build correct binding strings for them, especially if they are renamed or moved.</span></span>

<span data-ttu-id="78d6b-110">Per supportare l'associazione Rinomina-safe a questi oggetti all'interno di questi contenitori, Active Directory Domain Services hanno due attributi: **wellKnownObjects** e **otherWellKnownObjects archiviato nel**.</span><span class="sxs-lookup"><span data-stu-id="78d6b-110">To support rename-safe binding to these objects within these containers, Active Directory Domain Services have two attributes: **wellKnownObjects** and **otherWellKnownObjects**.</span></span> <span data-ttu-id="78d6b-111">Questi attributi hanno una sintassi di attributo ADSTYPE \_ DN \_ con \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="78d6b-111">These attributes have an attribute syntax of ADSTYPE\_DN\_WITH\_BINARY.</span></span> <span data-ttu-id="78d6b-112">Consentono più valori e contengono tuple GUID/DN di oggetti noti all'interno dei contenitori sui quali sono impostati.</span><span class="sxs-lookup"><span data-stu-id="78d6b-112">They allow multiple values and contain the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="78d6b-113">Il server Active Directory gestisce la parte del nome distinto di ogni voce **wellKnownObjects** e **otherWellKnownObjects archiviato nel** in modo che contenga il nome distinto corrente dell'oggetto specificato al momento della creazione della voce.</span><span class="sxs-lookup"><span data-stu-id="78d6b-113">The Active Directory server maintains the distinguished name portion of each **wellKnownObjects** and **otherWellKnownObjects** entry so that it contains the current distinguished name of the object specified when the entry was created.</span></span>

<span data-ttu-id="78d6b-114">È possibile impostare e usare la proprietà **otherWellKnownObjects archiviato nel** in qualsiasi oggetto.</span><span class="sxs-lookup"><span data-stu-id="78d6b-114">The **otherWellKnownObjects** property can be set and used on any object.</span></span>

<span data-ttu-id="78d6b-115">La proprietà **wellKnownObjects** viene usata nei contenitori domainDNS e Configuration.</span><span class="sxs-lookup"><span data-stu-id="78d6b-115">The **wellKnownObjects** property is used on the domainDNS and configuration containers.</span></span> <span data-ttu-id="78d6b-116">La proprietà **wellKnownObjects** è una proprietà solo di sistema e può essere modificata solo dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="78d6b-116">The **wellKnownObjects** property is a system-only property and can only be modified by the operating system.</span></span>

<span data-ttu-id="78d6b-117">Il contenitore **domainDNS** dispone dei seguenti oggetti noti:</span><span class="sxs-lookup"><span data-stu-id="78d6b-117">The **domainDNS** container has the following well-known objects:</span></span>

-   <span data-ttu-id="78d6b-118">Utenti</span><span class="sxs-lookup"><span data-stu-id="78d6b-118">Users</span></span>
-   <span data-ttu-id="78d6b-119">Computers (Computer)</span><span class="sxs-lookup"><span data-stu-id="78d6b-119">Computers</span></span>
-   <span data-ttu-id="78d6b-120">Sistema</span><span class="sxs-lookup"><span data-stu-id="78d6b-120">System</span></span>
-   <span data-ttu-id="78d6b-121">Controller di dominio</span><span class="sxs-lookup"><span data-stu-id="78d6b-121">Domain Controllers</span></span>
-   <span data-ttu-id="78d6b-122">Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="78d6b-122">Infrastructure</span></span>
-   <span data-ttu-id="78d6b-123">Oggetti eliminati</span><span class="sxs-lookup"><span data-stu-id="78d6b-123">Deleted Objects</span></span>
-   <span data-ttu-id="78d6b-124">Perso e trovato</span><span class="sxs-lookup"><span data-stu-id="78d6b-124">Lost and Found</span></span>

<span data-ttu-id="78d6b-125">Il contenitore di configurazione dispone degli oggetti noti: Deleted Objects.</span><span class="sxs-lookup"><span data-stu-id="78d6b-125">The configuration container has the well-known object: Deleted Objects.</span></span>

<span data-ttu-id="78d6b-126">Questi oggetti si trovano in ogni contenitore di **domainDNS** e configurazione in un servizio dominio di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78d6b-126">These objects are in every **domainDNS** and configuration container in an Active Directory Domain Service.</span></span>

<span data-ttu-id="78d6b-127">È possibile eseguire il binding a un oggetto noto usando il formato di associazione WKGUID.</span><span class="sxs-lookup"><span data-stu-id="78d6b-127">You can bind to a well-known object using the WKGUID binding format.</span></span> <span data-ttu-id="78d6b-128">Il binding con WKGUID è supportato solo in Active Directory Domain Services, ovvero il provider LDAP.</span><span class="sxs-lookup"><span data-stu-id="78d6b-128">Binding with WKGUID is only supported in Active Directory Domain Services, that is, the LDAP provider.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78d6b-129">Usare sempre il formato di associazione WKGUID per eseguire l'associazione agli oggetti noti, come elencato in precedenza, nei contenitori di dominio e configurazione.</span><span class="sxs-lookup"><span data-stu-id="78d6b-129">Always use the WKGUID binding format to bind to the well-known objects, as listed above, in the domain and configuration containers.</span></span> <span data-ttu-id="78d6b-130">In questo modo si garantisce che questi contenitori possano essere associati a anche se vengono spostati o rinominati.</span><span class="sxs-lookup"><span data-stu-id="78d6b-130">This ensures that these containers can be bound to even if they are moved or renamed.</span></span>

 

<span data-ttu-id="78d6b-131">Il formato della stringa di binding WKGUID è il seguente:</span><span class="sxs-lookup"><span data-stu-id="78d6b-131">The WKGUID binding string format is as follows:</span></span>


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



<span data-ttu-id="78d6b-132">" &lt; nome server &gt; " è il nome del server di directory.</span><span class="sxs-lookup"><span data-stu-id="78d6b-132">"&lt;server name&gt;" is the directory server name.</span></span> <span data-ttu-id="78d6b-133">Il &lt; nome del server &gt; è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="78d6b-133">The "&lt;server name&gt;" is optional.</span></span>

<span data-ttu-id="78d6b-134">" &lt; Xxxxx &gt; " è la rappresentazione di stringa del valore esadecimale del GUID che rappresenta l'oggetto noto.</span><span class="sxs-lookup"><span data-stu-id="78d6b-134">"&lt;XXXXX&gt;" is the string representation of the hexadecimal value of the GUID that represents the well-known object.</span></span> <span data-ttu-id="78d6b-135">La stringa GUID viene specificata nel form "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" e non ha lo stesso formato della stringa GUID prodotta dalla funzione [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , che assume il formato "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span><span class="sxs-lookup"><span data-stu-id="78d6b-135">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form and is not the same form as the GUID string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, which takes the form "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span></span> <span data-ttu-id="78d6b-136">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come creare una stringa associabile da un GUID, vedere [codice di esempio per la creazione di una rappresentazione di stringa associabile di un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="78d6b-136">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span>

<span data-ttu-id="78d6b-137">Per eseguire l'associazione a un oggetto specificato in **otherWellKnownObjects archiviato nel** in un oggetto, specificare " &lt; xxxxx &gt; " come formato stringa di binding del GUID dell'oggetto noto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="78d6b-137">To bind to an object specified in **otherWellKnownObjects** in an object, specify "&lt;XXXXX&gt;" as the bind string form of the well-known object GUID of the object.</span></span> <span data-ttu-id="78d6b-138">Per altre informazioni, vedere [lettura di objectGUID di un oggetto e creazione di una rappresentazione di stringa del GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span><span class="sxs-lookup"><span data-stu-id="78d6b-138">For more information, see [Reading an Object's objectGUID and Creating a String Representation of the GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span></span> <span data-ttu-id="78d6b-139">Per ulteriori informazioni sull'impostazione della proprietà **otherWellKnownObjects archiviato nel** sugli oggetti, vedere [Abilitazione dell'associazione Rename-Safe con la proprietà otherWellKnownObjects archiviato nel](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span><span class="sxs-lookup"><span data-stu-id="78d6b-139">For more information about setting the **otherWellKnownObjects** property on objects, see [Enabling Rename-Safe Binding with the otherWellKnownObjects Property](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span></span>

<span data-ttu-id="78d6b-140">Per eseguire l'associazione a un oggetto specificato in **wellKnownObjects** in domainDNS o nei contenitori di configurazione, specificare " &lt; xxxxx &gt; " come una delle seguenti costanti, elencate nella tabella seguente, come definito in ntdsapi. h.</span><span class="sxs-lookup"><span data-stu-id="78d6b-140">To bind to an object specified in **wellKnownObjects** in domainDNS or configuration containers, specify "&lt;XXXXX&gt;" as one of the following constants, listed in the following table, as defined in Ntdsapi.h.</span></span>



| <span data-ttu-id="78d6b-141">Contenitore</span><span class="sxs-lookup"><span data-stu-id="78d6b-141">Container</span></span>          | <span data-ttu-id="78d6b-142">Identificatore GUID</span><span class="sxs-lookup"><span data-stu-id="78d6b-142">GUID Identifier</span></span>                         |
|--------------------|-----------------------------------------|
| <span data-ttu-id="78d6b-143">Utenti</span><span class="sxs-lookup"><span data-stu-id="78d6b-143">Users</span></span>              | <span data-ttu-id="78d6b-144">\_contenitore utenti \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="78d6b-144">GUID\_USERS\_CONTAINER\_W</span></span>               |
| <span data-ttu-id="78d6b-145">Computers (Computer)</span><span class="sxs-lookup"><span data-stu-id="78d6b-145">Computers</span></span>          | <span data-ttu-id="78d6b-146">\_contenitore di calcolo \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="78d6b-146">GUID\_COMPUTRS\_CONTAINER\_W</span></span>            |
| <span data-ttu-id="78d6b-147">Sistema</span><span class="sxs-lookup"><span data-stu-id="78d6b-147">System</span></span>             | <span data-ttu-id="78d6b-148">\_contenitore di sistemi GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="78d6b-148">GUID\_SYSTEMS\_CONTAINER\_W</span></span>             |
| <span data-ttu-id="78d6b-149">Controller di dominio</span><span class="sxs-lookup"><span data-stu-id="78d6b-149">Domain Controllers</span></span> | <span data-ttu-id="78d6b-150">\_contenitore controller di dominio GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="78d6b-150">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span> |
| <span data-ttu-id="78d6b-151">Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="78d6b-151">Infrastructure</span></span>     | <span data-ttu-id="78d6b-152">\_contenitore infrastruttura \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="78d6b-152">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>      |
| <span data-ttu-id="78d6b-153">Oggetti eliminati</span><span class="sxs-lookup"><span data-stu-id="78d6b-153">Deleted Objects</span></span>    | <span data-ttu-id="78d6b-154">\_ \_ contenitore oggetti eliminati \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="78d6b-154">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>    |
| <span data-ttu-id="78d6b-155">Perso e trovato</span><span class="sxs-lookup"><span data-stu-id="78d6b-155">Lost and Found</span></span>     | <span data-ttu-id="78d6b-156">GUID \_ LOSTANDFOUND \_ contenitore \_ W</span><span class="sxs-lookup"><span data-stu-id="78d6b-156">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>        |



 

<span data-ttu-id="78d6b-157">Ad esempio, per eseguire l'associazione al contenitore utente in un dominio, specificare **GUID \_ Users \_ Container \_ W** come " &lt; xxxxx &gt; ".</span><span class="sxs-lookup"><span data-stu-id="78d6b-157">For example, to bind to the user container in a domain, specify **GUID\_USERS\_CONTAINER\_W** as "&lt;XXXXX&gt;".</span></span>

<span data-ttu-id="78d6b-158">" &lt; contenitore DN &gt; " è il nome distinto dell'oggetto contenitore con questo oggetto rappresentato come valore nella relativa proprietà **wellKnownObjects** .</span><span class="sxs-lookup"><span data-stu-id="78d6b-158">"&lt;container DN&gt;" is the distinguished name of the container object that has this object represented as a value in its **wellKnownObjects** property.</span></span> <span data-ttu-id="78d6b-159">Ad esempio, per eseguire l'associazione al contenitore degli utenti in un dominio, specificare il nome distinto del dominio come " &lt; DN del contenitore &gt; ".</span><span class="sxs-lookup"><span data-stu-id="78d6b-159">For example, to bind to the users container in a domain, specify the domain distinguished name as the "&lt;container DN&gt;".</span></span>

<span data-ttu-id="78d6b-160">Ad esempio, per eseguire l'associazione al contenitore Users del dominio Fabrikam.com, usare la stringa di binding seguente.</span><span class="sxs-lookup"><span data-stu-id="78d6b-160">For example, to bind to the users container of the domain Fabrikam.com, use the following binding string.</span></span>

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

<span data-ttu-id="78d6b-161">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire l'associazione a un GUID noto, vedere il [codice di esempio per l'associazione a oggetti noti](example-code-for-binding-to-well-known-objects.md).</span><span class="sxs-lookup"><span data-stu-id="78d6b-161">For more information and a code example that shows how to bind to a well-known GUID, see [Example Code for Binding to Well Known Objects](example-code-for-binding-to-well-known-objects.md).</span></span>

 

 
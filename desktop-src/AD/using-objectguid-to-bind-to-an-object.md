---
title: Utilizzo di objectGUID per l'associazione a un oggetto
description: Il nome distinto di un oggetto viene modificato se l'oggetto viene rinominato o spostato, pertanto il nome distinto non è un identificatore di oggetto affidabile.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Utilizzo di objectGUID per l'associazione a un oggetto AD
- objectGUID AD
- objectGUID AD, utilizzo di per l'associazione a un oggetto
- Active Directory, utilizzo di, associazione, utilizzo di objectGUID per l'associazione all'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046477"
---
# <a name="using-objectguid-to-bind-to-an-object"></a><span data-ttu-id="d2e50-107">Utilizzo di objectGUID per l'associazione a un oggetto</span><span class="sxs-lookup"><span data-stu-id="d2e50-107">Using objectGUID to Bind to an Object</span></span>

<span data-ttu-id="d2e50-108">Il nome distinto di un oggetto viene modificato se l'oggetto viene rinominato o spostato, pertanto il nome distinto non è un identificatore di oggetto affidabile.</span><span class="sxs-lookup"><span data-stu-id="d2e50-108">An object distinguished name changes if the object is renamed or moved, therefore the distinguished name is not a reliable object identifier.</span></span> <span data-ttu-id="d2e50-109">In Active Directory Domain Services la proprietà **objectGUID** di un oggetto non cambia mai, anche se l'oggetto è stato rinominato o spostato.</span><span class="sxs-lookup"><span data-stu-id="d2e50-109">In Active Directory Domain Services, an object's **objectGUID** property never changes, even if the object is renamed or moved.</span></span> <span data-ttu-id="d2e50-110">Per ulteriori informazioni su **objectGUID** e sugli identificatori, vedere [nomi e identità degli oggetti](object-names-and-identities.md).</span><span class="sxs-lookup"><span data-stu-id="d2e50-110">For more information about **objectGUID** and identifiers, see [Object Names and Identities](object-names-and-identities.md).</span></span>

<span data-ttu-id="d2e50-111">Il provider LDAP Active Directory fornisce un metodo per l'associazione a un oggetto mediante il GUID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2e50-111">The Active Directory LDAP provider provides a method to bind to an object using the object GUID.</span></span> <span data-ttu-id="d2e50-112">Il formato della stringa di binding è il seguente:</span><span class="sxs-lookup"><span data-stu-id="d2e50-112">The binding string format is as follows:</span></span>


```C++
LDAP://servername/<GUID=XXXXX>
```



<span data-ttu-id="d2e50-113">In questo esempio "ServerName" è il nome del server di directory e "XXXXX" è la rappresentazione di stringa del valore esadecimale del GUID.</span><span class="sxs-lookup"><span data-stu-id="d2e50-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the GUID.</span></span> <span data-ttu-id="d2e50-114">"ServerName" è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d2e50-114">The "servername" is optional.</span></span> <span data-ttu-id="d2e50-115">La stringa GUID viene specificata nel form "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX".</span><span class="sxs-lookup"><span data-stu-id="d2e50-115">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form.</span></span> <span data-ttu-id="d2e50-116">La stringa GUID può inoltre assumere il formato "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", che è lo stesso formato della stringa prodotta dalla funzione [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , senza le parentesi graffe circostanti " {} ".</span><span class="sxs-lookup"><span data-stu-id="d2e50-116">The GUID string can also take the form "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", which is the same form as the string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, without the surrounding braces "{}".</span></span> <span data-ttu-id="d2e50-117">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come creare una stringa associabile da un GUID, vedere [codice di esempio per la creazione di una rappresentazione di stringa associabile di un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="d2e50-117">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span> <span data-ttu-id="d2e50-118">È possibile utilizzare la proprietà [**IADs. Guid**](/windows/desktop/ADSI/iads-property-methods) per recuperare il formato stringa corretto del GUID.</span><span class="sxs-lookup"><span data-stu-id="d2e50-118">The [**IADs.GUID**](/windows/desktop/ADSI/iads-property-methods) property can be used to retrieve the proper string form of the GUID.</span></span>

<span data-ttu-id="d2e50-119">Quando si esegue l'associazione con il GUID dell'oggetto, alcuni metodi e proprietà [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="d2e50-119">When binding using the object GUID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="d2e50-120">Le proprietà **IADs** seguenti non sono supportate dagli oggetti ottenuti tramite binding mediante il GUID dell'oggetto:</span><span class="sxs-lookup"><span data-stu-id="d2e50-120">The following **IADs** properties are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="d2e50-121">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="d2e50-121">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="d2e50-122">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d2e50-122">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="d2e50-123">**Padre**</span><span class="sxs-lookup"><span data-stu-id="d2e50-123">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="d2e50-124">I metodi **IADsContainer** seguenti non sono supportati dagli oggetti ottenuti dall'associazione usando il GUID dell'oggetto:</span><span class="sxs-lookup"><span data-stu-id="d2e50-124">The following **IADsContainer** methods are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="d2e50-125">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="d2e50-125">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="d2e50-126">**Creare**</span><span class="sxs-lookup"><span data-stu-id="d2e50-126">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="d2e50-127">**Delete**</span><span class="sxs-lookup"><span data-stu-id="d2e50-127">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="d2e50-128">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="d2e50-128">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="d2e50-129">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="d2e50-129">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="d2e50-130">Per utilizzare questi metodi e proprietà dopo l'associazione a un oggetto utilizzando il GUID dell'oggetto, utilizzare il metodo [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare il nome distinto dell'oggetto e quindi utilizzare il nome distinto per associare nuovamente l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2e50-130">To use these methods and properties after binding to an object using the object GUID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="d2e50-131">Se un'applicazione archivia o memorizza nella cache gli identificatori o i riferimenti agli oggetti archiviati in Active Directory Domain Services, il GUID dell'oggetto è l'identificatore migliore da usare per diversi motivi:</span><span class="sxs-lookup"><span data-stu-id="d2e50-131">If an application stores or caches identifiers or references to objects stored in Active Directory Domain Services, the object GUID is the best identifier to use for several reasons:</span></span>

-   <span data-ttu-id="d2e50-132">La proprietà **objectGUID** di sull'oggetto non cambia mai anche se l'oggetto è stato rinominato o spostato.</span><span class="sxs-lookup"><span data-stu-id="d2e50-132">The **objectGUID** property of on object never changes even if the object is renamed or moved.</span></span>
-   <span data-ttu-id="d2e50-133">È facile eseguire l'associazione all'oggetto usando il GUID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2e50-133">It is easy to bind to the object using the object GUID.</span></span>
-   <span data-ttu-id="d2e50-134">Se l'oggetto viene rinominato o spostato, la proprietà **objectGUID** fornisce un identificatore singolo che può essere usato per trovare e identificare rapidamente l'oggetto anziché dover comporre una query con condizioni per tutte le proprietà che identificano tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2e50-134">If the object is renamed or moved, the **objectGUID** property provides a single identifier that can be used to quickly find and identify the object rather than having to compose a query that has conditions for all properties that would identify that object.</span></span>

 

 
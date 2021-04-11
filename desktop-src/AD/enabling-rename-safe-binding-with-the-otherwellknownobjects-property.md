---
title: Abilitazione di Rename-Safe binding con la proprietà otherWellKnownObjects archiviato nel
description: Gli oggetti della classe contenitore hanno un attributo otherWellKnownObjects archiviato nel che è possibile usare per associare un GUID al nome distinto (DN) di un oggetto figlio nel contenitore.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- proprietà otherWellKnownObjects archiviato nel
- proprietà otherWellKnownObjects archiviato nel, utilizzo di per l'associazione Rinomina-Safe
- Active Directory, utilizzo, associazione, associazione Rinomina-Safe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220945"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a><span data-ttu-id="53573-106">Abilitazione di Rename-Safe binding con la proprietà otherWellKnownObjects archiviato nel</span><span class="sxs-lookup"><span data-stu-id="53573-106">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>

<span data-ttu-id="53573-107">Gli oggetti della classe contenitore hanno un attributo **otherWellKnownObjects archiviato nel** che è possibile usare per associare un GUID al nome distinto (DN) di un oggetto figlio nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="53573-107">Objects of the Container class have an **otherWellKnownObjects** attribute that you can use to associate a GUID with the distinguished name (DN) of a child object in the container.</span></span> <span data-ttu-id="53573-108">Se l'oggetto figlio viene spostato o rinominato, il server di Active Directory aggiorna il DN nel valore **otherWellKnownObjects archiviato nel** per tale oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="53573-108">If the child object is moved or renamed, the Active Directory server updates the DN in the **otherWellKnownObjects** value for that child object.</span></span> <span data-ttu-id="53573-109">Questo consente di utilizzare la funzionalità di associazione WKGUID per eseguire l'associazione all'oggetto figlio utilizzando il GUID e il DN del contenitore anziché il DN dell'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="53573-109">This enables use of the WKGUID binding feature to bind to the child object using the GUID and the DN of the container rather than the child object's DN.</span></span>

<span data-ttu-id="53573-110">L'attributo **otherWellKnownObjects archiviato nel** è equivalente all'attributo **wellKnownObjects** ad eccezione del fatto che le applicazioni e i servizi possono scrivere un valore **otherWellKnownObjects archiviato nel** , ma solo il sistema è in grado di scrivere **wellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="53573-110">The **otherWellKnownObjects** attribute is equivalent to the **wellKnownObjects** attribute except that applications and services can write an **otherWellKnownObjects** value, but only the system can write **wellKnownObjects**.</span></span>

<span data-ttu-id="53573-111">L'uso dell'attributo **otherWellKnownObjects archiviato nel** e dell'associazione WKGUID è vantaggioso nelle situazioni seguenti in cui è necessaria un'associazione Rinomina-safe in relazione a un oggetto contenitore specifico.</span><span class="sxs-lookup"><span data-stu-id="53573-111">Using **otherWellKnownObjects** attribute and WKGUID binding is beneficial in the following situations where rename-safe binding is required in relation to a specific container object.</span></span>

<span data-ttu-id="53573-112">Se un oggetto contenitore contiene altri oggetti importanti o se gli oggetti importanti possono essere rinominati o spostati.</span><span class="sxs-lookup"><span data-stu-id="53573-112">If a container object contains other important objects, or if important objects can be renamed or moved.</span></span>

<span data-ttu-id="53573-113">Se sono presenti oggetti importanti per ogni istanza dell'oggetto contenitore.</span><span class="sxs-lookup"><span data-stu-id="53573-113">If the important objects exist for each instance of the container object.</span></span> <span data-ttu-id="53573-114">Ad esempio, il sistema usa l'attributo **wellKnownObjects** di ogni oggetto **domainDNS** per archiviare un valore per il contenitore Users, presente in ogni istanza di un oggetto **domainDNS** .</span><span class="sxs-lookup"><span data-stu-id="53573-114">For example, the system uses the **wellKnownObjects** attribute of each **domainDNS** object to store a value for the Users container, which exists in every instance of a **domainDNS** object.</span></span> <span data-ttu-id="53573-115">Questo consente alle applicazioni di eseguire il binding al contenitore degli utenti in modo indipendente dalla ridenominazione specificando il GUID noto e il DN del contenitore **domainDNS** .</span><span class="sxs-lookup"><span data-stu-id="53573-115">This enables applications to bind to the Users container in a rename-safe way by specifying the well-known GUID and the DN of the **domainDNS** container.</span></span> <span data-ttu-id="53573-116">Le applicazioni possono usare l'attributo **otherWellKnownObjects archiviato nel** di un contenitore in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="53573-116">Applications can use a container's **otherWellKnownObjects** attribute similarly.</span></span>

<span data-ttu-id="53573-117">Se è necessario un binding e/o una funzionalità di ricerca indipendente da rinominare sugli oggetti importanti.</span><span class="sxs-lookup"><span data-stu-id="53573-117">If you require rename-safe binding and/or search capability on the important objects.</span></span>

<span data-ttu-id="53573-118">**Per aggiungere le funzionalità di ricerca e associazione Rinomina-Safe**</span><span class="sxs-lookup"><span data-stu-id="53573-118">**To add rename-safe binding and search capabilities**</span></span>

1.  <span data-ttu-id="53573-119">Aggiungere un valore alla proprietà **otherWellKnownObjects archiviato nel** dell'oggetto contenitore quando viene creato l'oggetto importante in tale contenitore.</span><span class="sxs-lookup"><span data-stu-id="53573-119">Add a value to the **otherWellKnownObjects** property of the container object when the important object is created within that container.</span></span> <span data-ttu-id="53573-120">Il valore contiene il GUID che rappresenta l'oggetto noto.</span><span class="sxs-lookup"><span data-stu-id="53573-120">The value contains the GUID that represents the well-known object.</span></span> <span data-ttu-id="53573-121">Si noti che questo non è **objectGUID** e **Distinguishname** per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="53573-121">Be aware that this is not the **objectGUID** and the **distinguishedName** for that object.</span></span>
2.  <span data-ttu-id="53573-122">Utilizzare la funzionalità di associazione WKGUID per eseguire il binding o eseguire ricerche nell'oggetto importante.</span><span class="sxs-lookup"><span data-stu-id="53573-122">Use the WKGUID binding feature to bind to or search the important object.</span></span>

<span data-ttu-id="53573-123">L'attributo **otherWellKnownObjects archiviato nel** può avere più valori e contiene le tuple GUID/DN di oggetti noti all'interno dei contenitori in cui sono impostati.</span><span class="sxs-lookup"><span data-stu-id="53573-123">The **otherWellKnownObjects** attribute can have multiple values and contains the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="53573-124">L'attributo **otherWellKnownObjects archiviato nel** ha la sintassi DNWithBinary in cui i valori hanno il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="53573-124">The **otherWellKnownObjects** attribute has the DNWithBinary syntax in which values have the following form:</span></span>


```C++
B:<char count>:<well known GUID>:<object DN>
```



<span data-ttu-id="53573-125">In questo esempio, " &lt; char count &gt; " è il numero di cifre esadecimali in " &lt; well known GUID &gt; ", ovvero 32 (numero di cifre esadecimali in un GUID) sia per **otherWellKnownObjects archiviato nel** che per **wellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="53573-125">In this example, "&lt;char count&gt;" is the count of hexadecimal digits in "&lt;well known GUID&gt;", which is 32 (number of hex digits in a GUID) for both **otherWellKnownObjects** and **wellKnownObjects**.</span></span> <span data-ttu-id="53573-126">" &lt; well known GUID &gt; " è la rappresentazione in cifre esadecimale del GUID noto.</span><span class="sxs-lookup"><span data-stu-id="53573-126">"&lt;well known GUID&gt;" is the hexadecimal digit representation of the well-known GUID.</span></span> <span data-ttu-id="53573-127">" &lt; DN oggetto &gt; " è il nome distinto dell'oggetto rappresentato da questo valore WKO.</span><span class="sxs-lookup"><span data-stu-id="53573-127">"&lt;object DN&gt;" is the distinguished name of the object represented by this WKO value.</span></span> <span data-ttu-id="53573-128">Il server mantiene la parte ObjectDN di ogni valore **wellKnownObjects** e **otherWellKnownObjects archiviato nel** in modo che contenga il nome distinto corrente dell'oggetto specificato in origine al momento della creazione del valore.</span><span class="sxs-lookup"><span data-stu-id="53573-128">The server maintains the ObjectDN portion of each **wellKnownObjects** and **otherWellKnownObjects** value so that it contains the current distinguished name of the object originally specified when the value was created.</span></span>

<span data-ttu-id="53573-129">Se, ad esempio, {df447b5e-AA5B-11D2-8D53-00c04f79ab81} è il GUID noto dell'oggetto MyObject nel contenitore di contenuto del dominio Fabrikam.com, il valore di **otherWellKnownObjects archiviato nel** specifica il GUID noto e il DN di oggetto:</span><span class="sxs-lookup"><span data-stu-id="53573-129">For example, if {df447b5e-aa5b-11d2-8d53-00c04f79ab81} is the well-known GUID of the MyObject object in the MyContainer container in the Fabrikam.com domain, the **otherWellKnownObjects** value would specify the well-known GUID and the DN of MyObject:</span></span>


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



<span data-ttu-id="53573-130">Per eseguire l'associazione a questo oggetto, usare la stringa di associazione WKGUID seguente che specifica il GUID noto dell'oggetto e il DN del contenitore:</span><span class="sxs-lookup"><span data-stu-id="53573-130">To bind to this object, use the following WKGUID binding string that specifies the well-known GUID of the object and the DN of the container:</span></span>


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



<span data-ttu-id="53573-131">Dopo l'associazione a questo oggetto, è possibile utilizzare le interfacce COM ADSI per cercare, leggere, modificare o eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="53573-131">After binding to this object, you can use the ADSI COM interfaces to search, read, modify, or delete the object.</span></span>

<span data-ttu-id="53573-132">Per ulteriori informazioni e un esempio di codice che illustra come aggiungere un oggetto all'attributo **otherWellKnownObjects archiviato nel** , vedere [codice di esempio per la creazione di un oggetto contenitore](example-code-for-creating-a-container-object.md).</span><span class="sxs-lookup"><span data-stu-id="53573-132">For more information and a code example that shows how to add an object to the **otherWellKnownObjects** attribute, see [Example Code for Creating a Container Object](example-code-for-creating-a-container-object.md).</span></span>

 

 





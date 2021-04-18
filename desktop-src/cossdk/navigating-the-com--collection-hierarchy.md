---
description: Esplorazione della gerarchia della raccolta COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Esplorazione della gerarchia della raccolta COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304816"
---
# <a name="navigating-the-com-collection-hierarchy"></a><span data-ttu-id="54da8-103">Esplorazione della gerarchia della raccolta COM+</span><span class="sxs-lookup"><span data-stu-id="54da8-103">Navigating the COM+ Collection Hierarchy</span></span>

<span data-ttu-id="54da8-104">Alcune raccolte che è possibile recuperare facilmente usando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) nell'oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="54da8-104">Some collections you can retrieve easily by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="54da8-105">Questo metodo recupera una raccolta "di primo livello"; ovvero una raccolta, ad esempio [**applicazioni**](applications.md), che si basa su se stessa e che è univoca e non è inglobata logicamente in un'altra raccolta.</span><span class="sxs-lookup"><span data-stu-id="54da8-105">This method retrieves a "top-level" collection; that is, a collection such as [**Applications**](applications.md), which stands on its own and which is unique and not logically subsumed under another collection.</span></span>

<span data-ttu-id="54da8-106">Molte raccolte, tuttavia, sono inglobate logicamente in un'altra raccolta perché contengono elementi che fanno parte di una struttura più grande.</span><span class="sxs-lookup"><span data-stu-id="54da8-106">Many collections, however, are logically subsumed under another collection because they contain elements that are part of some larger structure.</span></span> <span data-ttu-id="54da8-107">La raccolta [**Components**](components.md) , ad esempio, è inglobata o correlata alla raccolta di [**applicazioni**](applications.md) perché contiene i componenti installati in una particolare applicazione com+, che a sua volta corrisponde a un elemento nella raccolta di **applicazioni** .</span><span class="sxs-lookup"><span data-stu-id="54da8-107">For example, the [**Components**](components.md) collection is subsumed, or related, to the [**Applications**](applications.md) collection because it contains the components installed in a particular COM+ application, which itself corresponds to an item in the **Applications** collection.</span></span> <span data-ttu-id="54da8-108">Le raccolte correlate, ad esempio, non sono univoche. è disponibile una raccolta di **componenti** per ogni applicazione distinta.</span><span class="sxs-lookup"><span data-stu-id="54da8-108">Related collections such as this are not unique; there is a **Components** collection for each distinct application.</span></span>

<span data-ttu-id="54da8-109">Pertanto, le raccolte sono disposte in una struttura gerarchica che corrisponde naturalmente alle relazioni logiche tra gli elementi in essi contenuti.</span><span class="sxs-lookup"><span data-stu-id="54da8-109">Therefore, collections are arranged in a hierarchical structure that corresponds naturally to the logical relationships between the items they contain.</span></span> <span data-ttu-id="54da8-110">Un diagramma della gerarchia della raccolta è reperibile in [raccolte di amministrazione com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="54da8-110">A diagram of the collection hierarchy can be found at [COM+ Administration Collections](com--administration-collections.md).</span></span> <span data-ttu-id="54da8-111">Per molti degli elementi che si desidera configurare utilizzando gli oggetti COMAdmin, è necessario spostarsi in una parte della gerarchia della raccolta per recuperare l'elemento appropriato.</span><span class="sxs-lookup"><span data-stu-id="54da8-111">For many of the elements that you want to configure using the COMAdmin objects, you need to navigate through some portion of the collection hierarchy to retrieve the appropriate item.</span></span>

<span data-ttu-id="54da8-112">Ciò significa che se si vuole ottenere un elemento in una raccolta correlata, è necessario eseguire prima di tutto il livello superiore necessario, ovvero le raccolte classificato.</span><span class="sxs-lookup"><span data-stu-id="54da8-112">What this means in practice is that if you want to get an item in a related collection, you need to go through all the necessary higher level, subsuming collections first.</span></span> <span data-ttu-id="54da8-113">Per recuperare una raccolta correlata, è necessario recuperare l'elemento specifico nella raccolta padre a cui è correlata la raccolta figlio.</span><span class="sxs-lookup"><span data-stu-id="54da8-113">And to retrieve a related collection, you need to retrieve the specific item in the parent collection to which the child collection is related.</span></span> <span data-ttu-id="54da8-114">Se, ad esempio, si desidera configurare un elemento corrispondente a un componente in una particolare applicazione COM+, è necessario eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="54da8-114">For example, if you want to configure an item corresponding to a component in a particular COM+ application, you must perform the following steps:</span></span>

1.  <span data-ttu-id="54da8-115">Ottenere la raccolta di [**applicazioni**](applications.md) e compilarla.</span><span class="sxs-lookup"><span data-stu-id="54da8-115">Get the [**Applications**](applications.md) collection and populate it.</span></span>
2.  <span data-ttu-id="54da8-116">Consente di enumerare il contenuto della raccolta di [**applicazioni**](applications.md) fino a quando non si ottiene l'elemento corrispondente all'applicazione COM+ corretta.</span><span class="sxs-lookup"><span data-stu-id="54da8-116">Enumerate through the contents of the [**Applications**](applications.md) collection until you get to the item corresponding to the correct COM+ application.</span></span>
3.  <span data-ttu-id="54da8-117">Ottenere e popolare la raccolta di [**componenti**](components.md) per quella particolare applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="54da8-117">Get and populate the [**Components**](components.md) collection for that particular COM+ application.</span></span>
4.  <span data-ttu-id="54da8-118">Enumerare il contenuto della raccolta [**Components**](components.md) fino a quando non si ottiene l'elemento corrispondente al componente corretto.</span><span class="sxs-lookup"><span data-stu-id="54da8-118">Enumerate through the contents of the [**Components**](components.md) collection until you get to the item corresponding to the correct component.</span></span>

<span data-ttu-id="54da8-119">Nell'esempio di Visual Basic Microsoft riportato di seguito viene illustrato come eseguire i passaggi precedenti:</span><span class="sxs-lookup"><span data-stu-id="54da8-119">The following Microsoft Visual Basic example shows how to perform the preceding steps:</span></span>


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



<span data-ttu-id="54da8-120">Nell'esempio precedente vengono usati due metodi **GetCollection** distinti.</span><span class="sxs-lookup"><span data-stu-id="54da8-120">Two distinct **GetCollection** methods are used in the preceding example.</span></span> <span data-ttu-id="54da8-121">Il primo è esposto da [**COMAdminCatalog**](comadmincatalog.md) e viene usato per ottenere una raccolta di primo livello, in questo caso "Applications".</span><span class="sxs-lookup"><span data-stu-id="54da8-121">The first is exposed by [**COMAdminCatalog**](comadmincatalog.md) and is used to get a top-level collection—in this case, "Applications".</span></span> <span data-ttu-id="54da8-122">Il secondo è esposto da [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e viene usato per ottenere una raccolta correlata alla raccolta corrente. è possibile indicare con precisione la raccolta desiderata passando il nome "Components" e il valore della proprietà chiave dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="54da8-122">The second is exposed by [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and is used to get a collection related to the present collection; you indicate precisely which collection you want by passing in the name "Components" and the Key property value of the parent object.</span></span> <span data-ttu-id="54da8-123">Il valore della proprietà Key è spesso un nome o un GUID che identifica in modo univoco l'oggetto; Questo valore viene identificato nella documentazione per ogni raccolta.</span><span class="sxs-lookup"><span data-stu-id="54da8-123">The Key property value is often a name or a GUID that uniquely identifies the object; this value is identified in the documentation for each collection.</span></span>

<span data-ttu-id="54da8-124">Nel caso più generale, è necessario ottenere le raccolte correlate in modo iterativo nella gerarchia della raccolta fino a quando non si recupera la raccolta desiderata.</span><span class="sxs-lookup"><span data-stu-id="54da8-124">In the most general case, you need to get related collections iteratively down the collection hierarchy until you retrieve the collection you want.</span></span> <span data-ttu-id="54da8-125">La procedura da seguire è la stessa del modello generale, ripetutamente.</span><span class="sxs-lookup"><span data-stu-id="54da8-125">The steps you would take follow the same general model, repetitively.</span></span> <span data-ttu-id="54da8-126">Per un elenco completo delle raccolte, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="54da8-126">For a complete list of collections, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="54da8-127">In alcuni casi, potrebbe essere necessario usare un metodo di collegamento la seconda volta che si segue un percorso attraverso la gerarchia di raccolta.</span><span class="sxs-lookup"><span data-stu-id="54da8-127">In some cases, you might want to use a shortcut method the second time you follow a path through the collection hierarchy.</span></span> <span data-ttu-id="54da8-128">È possibile utilizzare questo metodo solo dopo aver già memorizzato nella cache tutti i valori di chiave che interessano.</span><span class="sxs-lookup"><span data-stu-id="54da8-128">You can use this method only after you have already cached all the intervening Key values.</span></span> <span data-ttu-id="54da8-129">Per informazioni dettagliate, vedere [**ICOMAdminCatalog:: GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span><span class="sxs-lookup"><span data-stu-id="54da8-129">For details, see [**ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54da8-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54da8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54da8-131">Popolamento di raccolte COM+</span><span class="sxs-lookup"><span data-stu-id="54da8-131">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="54da8-132">Esecuzione di query per le raccolte correlate disponibili</span><span class="sxs-lookup"><span data-stu-id="54da8-132">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="54da8-133">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="54da8-133">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 




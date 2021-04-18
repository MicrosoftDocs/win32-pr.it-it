---
title: Oggetti e proprietà
description: Le caratteristiche di un oggetto in SDO sono determinate dalle proprietà dell'oggetto e dai valori associati a tali proprietà.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300080"
---
# <a name="objects-and-properties"></a><span data-ttu-id="17555-103">Oggetti e proprietà</span><span class="sxs-lookup"><span data-stu-id="17555-103">Objects and Properties</span></span>

<span data-ttu-id="17555-104">Le caratteristiche di un oggetto in SDO sono determinate dalle proprietà dell'oggetto e dai valori associati a tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="17555-104">The characteristics of an object in SDO are determined by the object's properties, and the values associated with those properties.</span></span> <span data-ttu-id="17555-105">A differenza di altri modelli a oggetti, gli oggetti SDO non dispongono di metodi.</span><span class="sxs-lookup"><span data-stu-id="17555-105">Unlike some other object models, SDO objects themselves do not have methods.</span></span> <span data-ttu-id="17555-106">Tuttavia, gli oggetti SDO espongono interfacce COM che forniscono metodi.</span><span class="sxs-lookup"><span data-stu-id="17555-106">However, SDO objects do expose COM interfaces that provide methods.</span></span>

<span data-ttu-id="17555-107">Gli oggetti in SDO espongono l'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) che fornisce i metodi per modificare le proprietà degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="17555-107">Objects in SDO expose the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface that provides methods for manipulating the objects properties.</span></span> <span data-ttu-id="17555-108">Per accedere alle proprietà dell'oggetto, ottenere un'interfaccia **ISdo** per l'oggetto e usare i metodi di interfaccia [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) e [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) per recuperare e impostare i valori per le proprietà.</span><span class="sxs-lookup"><span data-stu-id="17555-108">To access the object's properties, obtain an **ISdo** interface for the object, and use the [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) and [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) interface methods to retrieve and set values for the properties.</span></span> <span data-ttu-id="17555-109">L'argomento [recupero di un SDO utente](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contiene codice di esempio che illustra come ottenere l'interfaccia **ISdo** per un oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="17555-109">The topic [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains sample code that demonstrates obtaining the **ISdo** interface for a User object.</span></span>

<span data-ttu-id="17555-110">Dopo avere apportato le modifiche alle proprietà di un oggetto, usare il metodo [**ISdo:: Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) per scrivere le modifiche nell'archivio permanente per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="17555-110">After making changes to the properties of an object, use the [**ISdo::Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) method to write the changes to persistent storage for the object.</span></span> <span data-ttu-id="17555-111">È possibile annullare le modifiche apportate alle proprietà di un oggetto prima di chiamare **ISdo:: Apply** chiamando il metodo [**ISdo:: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) .</span><span class="sxs-lookup"><span data-stu-id="17555-111">You can cancel changes made to an object's properties before you call **ISdo::Apply** by calling the [**ISdo::Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) method.</span></span> <span data-ttu-id="17555-112">Questo metodo consente di ripristinare i valori delle proprietà di un oggetto dall'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="17555-112">This method restores the values of an object's properties from persistent storage.</span></span>

<span data-ttu-id="17555-113">Nella tabella seguente vengono illustrati i tipi di enumerazione che enumerano le proprietà di alcuni oggetti in SDO.</span><span class="sxs-lookup"><span data-stu-id="17555-113">The following table shows the enumeration types that enumerate the properties of some of the objects in SDO.</span></span>



| <span data-ttu-id="17555-114">Oggetto</span><span class="sxs-lookup"><span data-stu-id="17555-114">Object</span></span>                                 | <span data-ttu-id="17555-115">Tipo di enumerazione</span><span class="sxs-lookup"><span data-stu-id="17555-115">Enumeration type</span></span>                                       |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="17555-116">Tutti gli oggetti SDO</span><span class="sxs-lookup"><span data-stu-id="17555-116">All SDO objects</span></span>                        | [<span data-ttu-id="17555-117">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="17555-117">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| <span data-ttu-id="17555-118">Oggetto utente</span><span class="sxs-lookup"><span data-stu-id="17555-118">User Object</span></span>                            | [<span data-ttu-id="17555-119">**USERPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="17555-119">**USERPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| <span data-ttu-id="17555-120">Oggetto servizio (server dei criteri di rete)</span><span class="sxs-lookup"><span data-stu-id="17555-120">Service Object (Network Policy Server)</span></span> | [<span data-ttu-id="17555-121">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="17555-121">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| <span data-ttu-id="17555-122">Oggetto protocollo RADIUS Microsoft</span><span class="sxs-lookup"><span data-stu-id="17555-122">Microsoft RADIUS Protocol Object</span></span>       | [<span data-ttu-id="17555-123">**RADIUSPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="17555-123">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> <span data-ttu-id="17555-124">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="17555-124">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

## <a name="collections"></a><span data-ttu-id="17555-125">Raccolte</span><span class="sxs-lookup"><span data-stu-id="17555-125">Collections</span></span>

<span data-ttu-id="17555-126">Gli oggetti vengono spesso raggruppati in raccolte.</span><span class="sxs-lookup"><span data-stu-id="17555-126">Objects are often grouped into collections.</span></span> <span data-ttu-id="17555-127">L'API SDO fornisce funzionalità, tramite l'interfaccia di [**raccolta ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) , per enumerare gli oggetti in una raccolta e per aggiungere ed eliminare oggetti da una raccolta.</span><span class="sxs-lookup"><span data-stu-id="17555-127">The SDO API provides functionality, through the [**ISdo Collection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface, to enumerate the objects in a collection and to add and delete objects from a collection.</span></span>

<span data-ttu-id="17555-128">Per ottenere l'accesso a una raccolta, è necessario recuperare una proprietà di raccolta nell'oggetto che contiene la raccolta.</span><span class="sxs-lookup"><span data-stu-id="17555-128">Access to a collection is obtained by retrieving a collection property on the object that contains the collection.</span></span> <span data-ttu-id="17555-129">Per ulteriori informazioni, vedere la sezione [gerarchia del modello a oggetti](/windows/desktop/Nps/sdo-object-model-hierarchy).</span><span class="sxs-lookup"><span data-stu-id="17555-129">For more information, see the section [Object Model Hierarchy](/windows/desktop/Nps/sdo-object-model-hierarchy).</span></span>

<span data-ttu-id="17555-130">Il tipo di dati per tutte le proprietà che corrispondono alle raccolte è VT \_ Dispatch.</span><span class="sxs-lookup"><span data-stu-id="17555-130">The data type for all properties that correspond to collections is VT\_DISPATCH.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17555-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17555-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17555-132">Gerarchia del modello a oggetti SDO</span><span class="sxs-lookup"><span data-stu-id="17555-132">SDO Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="17555-133">Attributi supportati da SDO</span><span class="sxs-lookup"><span data-stu-id="17555-133">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 
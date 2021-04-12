---
description: Recupero e impostazione delle proprietà
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Recupero e impostazione delle proprietà (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483445"
---
# <a name="getting-and-setting-properties-component-services"></a><span data-ttu-id="d3e9e-103">Recupero e impostazione delle proprietà (Servizi componenti)</span><span class="sxs-lookup"><span data-stu-id="d3e9e-103">Getting and Setting Properties (Component Services)</span></span>

<span data-ttu-id="d3e9e-104">Prima di poter leggere o scrivere particolari proprietà esposte da un elemento in una raccolta, è necessario eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d3e9e-104">Before you can read or write particular properties exposed by an item in a collection, you must take the following steps:</span></span>

1.  <span data-ttu-id="d3e9e-105">Recuperare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-105">Retrieve the collection.</span></span>
2.  <span data-ttu-id="d3e9e-106">Compilare la raccolta per leggere i dati dal catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-106">Populate the collection to read in data for it from the COM+ catalog.</span></span>
3.  <span data-ttu-id="d3e9e-107">Recuperare l'elemento specifico della raccolta, che lo rappresenta con un oggetto della classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="d3e9e-107">Retrieve the specific item in the collection, representing it with an object from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="d3e9e-108">Per un esempio in cui vengono illustrati questi passaggi, vedere [esplorazione della gerarchia della raccolta com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="d3e9e-108">For an example that illustrates these steps, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="d3e9e-109">Poiché le particolari proprietà esposte possono variare a seconda dell'elemento rappresentato dall'elemento; ovvero un elemento che rappresenta un componente ha proprietà diverse rispetto a una che rappresenta un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-109">Because the particular properties exposed can vary depending on what the item represents; that is, an item representing a component has different properties than one representing a COM+ application.</span></span> <span data-ttu-id="d3e9e-110">Impostare una di queste proprietà utilizzando una singola proprietà generica, ovvero la proprietà Value, su [**COMAdminCatalogObject**](comadmincatalogobject.md).</span><span class="sxs-lookup"><span data-stu-id="d3e9e-110">Set any of these properties using a single generic property, the Value property, on [**COMAdminCatalogObject**](comadmincatalogobject.md).</span></span>

<span data-ttu-id="d3e9e-111">La proprietà Value consente di ottenere o impostare eventuali proprietà denominate specifiche esposte da un elemento, restituendo un valore per una proprietà denominata durante il recupero e accettando un nome e un valore quando si imposta.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-111">The Value property enables you to get or set any specific named property exposed by an item, returning a value for a named property when getting, and taking a name and value when setting.</span></span>

<span data-ttu-id="d3e9e-112">Non vengono effettivamente registrate modifiche nel catalogo COM+ fino a quando non si salvano in modo esplicito le modifiche utilizzando il metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sull'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d3e9e-112">No changes are actually recorded to the COM+ catalog until you explicitly save changes using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="d3e9e-113">Le modifiche in sospeso per tutte le proprietà di tutti gli elementi di una raccolta specifica vengono salvate in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-113">Pending changes for all properties on all items in a given collection are saved all at once.</span></span> <span data-ttu-id="d3e9e-114">Per informazioni dettagliate, vedere [salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="d3e9e-114">For details, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="d3e9e-115">Non tutte le modifiche apportate verranno accettate.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-115">Not all changes that you make will be accepted.</span></span> <span data-ttu-id="d3e9e-116">Il catalogo COM+ applica una logica coerenza per assicurarsi di configurare gli elementi in modo ragionevole.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-116">The COM+ catalog enforces some coherency logic to ensure that you configure things in a reasonable way.</span></span> <span data-ttu-id="d3e9e-117">Inoltre, quando si modificano alcune proprietà, altre potrebbero cambiare automaticamente dalla stessa logica di coerenza.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-117">Additionally, when you change some properties, others might change automatically by the same coherency logic.</span></span> <span data-ttu-id="d3e9e-118">Questi effetti vengono visualizzati quando si tenta di salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-118">These effects show up when you attempt to save changes.</span></span>

> [!Note]  
> <span data-ttu-id="d3e9e-119">È possibile che si sia in conflitto con un altro writer nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-119">It is possible for you to be in contention with another writer to the COM+ catalog.</span></span> <span data-ttu-id="d3e9e-120">Tra le chiamate a [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per una determinata raccolta, non si dispone di un blocco su nessuno dei dati nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-120">Between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) for a given collection, you do not have a lock on any of that data in the catalog.</span></span> <span data-ttu-id="d3e9e-121">Più parti possono contemporaneamente configurare gli elementi in una raccolta specificata e potrebbero essere in conflitto quando salvano le modifiche.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-121">Multiple parties may simultaneously be configuring items in a given collection and could be contending when they save changes.</span></span> <span data-ttu-id="d3e9e-122">Ciò significa che un altro utente potrebbe modificare le impostazioni di un oggetto prima o dopo l'esecuzione, eseguendo un tipo di programma usando gli oggetti COMAdmin o utilizzando lo strumento di amministrazione Servizi componenti, in locale o in remoto.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-122">This means that someone else might change settings on an object before or after you do, either running some kind of program using the COMAdmin objects or using the Component Services administrative tool, either locally or remotely.</span></span> <span data-ttu-id="d3e9e-123">La regola generale per la scrittura di oggetti nel catalogo è che tutte le proprietà di un oggetto vengono scritte in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-123">The general rule with writing objects on the catalog is that all properties on an object are written at once.</span></span> <span data-ttu-id="d3e9e-124">Ovvero l'ultimo writer WINS, l'oggetto viene salvato nel catalogo esattamente come l'ultimo autore lo ha configurato.</span><span class="sxs-lookup"><span data-stu-id="d3e9e-124">That is, the last writer wins—the object is saved in the catalog precisely as the last writer configured it.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d3e9e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3e9e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3e9e-126">Interdipendenze tra proprietà</span><span class="sxs-lookup"><span data-stu-id="d3e9e-126">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="d3e9e-127">Esecuzione di query per le proprietà disponibili</span><span class="sxs-lookup"><span data-stu-id="d3e9e-127">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="d3e9e-128">Salvataggio o eliminazione di modifiche</span><span class="sxs-lookup"><span data-stu-id="d3e9e-128">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 




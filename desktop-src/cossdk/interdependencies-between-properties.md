---
description: Interdipendenze tra proprietà
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdipendenze tra proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966172"
---
# <a name="interdependencies-between-properties"></a><span data-ttu-id="2dcf4-103">Interdipendenze tra proprietà</span><span class="sxs-lookup"><span data-stu-id="2dcf4-103">Interdependencies Between Properties</span></span>

<span data-ttu-id="2dcf4-104">Quando si impostano le proprietà, il catalogo COM+ applica una logica coerenza per assicurarsi di configurare gli elementi in modo ragionevole.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-104">When you set properties, the COM+ catalog enforces some coherency logic to ensure that you configure elements in a reasonable way.</span></span> <span data-ttu-id="2dcf4-105">Questa logica può essere implementata in due modi, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2dcf4-105">This logic can be implemented in two ways, as follows:</span></span>

-   <span data-ttu-id="2dcf4-106">**Dipendenze.**</span><span class="sxs-lookup"><span data-stu-id="2dcf4-106">**Dependencies.**</span></span> <span data-ttu-id="2dcf4-107">È possibile che non vengano apportate modifiche perché un'altra proprietà dipende da una particolare impostazione per una proprietà che si tenta di impostare.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-107">You might be blocked from making some changes because another property depends on a particular setting for a property you attempt to set.</span></span> <span data-ttu-id="2dcf4-108">Se, ad esempio, un componente viene impostato con le transazioni dell'attributo richieste e se si tenta di modificare l'impostazione di sincronizzazione su None, viene generato un errore quando si tenta di chiamare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) perché le transazioni dipendono dalla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-108">For example, if a component is set with the attribute Transactions Required and if you then attempt to change the Synchronization setting to None, an error is generated when you attempt to call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) because transactions depend on synchronization.</span></span>
-   <span data-ttu-id="2dcf4-109">**Effetti collaterali.**</span><span class="sxs-lookup"><span data-stu-id="2dcf4-109">**Side effects.**</span></span> <span data-ttu-id="2dcf4-110">Alcune proprietà possono essere modificate senza impostarle in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-110">Some properties might be changed for you without your explicitly setting them.</span></span> <span data-ttu-id="2dcf4-111">Se, ad esempio, si imposta un componente con le transazioni degli attributi necessarie, anche la sincronizzazione verrà impostata su Required.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-111">For example, if you set a component with the attribute Transactions Required, Synchronization will be set to Required as well.</span></span> <span data-ttu-id="2dcf4-112">Si tratta in realtà del lato invertito delle dipendenze: una proprietà ha la precedenza rispetto a un'altra e la relativa dipendenza viene espressa tramite la prima impostazione della proprietà secondaria e quindi bloccando le modifiche apportate a tale proprietà.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-112">This is really the flip side of dependencies—one property takes precedence over another, and its dependency is expressed through first setting the secondary property and then blocking changes to it.</span></span>

<span data-ttu-id="2dcf4-113">Nell'elenco delle proprietà esposte da elementi di una raccolta, tutte elencate in [raccolte di amministrazione com+](com--administration-collections.md), le dipendenze e gli effetti collaterali vengono indicati per ogni proprietà.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-113">In the list of properties exposed by items in a collection, all listed in [COM+ Administration Collections](com--administration-collections.md), the dependencies and side effects are stated for each property.</span></span> <span data-ttu-id="2dcf4-114">Quando si configurano le applicazioni e i componenti COM+, è necessario tenere presente quali vincoli vengono imposti alle configurazioni.</span><span class="sxs-lookup"><span data-stu-id="2dcf4-114">When you configure COM+ applications and components, you should be aware of what constraints are imposed on configurations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dcf4-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2dcf4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dcf4-116">Recupero e impostazione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="2dcf4-116">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="2dcf4-117">Esecuzione di query per le proprietà disponibili</span><span class="sxs-lookup"><span data-stu-id="2dcf4-117">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="2dcf4-118">Salvataggio o eliminazione di modifiche</span><span class="sxs-lookup"><span data-stu-id="2dcf4-118">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 




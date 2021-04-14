---
description: Registrazione e attivazione di componenti nelle partizioni
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registrazione e attivazione di componenti nelle partizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523530"
---
# <a name="registering-and-activating-components-in-partitions"></a><span data-ttu-id="2d63b-103">Registrazione e attivazione di componenti nelle partizioni</span><span class="sxs-lookup"><span data-stu-id="2d63b-103">Registering and Activating Components in Partitions</span></span>

<span data-ttu-id="2d63b-104">Dopo la creazione di una partizione, il passaggio successivo consiste nel registrare i componenti COM+ all'interno di tale partizione.</span><span class="sxs-lookup"><span data-stu-id="2d63b-104">After a partition has been created, the next step is register your COM+ components within that partition.</span></span> <span data-ttu-id="2d63b-105">Un componente viene registrato all'interno di una partizione quando viene creata una nuova applicazione COM+ o quando si installa un'applicazione COM+ esistente nella partizione.</span><span class="sxs-lookup"><span data-stu-id="2d63b-105">A component is registered within a partition when a new COM+ application is created or when an existing COM+ application is installed into the partition.</span></span> <span data-ttu-id="2d63b-106">Per semplificare l'amministrazione della registrazione quando più partizioni contengono gli stessi componenti COM+, il servizio partizioni consente a un amministratore di copiare applicazioni o componenti da una partizione all'altra.</span><span class="sxs-lookup"><span data-stu-id="2d63b-106">To ease the administration of registration when multiple partitions contain the same COM+ components, the partitions service allows an administrator to copy applications or components from one partition into another.</span></span> <span data-ttu-id="2d63b-107">Quando viene copiata un'applicazione COM+ o un componente, vengono copiate tutte le proprietà della partizione associate, ad eccezione dell'identità dell'applicazione o di uno dei membri di un ruolo.</span><span class="sxs-lookup"><span data-stu-id="2d63b-107">When a COM+ application or a component is copied, all associated partition properties are copied with it, except the application's identity or any of the members of a role.</span></span>

<span data-ttu-id="2d63b-108">Quando il programma client chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) per creare un'istanza di un oggetto, com+ esegue due passaggi distinti, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2d63b-108">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function to instantiate an object, COM+ performs two distinct steps, as follows:</span></span>

1.  <span data-ttu-id="2d63b-109">Individua la partizione in cui risiede il componente</span><span class="sxs-lookup"><span data-stu-id="2d63b-109">Locates the partition in which the component resides</span></span>
2.  <span data-ttu-id="2d63b-110">Individua il componente corretto all'interno della partizione</span><span class="sxs-lookup"><span data-stu-id="2d63b-110">Locates the correct component within that partition</span></span>

<span data-ttu-id="2d63b-111">Negli argomenti seguenti di questa sezione vengono descritti in dettaglio i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d63b-111">The following topics in this section describe these steps in detail:</span></span>

-   [<span data-ttu-id="2d63b-112">Individuazione delle partizioni durante l'attivazione</span><span class="sxs-lookup"><span data-stu-id="2d63b-112">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
-   [<span data-ttu-id="2d63b-113">Individuazione di un componente per l'attivazione</span><span class="sxs-lookup"><span data-stu-id="2d63b-113">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)

## <a name="related-topics"></a><span data-ttu-id="2d63b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d63b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d63b-115">Limitazioni relative alla progettazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="2d63b-115">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="2d63b-116">Componenti e partizioni in coda COM+</span><span class="sxs-lookup"><span data-stu-id="2d63b-116">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="2d63b-117">Implementazione della partizione</span><span class="sxs-lookup"><span data-stu-id="2d63b-117">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="2d63b-118">Che cosa sono le partizioni COM+?</span><span class="sxs-lookup"><span data-stu-id="2d63b-118">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 

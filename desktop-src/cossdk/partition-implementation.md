---
description: Quando viene installato in un server applicazioni, COM+ crea automaticamente una partizione, nota come partizione globale.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementazione della partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305135"
---
# <a name="partition-implementation"></a><span data-ttu-id="7ad0b-103">Implementazione della partizione</span><span class="sxs-lookup"><span data-stu-id="7ad0b-103">Partition Implementation</span></span>

<span data-ttu-id="7ad0b-104">Quando viene installato in un server applicazioni, COM+ crea automaticamente una partizione, nota come *partizione globale*.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-104">When installed on an application server, COM+ automatically creates a partition, known as the *global partition*.</span></span> <span data-ttu-id="7ad0b-105">La partizione globale include un set standard di applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-105">The global partition includes a standard set of COM+ applications.</span></span> <span data-ttu-id="7ad0b-106">Le applicazioni COM+ installate nella partizione globale sono automaticamente disponibili per tutti gli utenti del server.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-106">COM+ applications that are installed in the global partition are automatically available to all users on the server.</span></span> <span data-ttu-id="7ad0b-107">Se si dispone di altre applicazioni COM+ che si desidera rendere disponibili a tutti gli utenti del server, è possibile aggiungerle alla partizione globale.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-107">If you have other COM+ applications that you would like to make available to all users on the server, you can add them into the global partition.</span></span>

<span data-ttu-id="7ad0b-108">Oltre alla partizione globale, è possibile creare altre partizioni solo per gli utenti del server o per gli utenti di tutto il dominio.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-108">In addition to the global partition, you can create other partitions for users on that server only, or for users throughout the domain.</span></span> <span data-ttu-id="7ad0b-109">La creazione di partizioni aggiuntive e l'installazione di più configurazioni di un'applicazione COM+ consentono agli utenti di eseguire contemporaneamente tali configurazioni di applicazioni nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-109">Creating additional partitions and installing multiple configurations of a COM+ application into them allows your users to execute those application configurations simultaneously on the same computer.</span></span> <span data-ttu-id="7ad0b-110">Inoltre, l'installazione di applicazioni COM+ in una partizione diversa dalla partizione globale consente di controllare l'accesso degli utenti a tali applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-110">Also, by installing COM+ applications into a partition other than the global partition, you can control user access to those applications.</span></span>

<span data-ttu-id="7ad0b-111">**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-111">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="7ad0b-112">La partizione globale è l'unica partizione COM+ disponibile.</span><span class="sxs-lookup"><span data-stu-id="7ad0b-112">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="7ad0b-113">Per ulteriori informazioni sulle partizioni e le partizioni locali definite in Active Directory, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ad0b-113">For more information on local partitions and partitions defined within Active Directory, see the following topics:</span></span>

-   [<span data-ttu-id="7ad0b-114">Partizioni locali</span><span class="sxs-lookup"><span data-stu-id="7ad0b-114">Local Partitions</span></span>](local-partitions.md)
-   [<span data-ttu-id="7ad0b-115">Partizioni e Active Directory</span><span class="sxs-lookup"><span data-stu-id="7ad0b-115">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
-   [<span data-ttu-id="7ad0b-116">Partizioni predefinite</span><span class="sxs-lookup"><span data-stu-id="7ad0b-116">Default Partitions</span></span>](default-partitions.md)
-   [<span data-ttu-id="7ad0b-117">Partizione globale</span><span class="sxs-lookup"><span data-stu-id="7ad0b-117">The Global Partition</span></span>](the-global-partition.md)
-   [<span data-ttu-id="7ad0b-118">Proprietà partizione</span><span class="sxs-lookup"><span data-stu-id="7ad0b-118">Partition Properties</span></span>](partition-properties.md)

## <a name="related-topics"></a><span data-ttu-id="7ad0b-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ad0b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ad0b-120">Limitazioni relative alla progettazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="7ad0b-120">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="7ad0b-121">Componenti e partizioni in coda COM+</span><span class="sxs-lookup"><span data-stu-id="7ad0b-121">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="7ad0b-122">Registrazione e attivazione di componenti nelle partizioni</span><span class="sxs-lookup"><span data-stu-id="7ad0b-122">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="7ad0b-123">Che cosa sono le partizioni COM+?</span><span class="sxs-lookup"><span data-stu-id="7ad0b-123">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 




---
description: Partizioni predefinite
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Partizioni predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225780"
---
# <a name="default-partitions"></a><span data-ttu-id="e3e75-103">Partizioni predefinite</span><span class="sxs-lookup"><span data-stu-id="e3e75-103">Default Partitions</span></span>

<span data-ttu-id="e3e75-104">Quando a un utente viene assegnata una partizione predefinita, COM+ tenta innanzitutto di attivare i componenti in tale partizione.</span><span class="sxs-lookup"><span data-stu-id="e3e75-104">When a default partition is assigned to a user, COM+ attempts to activate components in that partition first.</span></span> <span data-ttu-id="e3e75-105">Se l'attivazione non riesce, COM+ cerca la partizione globale affinché il componente venga attivato.</span><span class="sxs-lookup"><span data-stu-id="e3e75-105">If the activation fails, COM+ searches the global partition for the component to activate.</span></span> <span data-ttu-id="e3e75-106">L'eccezione a questo processo si verifica quando il componente COM+ include un moniker di partizione che specifica in modo esplicito la partizione in cui si trova il componente.</span><span class="sxs-lookup"><span data-stu-id="e3e75-106">The exception to this process occurs when the COM+ component includes a partition moniker, which explicitly specifies the partition in which the component is located.</span></span> <span data-ttu-id="e3e75-107">In questo caso, il moniker della partizione ha la precedenza su qualsiasi configurazione di partizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e3e75-107">In this case, the partition moniker takes precedence over any default partition configuration.</span></span>

<span data-ttu-id="e3e75-108">Quando si utilizzano partizioni locali, la partizione predefinita viene assegnata agli utenti che utilizzano la cartella **com+ Partition Users** nello strumento di amministrazione Servizi componenti nel server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e3e75-108">When using local partitions, the default partition is assigned to users using the **COM+ Partition Users** folder in the Component Services administrative tool on the application server.</span></span> <span data-ttu-id="e3e75-109">Quando si usano i set di partizioni nella Active Directory, la partizione predefinita dell'utente è determinata dal set di partizioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e3e75-109">When using partition sets in the Active Directory, the user's default partition is determined by the user's partition set.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3e75-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3e75-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3e75-111">Partizioni locali</span><span class="sxs-lookup"><span data-stu-id="e3e75-111">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="e3e75-112">Proprietà partizione</span><span class="sxs-lookup"><span data-stu-id="e3e75-112">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="e3e75-113">Partizioni e Active Directory</span><span class="sxs-lookup"><span data-stu-id="e3e75-113">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="e3e75-114">Partizione globale</span><span class="sxs-lookup"><span data-stu-id="e3e75-114">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 




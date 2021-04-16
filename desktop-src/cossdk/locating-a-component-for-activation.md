---
description: Individuazione di un componente per l'attivazione
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Individuazione di un componente per l'attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104556574"
---
# <a name="locating-a-component-for-activation"></a><span data-ttu-id="7402f-103">Individuazione di un componente per l'attivazione</span><span class="sxs-lookup"><span data-stu-id="7402f-103">Locating a Component for Activation</span></span>

<span data-ttu-id="7402f-104">Quando COM+ individua la partizione corretta, tramite il set di partizioni predefinito dell'identità utente, un moniker di partizione o l'ID di partizione nel contesto dell'oggetto, COM + deve quindi individuare il componente corretto all'interno della partizione.</span><span class="sxs-lookup"><span data-stu-id="7402f-104">When COM+ has located the correct partition—through the user identity's default partition set, a partition moniker, or the partition ID in the object's context—COM+ must then locate the correct component within that partition.</span></span> <span data-ttu-id="7402f-105">Nella figura seguente viene illustrato come viene individuato e attivato un componente quando tale componente risiede in una partizione.</span><span class="sxs-lookup"><span data-stu-id="7402f-105">The following illustration shows how a component is found and activated when that component resides in a partition.</span></span>

> [!Note]  
> <span data-ttu-id="7402f-106">Prima dell'attivazione di un componente, COM+ esegue una convalida per verificare che l'identità utente che tenta di attivare il componente disponga dei diritti di accesso al set di partizioni in cui risiede il componente.</span><span class="sxs-lookup"><span data-stu-id="7402f-106">Prior to any component activation, COM+ performs a validation to verify that the user identity attempting to activate the component has rights to access the partition set in which the component resides.</span></span>

 

![Diagramma che mostra un albero per la risoluzione dei problemi per l'individuazione di un componente per l'attivazione.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

<span data-ttu-id="7402f-108">L'illustrazione precedente mostra quanto segue:</span><span class="sxs-lookup"><span data-stu-id="7402f-108">The preceding illustration shows the following:</span></span>

-   <span data-ttu-id="7402f-109">Se il componente chiamato risiede in una partizione e si trova nella stessa applicazione del componente chiamante, il componente viene attivato se il componente chiamato è contrassegnato come pubblico o privato.</span><span class="sxs-lookup"><span data-stu-id="7402f-109">If the component being called resides in a partition and is in the same application as the calling component, the component is activated whether the component being called is marked as public or private.</span></span>
-   <span data-ttu-id="7402f-110">Se il componente chiamato si trova in una partizione ma non esiste nella stessa applicazione del componente chiamante, COM+ verifica se il componente è contrassegnato come Public.</span><span class="sxs-lookup"><span data-stu-id="7402f-110">If the component being called resides in a partition but does not exist in the same application as the calling component, COM+ checks to see whether the component is marked as public.</span></span> <span data-ttu-id="7402f-111">Se non viene trovata alcuna versione pubblica, COM+ esegue una ricerca nella partizione globale per trovare una versione pubblica del componente.</span><span class="sxs-lookup"><span data-stu-id="7402f-111">If no public version is found, COM+ searches the Global Partition to find a public version of the component.</span></span> <span data-ttu-id="7402f-112">Se non viene trovata alcuna versione pubblica del componente nella partizione globale o se l'identità dell'utente non dispone di diritti per la partizione, l'attivazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7402f-112">If no public version of the component is found in the Global Partition or if the user identity has no rights to the partition, the activation fails.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7402f-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7402f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7402f-114">Individuazione delle partizioni durante l'attivazione</span><span class="sxs-lookup"><span data-stu-id="7402f-114">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
</dt> </dl>

 

 




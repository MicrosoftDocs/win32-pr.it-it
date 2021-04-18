---
description: Non è possibile dichiarare dinamicamente le risorse del buffer di vertex o del buffer gestito specificando \_ la dinamica D3DUSAGE al momento della creazione.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Risorse Application-Managed e strategie di allocazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304551"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a><span data-ttu-id="68623-103">Risorse Application-Managed e strategie di allocazione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="68623-103">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>

<span data-ttu-id="68623-104">Non è possibile dichiarare dinamicamente le risorse del buffer di vertex o del buffer gestito specificando \_ la dinamica D3DUSAGE al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="68623-104">Managed vertex-buffer or index-buffer resources cannot be declared dynamic by specifying D3DUSAGE\_DYNAMIC at creation time.</span></span> <span data-ttu-id="68623-105">Questa operazione richiede una copia aggiuntiva per ogni modifica apportata al contenuto del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="68623-105">This would require an additional copy for every modification to the vertex buffer contents.</span></span> <span data-ttu-id="68623-106">I buffer dei vertici dinamici sono progettati per il rendering di geometria dinamica e dati estratti da alberi partizionati di spazio binario o altre strutture di dati di visibilità.</span><span class="sxs-lookup"><span data-stu-id="68623-106">Dynamic vertex buffers are intended for rendering dynamic geometry and data pulled in from binary space partitioned trees or other visibility data structures.</span></span> <span data-ttu-id="68623-107">Questa operazione può essere eseguita tramite la pre-allocazione dei buffer del formato desiderato.</span><span class="sxs-lookup"><span data-stu-id="68623-107">This can be accomplished by pre-allocating buffers of the desired format.</span></span> <span data-ttu-id="68623-108">Queste risorse vengono quindi suddivise per supportare le esigenze dell'applicazione da parte di un gestore di risorse all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68623-108">These resources are then parceled out to support application needs by a resource manager within the application.</span></span> <span data-ttu-id="68623-109">Il numero totale di buffer dei vertici dinamici è ridotto perché un'applicazione utilizzerà simultaneamente solo alcuni stride del vertice diversi e perché è necessario un buffer del vertice diverso solo per gli stride univoci.</span><span class="sxs-lookup"><span data-stu-id="68623-109">The total number of dynamic vertex buffers is small because an application will use simultaneously only a few different vertex strides and because a different vertex buffer is required only for unique strides.</span></span> <span data-ttu-id="68623-110">Quando si gestiscono le risorse dinamiche in questo modo, assicurarsi che le richieste con frequenza elevata sulle risorse non diminuiscano in modo significativo le prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68623-110">When managing dynamic resources in this way, ensure that high-frequency demands on the resources do not significantly decrease the application's performance.</span></span>

<span data-ttu-id="68623-111">Quando si usano risorse gestite da Direct3D e dalle applicazioni, allocare risorse gestite dall'applicazione nella \_ memoria predefinita di D3DPOOL prima di creare risorse gestite da Direct3D.</span><span class="sxs-lookup"><span data-stu-id="68623-111">When using resources managed by both Direct3D and applications, allocate application-managed resources in D3DPOOL\_DEFAULT memory prior to creating Direct3D-managed resources.</span></span> <span data-ttu-id="68623-112">Questo consente al gestore della memoria di mantenere un conteggio accurato della memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="68623-112">This enables the memory manager to maintain an accurate count of available memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68623-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68623-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68623-114">Risorse Direct3D</span><span class="sxs-lookup"><span data-stu-id="68623-114">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 




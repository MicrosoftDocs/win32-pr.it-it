---
title: BypassNegotiation
description: La chiave del registro di sistema BypassNegotiation determina se la negoziazione delle funzionalità tra il server e il client si verifica o se vengono utilizzate impostazioni preconfigurate.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398358"
---
# <a name="bypassnegotiation"></a><span data-ttu-id="2628b-103">BypassNegotiation</span><span class="sxs-lookup"><span data-stu-id="2628b-103">BypassNegotiation</span></span>

<span data-ttu-id="2628b-104">La chiave del registro di sistema BypassNegotiation determina se la negoziazione delle funzionalità tra il server e il client si verifica o se vengono utilizzate impostazioni preconfigurate.</span><span class="sxs-lookup"><span data-stu-id="2628b-104">The BypassNegotiation registry key determines if capabilities negotiation between the server and client occurs or if pre-configured settings are used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2628b-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="2628b-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a><span data-ttu-id="2628b-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="2628b-106">Remarks</span></span>

<span data-ttu-id="2628b-107">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2628b-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="2628b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2628b-108">Value</span></span>   | <span data-ttu-id="2628b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2628b-109">Description</span></span>                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2628b-110">0</span><span class="sxs-lookup"><span data-stu-id="2628b-110">0</span></span>       | <span data-ttu-id="2628b-111">Server e client negoziano le funzionalità EAP.</span><span class="sxs-lookup"><span data-stu-id="2628b-111">Server and client negotiate EAP capabilities.</span></span>                                                                                                                                                        |
| <span data-ttu-id="2628b-112">diverso da zero</span><span class="sxs-lookup"><span data-stu-id="2628b-112">nonzero</span></span> | <span data-ttu-id="2628b-113">Server e client non negoziano le funzionalità EAP.</span><span class="sxs-lookup"><span data-stu-id="2628b-113">Server and client do not negotiate EAP capabilities.</span></span> <span data-ttu-id="2628b-114">Server e client utilizzano il valore della chiave del registro di sistema [AssumePhase2Fragmentation](assumephase2fragmentation.md) per trovare le funzionalità dell'altra parte.</span><span class="sxs-lookup"><span data-stu-id="2628b-114">Server and client use the [AssumePhase2Fragmentation](assumephase2fragmentation.md) registry key value to find the other party's capabilities.</span></span> |



 

<span data-ttu-id="2628b-115">Se il valore del registro di sistema non è presente, il server e il client negoziano le funzionalità EAP.</span><span class="sxs-lookup"><span data-stu-id="2628b-115">If this registry value is not present, the server and client negotiate EAP capabilities..</span></span>

## <a name="related-topics"></a><span data-ttu-id="2628b-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2628b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2628b-117">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="2628b-117">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 





---
title: AssumePhase2Fragmentation
description: La chiave del registro di sistema AssumePhase2Fragmentation determina se il server e il client presuppongono la frammentazione della fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398340"
---
# <a name="assumephase2fragmentation"></a><span data-ttu-id="29b52-103">AssumePhase2Fragmentation</span><span class="sxs-lookup"><span data-stu-id="29b52-103">AssumePhase2Fragmentation</span></span>

<span data-ttu-id="29b52-104">La chiave del registro di sistema AssumePhase2Fragmentation determina se il server e il client presuppongono la frammentazione della fase 2.</span><span class="sxs-lookup"><span data-stu-id="29b52-104">The AssumePhase2Fragmentation registry key determines if the server and client assume phase 2 fragmentation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="29b52-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="29b52-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a><span data-ttu-id="29b52-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="29b52-106">Remarks</span></span>

<span data-ttu-id="29b52-107">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="29b52-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="29b52-108">Valore</span><span class="sxs-lookup"><span data-stu-id="29b52-108">Value</span></span>   | <span data-ttu-id="29b52-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29b52-109">Description</span></span>                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b52-110">0</span><span class="sxs-lookup"><span data-stu-id="29b52-110">0</span></span>       | <span data-ttu-id="29b52-111">Server e client presuppongono che l'altra parte non sia in grado di deframmentare la fase 2 durante l'autenticazione PEAP.</span><span class="sxs-lookup"><span data-stu-id="29b52-111">Server and client assume the other party is not capable of phase 2 fragmentation during PEAP authentication.</span></span> |
| <span data-ttu-id="29b52-112">diverso da zero</span><span class="sxs-lookup"><span data-stu-id="29b52-112">nonzero</span></span> | <span data-ttu-id="29b52-113">Server e client presuppongono che l'altra parte sia in grado di deframmentare la fase 2 durante l'autenticazione PEAP.</span><span class="sxs-lookup"><span data-stu-id="29b52-113">Server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>     |



 

<span data-ttu-id="29b52-114">Se il valore del registro di sistema non è presente, il server e il client presuppongono che l'altra parte sia in grado di la frammentazione della fase 2 durante l'autenticazione PEAP.</span><span class="sxs-lookup"><span data-stu-id="29b52-114">If this registry value is not present, the server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29b52-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29b52-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29b52-116">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="29b52-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 





---
title: Architettura di memoria unificata
description: L'esecuzione di query per determinare se l'architettura di memoria unificata (UMA) è supportata può contribuire a determinare come gestire alcune risorse.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955221"
---
# <a name="unified-memory-architecture"></a><span data-ttu-id="03188-103">Architettura di memoria unificata</span><span class="sxs-lookup"><span data-stu-id="03188-103">Unified Memory Architecture</span></span>

<span data-ttu-id="03188-104">L'esecuzione di query per determinare se l'architettura di memoria unificata (UMA) è supportata può contribuire a determinare come gestire alcune risorse.</span><span class="sxs-lookup"><span data-stu-id="03188-104">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span>

<span data-ttu-id="03188-105">È possibile leggere un valore booleano, impostato dal driver, dalla [**struttura \_ d3d11 \_ data \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) per determinare se l'hardware supporta la funzionalità uma.</span><span class="sxs-lookup"><span data-stu-id="03188-105">A boolean, set by the driver, can be read from the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure to determine if the hardware supports UMA.</span></span>

<span data-ttu-id="03188-106">Per le applicazioni in esecuzione su UMA potrebbe essere necessario disporre di più risorse con accesso alla CPU abilitato rispetto a quando non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="03188-106">Applications running on UMA may want to have more resources with CPU access enabled than if it is not available.</span></span> <span data-ttu-id="03188-107">UMA consente alle applicazioni di evitare la copia dei dati delle risorse, anziché rimanere efficienti esclusivamente per schede grafiche non UMA.</span><span class="sxs-lookup"><span data-stu-id="03188-107">UMA enables applications to avoiding copying resource data around, instead of staying efficient solely for non-UMA graphics adapters.</span></span> [<span data-ttu-id="03188-108">Funzionalità di Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="03188-108">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)

## <a name="related-topics"></a><span data-ttu-id="03188-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03188-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03188-110">Funzionalità di Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="03188-110">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 





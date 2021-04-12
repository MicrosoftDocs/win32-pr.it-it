---
description: Le primitive che si trovano parzialmente all'interno o completamente al di fuori della vista tronco possono essere ritagliate in modo che venga eseguito il rendering solo della parte visibile della primitiva.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: Stato di ritaglio primitivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401341"
---
# <a name="primitive-clipping-state-direct3d-9"></a><span data-ttu-id="851e8-103">Stato di ritaglio primitivo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="851e8-103">Primitive Clipping State (Direct3D 9)</span></span>

<span data-ttu-id="851e8-104">Le primitive che si trovano parzialmente all'interno o completamente al di fuori della [vista tronco](viewports-and-clipping.md) possono essere ritagliate in modo che venga eseguito il rendering solo della parte visibile della primitiva.</span><span class="sxs-lookup"><span data-stu-id="851e8-104">Primitives that lie partially inside (or completely outside) the [view frustum](viewports-and-clipping.md) can be clipped so that only the visible portion of the primitive will be rendered.</span></span> <span data-ttu-id="851e8-105">Il ritaglio riduce la quantità di lavoro eseguita solo per le primitive o parti di una primitiva che saranno visibili.</span><span class="sxs-lookup"><span data-stu-id="851e8-105">Clipping reduces the amount of work that is done to only those primitives or portions of a primitive that will be visible.</span></span>

<span data-ttu-id="851e8-106">Per usare la pipeline per il ritaglio, impostare lo \_ stato di rendering del ritaglio D3DRS su **true** (valore predefinito) per abilitare il ritaglio oppure su **false** per disabilitare il ritaglio Direct3D.</span><span class="sxs-lookup"><span data-stu-id="851e8-106">To use the pipeline for clipping, set the D3DRS\_CLIPPING render state to **TRUE** (the default value) to enable clipping, or to **FALSE** to disable Direct3D clipping.</span></span>

## <a name="related-topics"></a><span data-ttu-id="851e8-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="851e8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="851e8-108">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="851e8-108">Render States</span></span>](render-states.md)
</dt> </dl>

 

 




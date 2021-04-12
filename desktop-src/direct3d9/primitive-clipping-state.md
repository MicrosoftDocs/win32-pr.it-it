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
# <a name="primitive-clipping-state-direct3d-9"></a>Stato di ritaglio primitivo (Direct3D 9)

Le primitive che si trovano parzialmente all'interno o completamente al di fuori della [vista tronco](viewports-and-clipping.md) possono essere ritagliate in modo che venga eseguito il rendering solo della parte visibile della primitiva. Il ritaglio riduce la quantità di lavoro eseguita solo per le primitive o parti di una primitiva che saranno visibili.

Per usare la pipeline per il ritaglio, impostare lo \_ stato di rendering del ritaglio D3DRS su **true** (valore predefinito) per abilitare il ritaglio oppure su **false** per disabilitare il ritaglio Direct3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 




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
# <a name="unified-memory-architecture"></a>Architettura di memoria unificata

L'esecuzione di query per determinare se l'architettura di memoria unificata (UMA) è supportata può contribuire a determinare come gestire alcune risorse.

È possibile leggere un valore booleano, impostato dal driver, dalla [**struttura \_ d3d11 \_ data \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) per determinare se l'hardware supporta la funzionalità uma.

Per le applicazioni in esecuzione su UMA potrebbe essere necessario disporre di più risorse con accesso alla CPU abilitato rispetto a quando non è disponibile. UMA consente alle applicazioni di evitare la copia dei dati delle risorse, anziché rimanere efficienti esclusivamente per schede grafiche non UMA. [Funzionalità di Direct3D 11,3](direct3d-11-3-features.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 





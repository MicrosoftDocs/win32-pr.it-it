---
title: Assegnazione di pesi dei filtri
description: A ogni filtro in Windows Filtering Platform (WFP) è associato un peso, che viene usato durante l'arbitraggio dei filtri.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9042b15da0df5f81c71a32deb923369a54243854e86aeaed1ba30c7fc8484193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746871"
---
# <a name="filter-weight-assignment"></a>Assegnazione di pesi dei filtri

A ogni filtro in Windows Filtering Platform (WFP) è associato un peso, che viene usato durante l'arbitraggio [dei filtri.](filter-arbitration.md)

Il peso del filtro usato dal Base Filtering Engine (BFE) è di tipo [**FWP \_ UINT64.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) I chiamanti hanno tre opzioni per l'aggiunta di filtri.

-   Impostare il peso su un [**\_ UINT64 FWP.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) BFE usa il peso fornito così come è.
-   Impostare il peso su [**FWP \_ EMPTY.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) BFE genera automaticamente un peso compreso \[ nell'intervallo 0, 2⁶⁰).
-   Imposta lo spessore su un [**\_ UINT8 FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) nell'intervallo \[ 0, 15 \] . BFE usa il peso fornito come identificatore dell'intervallo di peso.

    BFE genera automaticamente i 60 bit meno elevati (esattamente come se il peso fosse stato impostato su [**FWP \_ EMPTY)**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)e quindi usa il valore fornito per impostare i 4 bit più alti. In questo modo i chiamanti possono dividere manualmente lo spazio di ponderazione in 16 intervalli, pur continuando a usare la ponderazione automatica all'interno di un intervallo.

> [!Note]  
> Quando due o più callout vengono registrati nello stesso sottolivelli, possono verificarsi problemi quando lo stesso peso viene assegnato ai filtri. Questo problema può essere evitato facendo in modo che i callout creino un proprio sottolivetto [**usando FwpmSubLayerAdd0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori di peso del filtro**](filter-weight-identifiers.md)
</dt> </dl>

 

 





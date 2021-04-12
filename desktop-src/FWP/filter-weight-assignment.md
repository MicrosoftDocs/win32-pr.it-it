---
title: Assegnazione di pesi dei filtri
description: A ogni filtro della piattaforma filtro Windows è associato un peso, che viene utilizzato durante l'arbitraggio dei filtri.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/26/2020
ms.locfileid: "104398774"
---
# <a name="filter-weight-assignment"></a>Assegnazione di pesi dei filtri

A ogni filtro della piattaforma filtro Windows è associato un peso, che viene utilizzato durante l' [arbitraggio dei filtri](filter-arbitration.md).

Il peso del filtro utilizzato dal motore di filtro di base (BFE) è di tipo [**FWP \_ UInt64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Nei chiamanti sono disponibili tre opzioni per l'aggiunta di filtri.

-   Impostare il peso su un [**FWP \_ UInt64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). BFE usa il peso fornito così com'è.
-   Impostare Weight su [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). BFE genera automaticamente un peso compreso nell'intervallo \[ 0, 2 ⁶ ⁰).
-   Impostare il peso su un [**\_ Uint8 FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) nell'intervallo compreso tra \[ 0 e 15 \] . BFE usa il peso fornito come identificatore dell'intervallo di ponderazione.

    BFE genera automaticamente il 60 bit di ordine inferiore (esattamente come se il peso fosse stato impostato su [**FWP \_ vuoto**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), quindi usa il valore fornito per impostare i 4 bit più significativi. Ciò consente ai chiamanti di dividere manualmente lo spazio del peso in 16 intervalli, pur continuando a utilizzare la ponderazione automatica in un intervallo.

> [!Note]  
> Quando due o più callout sono registrati nello stesso sottolivello, possono verificarsi problemi quando lo stesso peso viene assegnato ai filtri. Questo problema può essere impedito facendo in modo che i callout creino il proprio sottolivello usando [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori di peso del filtro**](filter-weight-identifiers.md)
</dt> </dl>

 

 





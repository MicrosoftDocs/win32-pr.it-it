---
description: La certificazione incrociata consente alle entità in un'infrastruttura a chiave pubblica (PKI) di considerare attendibili le entità in un'altra infrastruttura a chiave pubblica.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificazione incrociata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644e5326f9d3b9f7cbe87290c044dea7f401f8a888fa3904afa162118a98d89b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904546"
---
# <a name="cross-certification"></a>Certificazione incrociata

La certificazione incrociata consente alle entità in un'infrastruttura a chiave pubblica (PKI) di considerare attendibili le entità in un'altra infrastruttura a chiave pubblica. Questa relazione di trust reciproco è in genere supportata da un contratto di certificazione incrociato tra le autorità di certificazione (CA) in ogni infrastruttura pKI. Il contratto stabilisce le responsabilità e la responsabilità di ogni parte.

Una relazione di trust reciproco tra due CA richiede che ogni AUTORITÀ di certificazione eserciti un certificato all'altra per stabilire la relazione in entrambe le direzioni. Il percorso di attendibilità non è gerarchico (nessuna delle AUTORITÀ di certificazione è subordinata all'altra) anche se le PKI separate possono essere gerarchie di certificati. Dopo che due CA hanno stabilito e specificato le condizioni di attendibilità e i certificati rilasciati tra loro, le entità all'interno di PKIs separate possono interagire in base ai criteri specificati nei certificati.

![diagramma di certificazione incrociata](images/cross-certification.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli di attendibilità](about-trust-models.md)
</dt> </dl>

 

 




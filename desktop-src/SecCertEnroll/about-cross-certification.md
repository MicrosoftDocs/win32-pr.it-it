---
description: La certificazione incrociata consente alle entità in un'infrastruttura a chiave pubblica (PKI) di considerare attendibili le entità in un'altra PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificazione incrociata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232664"
---
# <a name="cross-certification"></a>Certificazione incrociata

La certificazione incrociata consente alle entità in un'infrastruttura a chiave pubblica (PKI) di considerare attendibili le entità in un'altra PKI. Questa relazione di trust reciproco è in genere supportata da un contratto di certificazione incrociata tra le autorità di certificazione (CAs) in ogni infrastruttura PKI. Il contratto stabilisce le responsabilità e la responsabilità di ogni parte.

Una relazione di trust reciproca tra due ca richiede che ogni CA rilascia un certificato all'altro per stabilire la relazione in entrambe le direzioni. Il percorso di attendibilità non è gerarchico (nessuna delle CA di governance è subordinata all'altra) Sebbene il PKI separato possa essere costituito da gerarchie di certificati. Dopo che due CA hanno stabilito e specificato le condizioni di attendibilità e i certificati emessi tra loro, le entità all'interno del PKI separato possono interagire in base ai criteri specificati nei certificati.

![diagramma di certificazione incrociata](images/cross-certification.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli di attendibilità](about-trust-models.md)
</dt> </dl>

 

 




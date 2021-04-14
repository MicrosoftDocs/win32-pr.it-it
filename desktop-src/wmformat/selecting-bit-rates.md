---
title: Selezione delle velocità in bit
description: Selezione delle velocità in bit
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- profili, selezione velocità in bit
- profili, velocità in bit
- codec, scelta della velocità in bit
- codec, velocità in bit
- profili, selezione velocità in bit
- codec, selezione velocità in bit
- velocità in bit, selezione
- velocità in bit, profili
- velocità in bit, codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328239"
---
# <a name="selecting-bit-rates"></a>Selezione delle velocità in bit

Per i file che verranno trasmessi in rete, è necessario considerare attentamente le velocità in bit da usare. Nella maggior parte dei casi è possibile aggiungere insieme la velocità in bit di tutti i flussi in un file per ottenere un'idea generale della larghezza di banda disponibile necessaria per lo streaming del file. Tuttavia, per ogni flusso è necessaria anche una certa quantità di overhead. Questo overhead è riepilogato nella tabella seguente.



| Intervallo di velocità in bit (Kbps) | Larghezza di banda aggiuntiva necessaria per l'overhead (Kbps) |
|-----------------------|---------------------------------------------------|
| da 10 a 16               | 3                                                 |
| 17-30               | 4                                                 |
| 31 – 45               | 5                                                 |
| 46 – 70               | 6                                                 |
| 71 – 225              | 7                                                 |
| >225               | 9                                                 |



 

Il sovraccarico normale necessario per un flusso non prende in considerazione le estensioni di unità dati. Ogni estensione di unità dati aggiunge alla dimensione dell'esempio a cui è collegato. A seconda del tipo di estensione dell'unità dati, questo può aumentare significativamente la velocità in bit per il flusso.

È inoltre necessario considerare che la larghezza di banda massima teorica disponibile su una connessione di rete non è una velocità in bit di destinazione pratica. La larghezza di banda media disponibile per una determinata connessione non è sufficiente per la capacità della larghezza di banda della connessione, a causa del traffico di rete e di molti altri fattori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Progettazione di profili**](designing-profiles.md)
</dt> </dl>

 

 





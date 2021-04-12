---
title: Codifica della velocità in bit costante (CBR)
description: Codifica della velocità in bit costante (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK, codifica CBR
- Windows Media Format SDK, velocità in bit costante (CBR)
- codec, codifica CBR
- codec, velocità in bit costante (CBR)
- velocità in bit costante (CBR)
- CBR (velocità in bit costante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396682"
---
# <a name="constant-bit-rate-cbr-encoding"></a>Codifica della velocità in bit costante (CBR)

La codifica della velocità in bit costante (CBR) è il metodo predefinito di codifica con Windows Media Format SDK. Quando si usa la codifica CBR, si specifica la velocità in bit di destinazione per un flusso e il codec usa qualsiasi quantità di compressione necessaria per ottenerlo.

Con la codifica CBR la velocità in bit e le dimensioni del flusso codificato sono note prima della codifica. Se, ad esempio, si codifica un brano di tre minuti a 32.000 bit al secondo, si è certi che le dimensioni del file saranno pari a circa 704 kilobyte (32.000 bps x 180 secondi/8 bit per byte/1.024). Si sa anche che la larghezza di banda necessaria per trasmettere il contenuto codificato è di circa 32.000 bit al secondo.

La codifica della velocità in bit variabile vincolata (descritta nella sezione seguente) consente anche di stabilire la velocità in bit prima della codifica, ma poiché la frequenza è variabile, il file risultante non può essere trasmesso in modo efficiente come un file codificato in modalità CBR. Con CBR, la velocità in bit nel tempo rimane sempre vicina alla velocità in bit media o di destinazione e la quantità di variazione può essere specificata.

Lo svantaggio della codifica CBR è che la qualità del contenuto codificato non sarà costante. Poiché alcuni contenuti sono più difficili da comprimere, le parti di un flusso CBR saranno di qualità inferiore rispetto ad altri. Un film tipico, ad esempio, presenta alcune scene piuttosto statiche e alcune scene che sono piene di azioni. Se si codifica un film usando CBR, le scene statiche e pertanto semplici da codificare in modo efficiente saranno di qualità superiore rispetto a quelle delle azioni, che risultano molto più difficili da codificare in modo efficiente.

La codifica CBR può anche causare una qualità incoerente da un file a un altro. Se si usa CBR per codificare diversi brani di genere diversi alla stessa velocità in bit, è possibile notare una certa differenza di qualità tra di essi.

In generale, le variazioni nella qualità di un file CBR sono più pronunciate a velocità in bit inferiori. A una velocità in bit superiore, la qualità di un file con codifica CBR sarà comunque diversa, ma i problemi di qualità saranno meno evidenti per l'utente. Quando si usa la codifica CBR, è consigliabile impostare la larghezza di banda massima come consentito dallo scenario di recapito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scelta di un metodo di codifica**](choosing-an-encoding-method.md)
</dt> <dt>

[**Funzionalità di codec**](codec-features.md)
</dt> <dt>

[**Codifica della velocità in bit variabile (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 





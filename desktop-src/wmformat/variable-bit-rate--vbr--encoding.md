---
title: Codifica della velocità in bit variabile (VBR)
description: Codifica della velocità in bit variabile (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media Format SDK, codifica VBR
- Windows Media Format SDK, velocità in bit variabile (VBR)
- Windows Media Format SDK, codifica VBR basata sulla qualità
- Windows Media Format SDK, codifica VBR non vincolata
- Windows Media Format SDK, codifica VBR vincolata
- codec, codifica VBR
- codec, velocità in bit variabile (VBR)
- codec, codifica VBR basata sulla qualità
- codec, codifica VBR non vincolata
- codec, codifica VBR vincolata
- velocità in bit variabile (VBR), informazioni
- VBR (velocità in bit variabile), informazioni
- codifica VBR basata sulla qualità, informazioni
- codifica VBR non vincolata, informazioni
- codifica VBR vincolata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298917"
---
# <a name="variable-bit-rate-vbr-encoding"></a>Codifica della velocità in bit variabile (VBR)

La codifica con velocità in bit variabile (VBR) è un'alternativa a constant bit rate Encoding (CBR) ed è supportata da alcuni codec. Quando la codifica CBR si impegna a mantenere la velocità in bit del supporto codificato, VBR tenta di ottenere la migliore qualità possibile del supporto codificato.

La qualità del contenuto codificato dipende dalla quantità di dati persi durante la compressione e decompressione del contenuto. La perdita di dati durante il processo di compressione è influenzata da molti fattori, ma in genere a una maggiore la complessità dei dati originali e a un maggiore rapporto di compressione corrisponde una maggiore perdita di dettagli nel processo di compressione.

Sono disponibili tre tipi di codifica VBR: basata sulla qualità, non vincolata e vincolata.

## <a name="quality-based-vbr-encoding"></a>Codifica VBR basata sulla qualità

Il primo tipo di codifica VBR è basato sulla qualità, che usa un passaggio di codifica. La codifica VBR basata sulla qualità consente di specificare un livello di qualità per un flusso multimediale digitale anziché una velocità in bit. Il codec codifica quindi il contenuto in modo che tutti gli esempi siano di qualità paragonabile.

Il vantaggio principale della codifica VBR basata sulla qualità è che la qualità è coerente all'interno di un file e da un file a quello successivo. Ad esempio, è possibile scrivere un programma per copiare canzoni da CD a file ASF in un computer. In questo caso, la qualità coerente è probabilmente più importante per l'esperienza dell'utente finale rispetto alla dimensione del file coerente. L'uso della codifica VBR basata sulla qualità garantisce che tutti i brani copiati abbiano la stessa qualità.

Lo svantaggio della codifica VBR basata sulla qualità è che non esiste alcun modo per individuare i requisiti di larghezza di banda o di larghezza di banda del supporto codificato prima della codifica. Questo può rendere i file con codifica VBR basati sulla qualità inappropriati per le situazioni in cui la memoria o la larghezza di banda sono limitate, ad esempio lettori multimediali portatili o connessioni Internet a larghezza di banda ridotta.

In generale, la codifica VBR basata sulla qualità è particolarmente adatta per la riproduzione locale o connessioni di rete a larghezza di banda elevata. In questi casi, la qualità coerente offrirà un'esperienza utente migliore.

## <a name="unconstrained-vbr-encoding"></a>Codifica VBR non vincolata

La codifica VBR non vincolata usa due sessioni di codifica. Quando si usa la codifica VBR non vincolata, è possibile specificare una velocità in bit per il flusso, come si farebbe con la codifica CBR. Tuttavia, il codec usa questo valore solo come velocità in bit media per il flusso e codifica in modo che la qualità sia il più alto possibile mantenendo la media. La velocità in bit effettiva in qualsiasi punto del flusso codificato può variare considerevolmente dal valore medio.

Non viene impostata una finestra del buffer per la codifica VBR non vincolata come per un flusso con codifica CBR. Al contrario, il codec calcola le dimensioni della finestra del buffer necessaria in base ai requisiti degli esempi codificati.

Il vantaggio della codifica VBR non vincolata consiste nel fatto che il flusso compresso ha la qualità massima possibile rimanendo all'interno di una larghezza di banda media prevedibile.

## <a name="constrained-vbr-encoding"></a>Codifica VBR vincolata

La codifica VBR vincolata è identica alla codifica VBR non vincolata, con la differenza che si specifica una velocità in bit massima e una finestra massima del buffer nel profilo. Il codec usa quindi i valori massimi per determinare come comprimere i dati. Se si impostano i valori massimi a sufficienza, la codifica VBR vincolata produrrà lo stesso flusso codificato come codifica VBR non vincolata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scelta di un metodo di codifica**](choosing-an-encoding-method.md)
</dt> <dt>

[**Funzionalità di codec**](codec-features.md)
</dt> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Configurazione di flussi VBR**](configuring-vbr-streams.md)
</dt> <dt>

[**Codifica della velocità in bit costante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Codifica a due passaggi**](two-pass-encoding.md)
</dt> <dt>

[**Uso della codifica Two-Pass**](using-two-pass-encoding.md)
</dt> </dl>

 

 





---
title: Copia di Flussi usando esempi decompressi
description: Copia di Flussi usando esempi decompressi
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows MEDIA Format SDK, copia di flussi
- Advanced Systems Format (ASF), copia di flussi
- ASF (Advanced Systems Format), copia di flussi
- flussi, copia con dati decompressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e044d2a1d456c14c2e2d069e0a117ab6f6de218c062771da9c24bf887ddfdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848807"
---
# <a name="copying-streams-using-decompressed-samples"></a>Copia di Flussi usando esempi decompressi

È consigliabile non copiare flussi da un file a un altro usando esempi decompressi. Il processo di decompressione e ricompressione degli esempi comprimerà la qualità dell'output. Se è necessario decomprimere gli esempi e quindi copiarli in un altro flusso, è possibile riscontrare alcune difficoltà con i flussi codificati VBR (Quality-Based Variable Bit Rate).

Al termine della compressione di un flusso VBR basato sulla qualità, il codec registra la velocità in bit e la finestra del buffer del contenuto risultante. Quando si legge un file contenente un flusso codificato con VBR basato sulla qualità, il profilo ottenuto dal lettore annoterà la velocità in bit e la finestra del buffer, nonché la velocità in bit massima e la finestra del buffer massima. Questa configurazione nel profilo indica in genere un flusso di velocità in bit variabile vincolata a velocità in bit. Di conseguenza, quando si imposta il profilo nel writer, si prevede un passaggio di pre-elaborazione per il flusso, perché i flussi VBR vincolati a velocità in bit richiedono la codifica a due passi. È necessario considerare il flusso come se fosse un flusso VBR vincolato a velocità in bit e distribuire gli esempi per la pre-elaborazione. Poiché si usano i valori restituiti dopo la codifica del contenuto a un determinato livello di qualità, tali valori rappresentano il livello di qualità desiderato. Naturalmente, la qualità dell'output ri-codificato sarà comunque in qualche modo compromessa, come risultato della ri-codifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Copia di dati da un file a un altro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copia Flussi senza decomprimere i dati**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 





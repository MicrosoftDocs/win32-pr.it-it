---
title: Copia di flussi con esempi decompressi
description: Copia di flussi con esempi decompressi
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Media Format SDK, copia di flussi
- Formato di sistemi avanzati (ASF), copia dei flussi
- ASF (formato avanzato dei sistemi), copia dei flussi
- flussi, copia con dati decompressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298785"
---
# <a name="copying-streams-using-decompressed-samples"></a>Copia di flussi con esempi decompressi

Si consiglia vivamente di non copiare i flussi da un file a un altro usando campioni decompressi. Il processo di decompressione e ricompressione degli esempi ridurrà la qualità dell'output. Se è necessario decomprimere gli esempi e quindi copiarli in un altro flusso, è possibile che si verifichino alcune difficoltà con i flussi codificati della velocità in bit (VBR) basati sulla qualità.

Quando il codec termina la compressione di un flusso VBR basato sulla qualità, registra la velocità in bit e la finestra del buffer del contenuto risultante. Quando si legge un file contenente un flusso codificato con VBR basato sulla qualità, il profilo ottenuto dal lettore annoterà la velocità in bit e la finestra del buffer, nonché la velocità in bit massima e la finestra massima del buffer. Questa configurazione nel profilo indica normalmente un flusso di velocità in bit limitato a una velocità in bit. Di conseguenza, quando si imposta il profilo sul writer, è previsto un passaggio di pre-elaborazione per il flusso, perché i flussi VBR vincolati a velocità in bit richiedono la codifica in due passaggi. È consigliabile considerare il flusso come se fosse un flusso VBR vincolato a velocità in bit e recapitare gli esempi per la pre-elaborazione. Poiché si utilizzano i valori restituiti dopo la codifica del contenuto a un particolare livello di qualità, tali valori rappresentano il livello di qualità desiderato. Naturalmente, la qualità dell'output di cui è stato ricodificato sarà leggermente ridotta, in seguito alla nuova codifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Copia di dati da un file a un altro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copia dei flussi senza decomprimere i dati**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 





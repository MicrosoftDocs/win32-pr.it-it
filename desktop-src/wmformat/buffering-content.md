---
title: Buffering del contenuto
description: Buffering del contenuto
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK, memorizzazione nel buffer del contenuto
- buffering del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3005895f7a196073566c32bb455f5808bf6f11feb491000b140e1bbf88b94b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586991"
---
# <a name="buffering-content"></a>Buffering del contenuto

Quando l'oggetto lettore apre un file di streaming, determina le dimensioni del buffer in base alle impostazioni nell'intestazione del file. È possibile pensare al buffer come a un bucket con un foro nella parte inferiore che perde a una velocità costante. Se la velocità con cui viene riempito il bucket non è, in media, maggiore della velocità con cui si verifica la perdita, il bucket non causa mai un overflow.

La frequenza con cui il bucket immaginario perde è la velocità in bit del flusso. La velocità con cui il bucket si riempie è la velocità effettiva in bit del flusso. Le dimensioni dei dati in un flusso compresso variano da campione a campione a seconda della quantità di compressione ottenuta. Pertanto, anche se la velocità in bit del flusso è impostata nel profilo, rappresenta la velocità in bit media, non una costante.

L'altra impostazione di flusso importante per il processo di memorizzazione nel buffer è la finestra del buffer. La finestra del buffer viene misurata in tempo e specifica la quantità di contenuto che può essere memorizzata nel buffer. La capacità del bucket immaginario può essere trovata usando la finestra del buffer. Ad esempio, se si dispone di un flusso con una velocità in bit di 32 Kbps e una finestra del buffer di 3 secondi, il buffer viene ridimensionato in modo da contenere 3 secondi di contenuto a 32 Kbps o 12.000 byte (32.000 bit al secondo x 3 secondi/8 bit per byte). Il codec limita la variazione tra la velocità in bit di streaming effettiva dei campioni codificati in modo che, in un periodo di tempo uguale alla finestra del buffer, la velocità in bit media non sia maggiore della velocità in bit del flusso.

In genere, si impostano la frequenza in bit e la finestra del buffer per un flusso in un profilo e il writer gestisce il resto. Quando si passano esempi compressi al lettore, tuttavia, è necessario assicurarsi che i valori corretti siano trasferiti al nuovo file impostando la velocità in bit e la finestra del buffer per il flusso nel profilo di destinazione su valori del flusso compresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Esempi di supporti**](media-samples.md)
</dt> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 





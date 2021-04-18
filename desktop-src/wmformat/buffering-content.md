---
title: Contenuto del buffer
description: Contenuto del buffer
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK, contenuto del buffer
- contenuto del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297744"
---
# <a name="buffering-content"></a>Contenuto del buffer

Quando l'oggetto Reader apre un file di flusso, determina le dimensioni del buffer in base alle impostazioni nell'intestazione del file. È possibile considerare il buffer come un bucket con un foro nella parte inferiore che perde a una velocità costante. Fino a quando la velocità con cui viene riempito il bucket non è, in media, maggiore della frequenza con cui si verificano perdite, il bucket non verrà mai overflow.

La velocità con cui si verifica la perdita del bucket immaginaria è la velocità in bit del flusso. La velocità di riempimento del bucket è la velocità effettiva in bit del flusso. I dati in un flusso compresso variano a seconda della quantità di compressione conseguita, da campione a campione. Pertanto, anche se la velocità in bit del flusso è impostata nel profilo, rappresenta la velocità in bit media, non una costante.

L'altra impostazione di flusso importante per il processo di buffering è la finestra buffer. La finestra buffer viene misurata nel tempo e specifica la quantità di contenuto che può essere memorizzato nel buffer. È possibile trovare la capacità del bucket immaginario usando la finestra buffer. Se, ad esempio, si dispone di un flusso con una velocità in bit di 32 kbps e una finestra del buffer di 3 secondi, il buffer viene ridimensionato in modo da contenere 3 secondi di contenuto di 32 kbps o 12.000 byte (32.000 bit al secondo x 3 secondi/8 bit per byte). Il codec limita la variazione tra la velocità effettiva in bit di streaming dei campioni codificati, in modo che, in un periodo di tempo uguale alla finestra del buffer, la velocità in bit media non sia maggiore della velocità in bit del flusso.

In genere, è possibile impostare la velocità in bit e la finestra del buffer per un flusso in un profilo e il writer gestisce il resto. Quando si passano esempi compressi al lettore, tuttavia, è necessario assicurarsi che i valori corretti vengano trasferiti nel nuovo file impostando la velocità in bit e la finestra del buffer per il flusso nel profilo di destinazione sui valori del flusso compresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Esempi di supporti**](media-samples.md)
</dt> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 





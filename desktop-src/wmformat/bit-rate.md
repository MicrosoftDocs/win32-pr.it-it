---
title: Velocità in bit
description: Velocità in bit
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK, velocità in bit
- Advanced Systems Format (ASF), velocità in bit
- ASF (Advanced Systems Format),velocità in bit
- velocità in bit, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a15332e18d47a72974098ad38c6a942ceaf4780e1b79dffacd49382e3416ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809871"
---
# <a name="bit-rate"></a>Velocità in bit

La velocità in bit si riferisce alla quantità di dati al secondo che viene recapitata da un file ASF. Le misurazioni della velocità in bit sono in bit al secondo (bps) o kilobit al secondo (Kbps). La velocità in bit è spesso confusa con la larghezza di banda, che è una misura della capacità di trasferimento dei dati di una rete. La larghezza di banda viene misurata anche in bps e Kbps.

L Windows Media Format SDK può essere usato per creare applicazioni che forniscono flussi Windows contenuti basati su contenuti multimediali da percorsi Internet o Intranet. Quando si esegue lo streaming dei dati in una rete o in Internet, la velocità in bit è di importanza fondamentale per l'esperienza dell'utente finale. Se la larghezza di banda disponibile per la rete è inferiore alla velocità in bit del file ASF, la riproduzione del file verrà interrotta in qualche modo. In genere, una larghezza di banda insufficiente comporta l'omissione dei campioni o la sospensione della riproduzione mentre vengono memorizzati nel buffer più dati.

A ogni file ASF viene assegnato un valore di velocità in bit al momento della creazione, in base al tipo e al numero di flussi inclusi nel profilo usato. I singoli flussi hanno velocità in bit proprie. Le velocità in bit possono essere costanti (i dati originali vengono compressi in modo da mantenere un flusso costante di dati approssimativamente alla stessa velocità) o variabile (i dati originali vengono compressi in modo da mantenere la stessa qualità in tutto, anche se ciò può significare un flusso di dati non uniforme). Tipi di velocità in bit diversi possono essere applicati a flussi diversi all'interno dello stesso file.

È possibile codificare lo stesso contenuto in diversi flussi, ognuno con una velocità in bit diversa. È quindi possibile configurare i flussi in modo che si escludono a vicenda. In questo modo è possibile creare un singolo file che può essere trasmesso agli utenti con larghezze di banda diverse. Questa funzionalità è detta velocità in bit multipla, o MBR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Codifica CBR (Constant Bit Rate)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Profiles**](profiles.md)
</dt> <dt>

[**Codifica vbr (Variable Bit Rate)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 





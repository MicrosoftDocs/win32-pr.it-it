---
title: Velocità in bit
description: Velocità in bit
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK, velocità in bit
- ASF (Advanced Systems Format), velocità in bit
- ASF (formato avanzato dei sistemi), velocità in bit
- velocità in bit, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713711"
---
# <a name="bit-rate"></a>Velocità in bit

La velocità in bit si riferisce alla quantità di dati al secondo recapitati da un file ASF. Le misurazioni della velocità in bit sono in bit al secondo (BPS) o kilobit al secondo (Kbps). La velocità in bit è spesso confusa con la larghezza di banda, ovvero una misurazione della capacità di trasferimento dei dati di una rete. La larghezza di banda viene misurata anche in bps e kbps.

Windows Media Format SDK può essere usato per creare applicazioni che forniscono contenuti basati su Windows Media in streaming da percorsi Internet o Intranet. Quando si esegue il flusso di dati in una rete o in Internet, la velocità in bit è di importanza fondamentale per l'esperienza dell'utente finale. Se la larghezza di banda disponibile per la rete è inferiore alla velocità in bit del file ASF, la riproduzione del file verrà interrotta in qualche modo. In genere, la larghezza di banda insufficiente comporta l'omissione degli esempi o la sospensione della riproduzione mentre vengono memorizzati nel buffer più dati.

A ogni file ASF viene assegnato un valore di velocità in bit al momento della creazione, in base al tipo e al numero di flussi inclusi nel profilo utilizzato. I singoli flussi hanno una propria velocità in bit. Le velocità in bit possono essere costanti (i dati originali vengono compressi in modo da mantenere un flusso costante di dati alla stessa velocità) o variabile (i dati originali vengono compressi in modo da mantenere la stessa qualità in tutto, anche se questo potrebbe significare un flusso di dati non uniforme). È possibile applicare tipi di velocità in bit diversi a flussi diversi all'interno dello stesso file.

È possibile codificare lo stesso contenuto in più flussi diversi, ognuno con una velocità in bit diversa. È quindi possibile configurare i flussi in modo che si escludano a vicenda. Questo consente di creare un singolo file che può essere trasmesso a utenti con larghezze di banda diverse. Questa funzionalità è denominata velocità in bit multipla o MBR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Codifica della velocità in bit costante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Profili**](profiles.md)
</dt> <dt>

[**Codifica della velocità in bit variabile (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 





---
title: Per usare un flusso di script
description: Per usare un flusso di script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, flussi di script
- Formati di sistema avanzati (ASF), flussi di script
- ASF (formato avanzato dei sistemi), flussi di script
- flussi di script, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332556"
---
# <a name="to-use-a-script-stream"></a>Per usare un flusso di script

In questa sezione viene descritto come inviare i dati di script al writer per l'inclusione in un file. Per informazioni sull'inclusione di flussi di script nei profili, vedere [configurazione di tipi di flusso arbitrari](configuring-arbitrary-stream-types.md).

Ogni script è costituito da due stringhe, una stringa di *tipo* e una stringa di *argomento* .

I dati di script devono essere formattati prima di essere inviati al writer. Le stringhe devono essere concatenate, separate da un carattere **null** e terminate con un carattere **null** . Nell'esempio seguente viene illustrato uno script legittimo:



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | \\0 | h   | u   | u   | p   | :   | /   | /   | w   | w   | w   | .   | a   | d   | a   | u   | u   | m   | .   | c   | o   | m   | \\0 |



 

Ogni coppia di comandi di script deve essere scritta come esempio per il writer. Per ulteriori informazioni sulla scrittura di esempi, vedere [per scrivere esempi](to-write-samples.md).

Quando viene riprodotto il file ASF, i comandi di script vengono recapitati dal lettore (o dal lettore sincrono) nell'ordine temporale della presentazione. È responsabilità dell'applicazione analizzare le due stringhe e rispondere al comando script.

> [!Note]  
> Quando si usa il DRM per crittografare un file, nessun comando di script può avere un tempo di presentazione pari a 0.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di comandi script**](using-script-commands.md)
</dt> </dl>

 

 





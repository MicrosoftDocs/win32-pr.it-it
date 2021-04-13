---
title: Formati
description: Formati
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK, input
- Windows Media Format SDK, flussi
- Windows Media Format SDK, output
- Windows Media Format SDK, formati
- Advanced Systems Format (ASF), input
- ASF (formato avanzato dei sistemi), input
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- ASF (Advanced Systems Format), output
- ASF (formato avanzato dei sistemi), output
- Formato ASF (Advanced Systems Format), formati
- ASF (formato avanzato dei sistemi), formati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331487"
---
# <a name="formats"></a>Formati

Le informazioni in un formato descrivono tutti gli elementi necessari per conoscere un particolare tipo di supporto. Ogni formato ha un tipo principale, ad esempio audio o video, e può avere un sottotipo. I formati contengono informazioni diverse in base al tipo principale. I formati audio e video richiedono molto più informazioni rispetto ad altri tipi.

Proprio come gli oggetti di Windows Media Format SDK distinguono tra i numeri di input, i numeri di flusso e i numeri di output (vedere [input, flussi e](inputs-streams-and-outputs.md)output), esistono differenze importanti tra i formati di input, i formati di flusso e i formati di output. Queste differenze sono descritte di seguito:

## <a name="input-formats"></a>Formati di input

Un formato di input descrive i supporti digitali passati all'oggetto writer. Se un flusso in un file ASF viene compresso con un codec, il codec supporterà solo determinati formati di input. Quando si utilizzano i codec Windows Media Audio e video, è possibile enumerare i formati di input supportati utilizzando l'oggetto writer. Quando si scrive un file, si è responsabili della selezione di un formato di input corrispondente al supporto di input.

Sebbene il formato dei supporti di input debba essere supportato dal codec che comprimerà i dati, alcune impostazioni del formato di input non devono corrispondere al formato del flusso. Il formato di input per un flusso video, ad esempio, può avere dimensioni del frame diverse da quelle definite nel formato del flusso. In questi casi, il codec eseguirà le conversioni.

## <a name="stream-formats"></a>Formati di flusso

Un formato di flusso descrive il formato del supporto archiviato nel file ASF. Il formato del flusso è il formato descritto nel profilo e può essere uguale o meno al formato di input e di output. Se viene usato un codec per comprimere i dati in un flusso, il formato del flusso sarà diverso dai formati di input e di output.

Quando si usano i codec Windows Media Audio e video, è necessario ottenere un elenco di formati di flusso supportati dal codec per assicurarsi che non si stia tentando di specificare un formato non supportato dal codice. Alcune impostazioni di formato, ad esempio le dimensioni e la profondità dei colori di un frame video, devono essere configurate manualmente dopo aver recuperato il formato del codec.

## <a name="output-formats"></a>Formati di output

Un formato di output descrive i supporti digitali che il lettore (o il lettore sincrono) recapita alla propria applicazione. Se un flusso in un file ASF viene compresso con un codec, il codec supporterà solo determinati formati di output. Quando si usano i codec Windows Media Audio e video, è possibile enumerare i formati di output supportati usando l'oggetto Reader. Ogni codec Windows Media ha un formato di output predefinito, ma è possibile selezionare qualsiasi formato di output supportato per il recapito di esempio.

Sebbene il formato dei supporti di output debba essere supportato dal codec che ha compresso i dati, alcune impostazioni del formato di output non devono corrispondere al formato del flusso. Ad esempio, il formato di output per un flusso video potrebbe avere dimensioni del frame diverse da quelle definite nel formato del flusso. In questi casi, il codec eseguirà le conversioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> </dl>

 

 





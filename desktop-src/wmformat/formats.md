---
title: Formati
description: Formati
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows SDK formato multimediale,input
- Windows MEDIA Format SDK, flussi
- Windows Media Format SDK,outputs
- Windows MEDIA Format SDK, formati
- Advanced Systems Format (ASF), inputs
- ASF (Advanced Systems Format),inputs
- Advanced Systems Format (ASF), flussi
- ASF (Advanced Systems Format), flussi
- Advanced Systems Format (ASF), output
- ASF (Advanced Systems Format),outputs
- Advanced Systems Format (ASF), formati
- ASF (Advanced Systems Format),formati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10f217b9935926d7bd7d5cba9ac53e6834385685e4a0f87ea6ba713cc8ff70b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089691"
---
# <a name="formats"></a>Formati

Le informazioni in un formato descrivono tutte le informazioni necessarie su un particolare tipo di supporto. Ogni formato ha un tipo principale, ad esempio audio o video, e può avere un sottotipo. I formati contengono informazioni diverse in base al tipo principale. I formati audio e video richiedono molte più informazioni rispetto ad altri tipi.

Così come gli oggetti di Windows Media Format SDK distinguono tra numeri di input, numeri di flusso e numeri di output (vedere [Input, Flussi e Output),](inputs-streams-and-outputs.md)esistono importanti differenze tra i formati di input, i formati di flusso e i formati di output. Queste differenze sono descritte di seguito:

## <a name="input-formats"></a>Formati di input

Un formato di input descrive i supporti digitali passati all'oggetto writer. Se un flusso in un file ASF è compresso con un codec, il codec supporterà solo determinati formati di input. Quando si usa Windows codec Audio e Video multimediali, è possibile enumerare i formati di input supportati usando l'oggetto writer. Quando si scrive un file, si è responsabili della selezione di un formato di input corrispondente ai supporti di input.

Anche se il formato multimediale di input deve essere supportato dal codec che comprimerà i dati, alcune impostazioni del formato di input non devono corrispondere al formato del flusso. Ad esempio, il formato di input per un flusso video può avere una dimensione del fotogramma diversa da quella definita nel formato del flusso. Il codec eseguirà le conversioni in questi casi.

## <a name="stream-formats"></a>Formati di flusso

Un formato di flusso descrive il formato del supporto archiviato nel file ASF. Il formato del flusso è il formato descritto nel profilo e può essere uguale o meno al formato di input e di output. Se si usa un codec per comprimere i dati in un flusso, il formato del flusso sarà diverso dai formati di input e output.

Quando si usano i codec audio e video di Windows, è necessario ottenere un elenco dei formati di flusso supportati dal codec per assicurarsi che non si tenti di specificare un formato non supportato dal codice. Alcune impostazioni di formato, ad esempio le dimensioni e la profondità del colore di un fotogramma video, devono essere configurate manualmente dopo il recupero del formato codec.

## <a name="output-formats"></a>Formati di output

Un formato di output descrive i supporti digitali che il lettore (o lettore sincrono) recapita all'applicazione. Se un flusso in un file ASF è compresso con un codec, il codec supporterà solo determinati formati di output. Quando si usa Windows codec Audio e Video multimediali, è possibile enumerare i formati di output supportati usando l'oggetto reader. Ogni codec di Windows ha un formato di output predefinito, ma è possibile selezionare qualsiasi formato di output supportato per la distribuzione di campioni.

Anche se il formato multimediale di output deve essere supportato dal codec che ha compresso i dati, alcune impostazioni del formato di output non devono corrispondere al formato del flusso. Ad esempio, il formato di output per un flusso video può avere una dimensione del fotogramma diversa da quella definita nel formato di flusso. Il codec eseguirà le conversioni in questi casi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> </dl>

 

 





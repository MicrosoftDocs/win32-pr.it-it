---
description: Il flusso è il processo di gestione di una piccola parte di un file audio in memoria. Ciò consente di riprodurre file audio di grandi dimensioni, ad esempio la musica in background, e di non richiedere una grande quantità di memoria.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: Dati audio di streaming XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317840"
---
# <a name="xaudio2-streaming-audio-data"></a>Dati audio di streaming XAudio2

Il flusso è il processo di gestione di una piccola parte di un file audio in memoria. Ciò consente di riprodurre file audio di grandi dimensioni, ad esempio la musica in background, e di non richiedere una grande quantità di memoria.

Quando si esegue il flusso di un file audio, i relativi dati vengono letti dal disco in blocchi anziché caricare l'intero file in una sola volta. Il flusso viene eseguito in modo asincrono leggendo i dati audio in una coda di buffer del disco. Ogni buffer viene riempito e quindi inviato a una voce di origine. Quando la voce termina la riproduzione di un buffer, il buffer diventa disponibile per la lettura. Il ciclo dei buffer del disco in questo modo consente di riprodurre un file audio di grandi dimensioni mentre viene caricata solo una parte dei dati. Il codice di streaming deve essere inserito in un thread separato, in cui può essere sospeso durante l'attesa del completamento delle operazioni di disco e audio con esecuzione prolungata. Una classe di callback viene utilizzata per riattivare il thread attivando gli eventi quando le operazioni audio sono state completate.

Per un esempio di come è possibile eseguire lo streaming con XAudio2, vedere [procedura: trasmettere un suono dal disco](how-to--stream-a-sound-from-disk.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Streaming di dati audio](streaming-audio-data.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 




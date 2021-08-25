---
description: Lo streaming è il processo che consente di mantenere solo una piccola parte di un file audio in riproduzione in memoria. In questo modo è possibile riprodurre file audio di grandi dimensioni, ad esempio musica di sottofondo, senza richiedere una grande quantità di memoria.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: Dati audio di streaming XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df15420adce8f8807c3f969615a2cf6d5b51981e03fd7067e2c1c3348d1b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805391"
---
# <a name="xaudio2-streaming-audio-data"></a>Dati audio di streaming XAudio2

Lo streaming è il processo che consente di mantenere solo una piccola parte di un file audio in riproduzione in memoria. In questo modo è possibile riprodurre file audio di grandi dimensioni, ad esempio musica di sottofondo, senza richiedere una grande quantità di memoria.

Quando un file audio viene trasmesso, i relativi dati vengono letti dal disco in blocchi anziché caricare l'intero file contemporaneamente. Lo streaming viene ottenuto leggendo in modo asincrono i dati audio in una coda di buffer del disco. Ogni buffer viene riempito e quindi inviato a una voce di origine. Al termine della riproduzione di un buffer da parte della voce, il buffer diventa nuovamente disponibile per la lettura. L'esecuzione di cicli nei buffer del disco in questo modo consente la riproduzione di un file audio di grandi dimensioni mentre viene caricata solo una parte dei dati. Il codice di streaming deve essere inserito in un thread separato, in cui può essere messo in sospensione durante l'attesa del completamento delle operazioni audio e disco a esecuzione lunga. Una classe di callback viene usata per riattivare il thread attivando eventi al termine delle operazioni audio.

Per un esempio di come è possibile eseguire lo streaming con XAudio2, vedere Procedura: Trasmettere un [suono dal disco.](how-to--stream-a-sound-from-disk.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Streaming di dati audio](streaming-audio-data.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 




---
description: Illustra come usare le Microsoft Media Foundation decodificare l'audio da un file multimediale.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Esempio di clip audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f180dfb7c4b0e456f45169d36fdfb1f77701b0e82250690706208a715fdd3ce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035489"
---
# <a name="audio-clip-sample"></a>Esempio di clip audio

Illustra come usare le Microsoft Media Foundation decodificare l'audio da un file multimediale.

L'applicazione di esempio Audio Clip legge i dati audio da un file multimediale e scrive l'audio non compresso in un file WAVE.

## <a name="apis-demonstrated"></a>DIMOSTRAZIONE DELLE API

In questo esempio vengono illustrate le Media Foundation seguenti:

-   [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>Utilizzo

Questo esempio è un'applicazione della riga di comando. Usa gli argomenti della riga di comando seguenti:

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   inputfile: nome di un file che contiene un flusso audio.
-   outputfile.wav: nome del file WAVE da scrivere.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository github Windows esempi classici.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[Esercitazione: Decodifica dell'audio](tutorial--decoding-audio.md)
</dt> </dl>

 

 




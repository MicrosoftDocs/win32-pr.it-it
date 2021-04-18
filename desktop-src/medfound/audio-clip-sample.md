---
description: Viene illustrato come utilizzare Microsoft Media Foundation per decodificare l'audio da un file multimediale.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Esempio di clip audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305515"
---
# <a name="audio-clip-sample"></a>Esempio di clip audio

Viene illustrato come utilizzare Microsoft Media Foundation per decodificare l'audio da un file multimediale.

L'applicazione di esempio clip audio legge i dati audio da un file multimediale e scrive l'audio non compresso in un file WAVE.

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Media Foundation seguenti:

-   [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>Utilizzo

Questo esempio è un'applicazione della riga di comando. USA gli argomenti della riga di comando seguenti:

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   InputFile: nome di un file che contiene un flusso audio.
-   outputfile. wav: nome del file WAVE da scrivere.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[Esercitazione: decodifica audio](tutorial--decoding-audio.md)
</dt> </dl>

 

 




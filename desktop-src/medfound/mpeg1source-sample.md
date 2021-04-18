---
description: Esempio MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Esempio MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309072"
---
# <a name="mpeg1source-sample"></a>Esempio MPEG1Source

Viene illustrato come scrivere un'origine multimediale personalizzata in Microsoft Media Foundation. L'esempio implementa un'origine multimediale che analizza i flussi a livello di sistemi MPEG-1 e genera esempi che contengono payload MPEG-1.

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Media Foundation seguenti:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

Prima di esaminare questo esempio, è opportuno esaminare l' [esempio WavSource](wavsource-sample.md), che fornisce un'implementazione più semplice di un'origine multimediale. L'esempio MPEG1Source aggiunge alcune funzionalità che si trovano nella maggior parte delle implementazioni reali di un'origine multimediale:

-   Più flussi
-   Metodi asincroni
-   I/O asincrono

Nell'Windows SDK per Windows Server 2008, questo esempio include anche un decodificatore MPEG-1 video di esempio che Visualizza il codice temporale per ogni fotogramma video. Non decodifica effettivamente il Bitstream MPEG-1.

A partire da Windows SDK per Windows 7, il decodificatore è stato spostato in un esempio separato. Vedere [esempio di decodificatore](decoder-sample.md).

## <a name="usage"></a>Utilizzo

L'esempio MPEG1Source compila una DLL che è un server COM per l'origine del supporto, il gestore del flusso di byte dell'origine multimediale e il decodificatore MFT. Prima di usare l'origine del supporto, è necessario registrare la DLL.

Per usare l'origine del supporto, è possibile eseguire l' [esempio BasicPlayback](/previous-versions//bb970475(v=vs.85)). Il sistema di risoluzione di origine caricherà automaticamente l'origine del supporto se si seleziona un file MPEG-1 per la riproduzione. Se si verifica un errore, verificare che la DLL MPEG1Source sia stata registrata correttamente.

È anche possibile usare lo strumento TopoEdit per creare una topologia di riproduzione che contiene l'origine multimediale. Per ulteriori informazioni su TopoEdit, vedere [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Origini supporti](media-sources.md)
</dt> <dt>

[Gestori di schemi e gestori di Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Esercitazione: scrittura di un'origine multimediale personalizzata](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[Esempio WavSource](wavsource-sample.md)
</dt> </dl>

 

 

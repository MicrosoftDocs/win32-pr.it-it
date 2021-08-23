---
description: Esempio wavsource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Esempio wavsource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba8ab5bfd5ae1ccfb4df4c90b447c412e9e835a403d496834224f012f8bad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972540"
---
# <a name="wavsource-sample"></a>Esempio wavsource

Illustra come creare un'origine multimediale personalizzata in Microsoft Media Foundation. L'esempio implementa un'origine multimediale che analizza i file audio wav.

Questo esempio è un esempio relativamente semplice di un'origine multimediale:

-   È presente un solo flusso, quindi non è disponibile codice per implementare la selezione del flusso.
-   L'origine multimediale non implementa il controllo della frequenza, ovvero la riproduzione veloce in avanti o inversa.
-   Tutti i metodi di origine e flusso vengono implementati come metodi sincroni.
-   Poiché la parte di dati di un file wav è un singolo blocco di audio PCM non compresso, l'origine multimediale non deve leggere le intestazioni dei pacchetti o analizzare in altro modo il flusso durante la riproduzione, a parte la lettura dell'intestazione [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) iniziale.

Per un esempio più avanzato di un'origine multimediale, vedere [MPEG1Source Sample (Esempio MPEG1Source).](mpeg1source-sample.md)

## <a name="apis-demonstrated"></a>DIMOSTRAZIONE DELLE API

In questo esempio vengono illustrate le Media Foundation seguenti:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Utilizzo

L'esempio WavSource compila una DLL che è un server COM sia per l'origine multimediale che per il gestore del flusso di byte dell'origine multimediale. Prima di utilizzare l'origine supporto, è necessario registrare la DLL.

Per usare l'origine multimediale, è possibile eseguire [BasicPlayback.](/previous-versions//bb970475(v=vs.85)) Il resolver di origine carica automaticamente l'origine multimediale se si seleziona un file wav per la riproduzione. Se si verifica un errore, assicurarsi di aver registrato correttamente la DLL WavSource.

È anche possibile usare lo strumento TopoEdit per creare una topologia di riproduzione contenente l'origine multimediale. Per altre informazioni su TopoEdit, vedere [TopoEdit.](topoedit.md)

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository github Windows esempi classici.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Origini multimediali](media-sources.md)
</dt> <dt>

[Esempio MPEG1Source](mpeg1source-sample.md)
</dt> <dt>

[Gestori di schemi e Byte-Stream di schema](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Scrittura di un'origine multimediale personalizzata](writing-a-custom-media-source.md)
</dt> </dl>

 

 

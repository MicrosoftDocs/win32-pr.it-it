---
description: Esempio WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Esempio WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880566"
---
# <a name="wavsource-sample"></a>Esempio WavSource

Viene illustrato come creare un'origine multimediale personalizzata in Microsoft Media Foundation. Nell'esempio viene implementata un'origine multimediale che analizza i file audio WAV.

Questo esempio è un esempio relativamente semplice di un'origine multimediale:

-   Esiste un solo flusso, pertanto non è disponibile codice per implementare la selezione del flusso.
-   L'origine multimediale non implementa il controllo della frequenza, ovvero la riproduzione veloce o inversa.
-   Tutti i metodi source e Stream vengono implementati come metodi sincroni.
-   Poiché la parte relativa ai dati di un file WAV è costituita da un singolo blocco di audio PCM non compresso, non è necessario che l'origine supporti legga le intestazioni dei pacchetti né analizzi il flusso durante la riproduzione, oltre a leggere l'intestazione [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) iniziale.

Per un esempio più avanzato di un'origine multimediale, vedere l'esempio [MPEG1Source](mpeg1source-sample.md).

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Media Foundation seguenti:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Utilizzo

L'esempio WavSource compila una DLL che è un server COM per il gestore del flusso di byte di origine multimediale e di origine multimediale. Prima di usare l'origine del supporto, è necessario registrare la DLL.

Per usare l'origine del supporto, è possibile eseguire [BasicPlayback](/previous-versions//bb970475(v=vs.85)). Il resolver di origine caricherà automaticamente l'origine del supporto se si seleziona un file WAV per la riproduzione. Se si verifica un errore, verificare che la DLL WavSource sia stata registrata correttamente.

È anche possibile usare lo strumento TopoEdit per creare una topologia di riproduzione che contiene l'origine multimediale. Per ulteriori informazioni su TopoEdit, vedere [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Origini supporti](media-sources.md)
</dt> <dt>

[Esempio MPEG1Source](mpeg1source-sample.md)
</dt> <dt>

[Gestori di schemi e gestori di Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Scrittura di un'origine multimediale personalizzata](writing-a-custom-media-source.md)
</dt> </dl>

 

 

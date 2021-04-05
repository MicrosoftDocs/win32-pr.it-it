---
title: Per eseguire la transcodifica del contenuto con la ricompressione intelligente
description: Per eseguire la transcodifica del contenuto con la ricompressione intelligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Media Format SDK, codifica del contenuto
- Windows Media Format SDK, ricompressione intelligente
- Windows Media Format SDK, ricompressione
- Windows Media Format SDK, Windows Media Audio Codec
- ASF (Advanced Systems Format), codifica del contenuto
- ASF (formato avanzato dei sistemi), transcodifica del contenuto
- ASF (Advanced Systems Format), ricompressione intelligente
- ASF (formato avanzato dei sistemi), ricompressione intelligente
- ASF (Advanced Systems Format), ricompressione
- ASF (formato avanzato dei sistemi), ricompressione
- ASF (Advanced Systems Format), codec Windows Media Audio
- ASF (Advanced Systems Format), Windows Media Audio Codec
- transcodifica del contenuto
- ricompressione intelligente
- ricompressione
- Codec Windows Media Audio, transcodifica del contenuto
- codec, codec Windows Media Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336353"
---
# <a name="to-transcode-content-with-smart-recompression"></a>Per eseguire la transcodifica del contenuto con la ricompressione intelligente

È possibile transcodificare il contenuto da una velocità in bit a un'altra usando Windows Media Format SDK. In genere, ciò implica semplicemente la decodifica del contenuto e la codifica di nuovo nella velocità in bit desiderata. Il codec Windows Media Audio 9 supporta la ricompressione intelligente, che consente la transcodifica che ottiene una qualità migliore del normale.

Per la ricompressione intelligente, il flusso audio originale deve essere codificato con il codec Windows Media Audio. Sono supportate tutte le versioni del codec, ma i codec audio specializzati (Windows Media Audio 9 Professional e Windows Media Audio 9 Voice) non lo sono. Se l'audio originale è stato codificato con il codec di Windows Media Audio 9 senza perdita di dati, non è necessario usare la ricompressione intelligente perché non è stata persa alcuna informazione nella codifica originale.

Per usare la ricompressione intelligente, seguire questa procedura.

1.  Configurare un oggetto Reader con il file di origine per la lettura. Per ulteriori informazioni, vedere la pagina relativa alla [lettura di file ASF](reading-asf-files.md).
2.  Configurare un oggetto writer da usare per la transcodifica del file. Impostare il nome del file per il nuovo file. Selezionare un profilo da usare per il nuovo file. Imposta il profilo selezionato nell'oggetto writer. Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).
3.  Ottenere un puntatore all'interfaccia [**IWMProfile**](iwmprofile.md) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.
4.  Recuperare l'interfaccia [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) per il flusso audio da transcodificare chiamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).
5.  Ottenere l'interfaccia [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) per l'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.
6.  Recuperare la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il flusso effettuando due chiamate a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Ottenere le dimensioni della struttura alla prima chiamata e allocare la memoria per il passaggio di un buffer alla seconda chiamata.
7.  Ottenere un puntatore all'interfaccia [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) per l'input nel writer chiamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
8.  Ottenere l'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) per l'oggetto proprietà del supporto di input chiamando **IWMInputMediaProps:: QueryInterface**.
9.  Usare il metodo [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per impostare la proprietà g \_ wszOriginalWaveFormat. Utilizzare la struttura **WAVEFORMATEX** ottenuta nel passaggio 6 come valore della proprietà.
10. Includere le modifiche apportate alle proprietà del supporto di input chiamando [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passandogli un puntatore all'interfaccia **IWMInputMediaProps** .
11. Iniziare a leggere gli esempi dal file originale e passarli al writer con le chiamate a [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> <dt>

[**Interfaccia IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**Interfaccia IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interfaccia IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interfaccia IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**Interfaccia IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 





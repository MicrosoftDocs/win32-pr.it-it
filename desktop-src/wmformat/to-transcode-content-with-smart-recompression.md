---
title: Per transcodificare il contenuto con la ricompressione intelligente
description: Per transcodificare il contenuto con la ricompressione intelligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Media Format SDK, transcoding del contenuto
- Windows Media Format SDK, ricompressione intelligente
- Windows MEDIA Format SDK, recompression
- Windows Media Format SDK, Windows codec Audio multimediale
- Advanced Systems Format (ASF), transcodificare il contenuto
- ASF (Advanced Systems Format), transcodificare il contenuto
- Advanced Systems Format (ASF), ricompressione intelligente
- ASF (Advanced Systems Format), ricompressione intelligente
- Advanced Systems Format (ASF), recompression
- ASF (Advanced Systems Format), recompression
- Advanced Systems Format (ASF), Windows codec Audio multimediale
- ASF (Advanced Systems Format), Windows codec audio multimediali
- transcoding di contenuto
- ricompressione intelligente
- Ricompressione
- Windows Codec audio multimediali, transcodico contenuto
- codec, Windows codec Audio multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1cf363e196feca81ef9757f006b211758c2ff7fbdd1f50b5136992b394f8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699092"
---
# <a name="to-transcode-content-with-smart-recompression"></a>Per transcodificare il contenuto con la ricompressione intelligente

È possibile transcodificare il contenuto da una velocità in bit a un'altra usando Windows Media Format SDK. In genere, ciò comporta semplicemente la decodifica del contenuto e la codifica alla velocità in bit desiderata. Il Windows Media Audio 9 supporta la ricompressione intelligente, che consente la transcoduttura che ottiene una qualità migliore del normale.

Per la ricompressione intelligente, il flusso audio originale deve essere codificato con il codec Windows Audio multimediale. Tutte le versioni del codec sono supportate, ma i codec audio specializzati (Windows Media Audio 9 Professional e Windows Media Audio 9 Voice) non lo sono. Se l'audio originale è stato codificato con il codec Windows Media Audio 9 Lossless, non è necessario usare la ricompressione intelligente, perché nessuna informazione è stata persa nella codifica originale.

Per usare la ricompressione intelligente, seguire questa procedura.

1.  Configurare un oggetto lettore con il file di origine per la lettura. Per altre informazioni, vedere [Lettura di file ASF.](reading-asf-files.md)
2.  Configurare un oggetto writer da usare per la transcoding del file. Impostare il nome del file per il nuovo file. Selezionare un profilo da usare per il nuovo file. Impostare il profilo selezionato nell'oggetto writer. Per altre informazioni, vedere [Scrittura di file ASF.](writing-asf-files.md)
3.  Ottenere un puntatore [**all'interfaccia IWMProfile**](iwmprofile.md) dell'oggetto lettore chiamando **IWMReader::QueryInterface**.
4.  Recuperare [**l'interfaccia IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) per il flusso audio da transcodificare chiamando [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).
5.  Ottenere [**l'interfaccia IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) per l'oggetto di configurazione del flusso chiamando **IWMStreamConfig::QueryInterface**.
6.  Recuperare la [**struttura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il flusso effettuando due chiamate a [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Ottenere le dimensioni della struttura alla prima chiamata e allocare memoria per un buffer da passare alla seconda chiamata.
7.  Ottenere un puntatore [**all'interfaccia IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) per l'input nel writer chiamando [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
8.  Ottenere [**l'interfaccia IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) per l'oggetto proprietà del supporto di input chiamando **IWMInputMediaProps::QueryInterface**.
9.  Usare il [**metodo IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per impostare la \_ proprietà g wszOriginalWaveFormat. Usare la **struttura WAVEFORMATEX** ottenuta nel passaggio 6 come valore della proprietà .
10. Includere le modifiche apportate alle proprietà dei supporti di input chiamando [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passando un puntatore **all'interfaccia IWMInputMediaProps.**
11. Iniziare a leggere gli esempi dal file originale e passarli al writer con chiamate a [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).

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

 

 





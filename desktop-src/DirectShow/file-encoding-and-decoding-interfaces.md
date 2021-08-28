---
description: Interfacce di codifica e decodifica dei file
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfacce di codifica e decodifica dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6654497b0d2407666b286fb74f06a91e66834cfb963b62b7e22eb5755fa30b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639661"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Interfacce di codifica e decodifica dei file

Queste interfacce supportano la codifica e la decodifica dei file.



| Interfaccia                                                    | Descrizione                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Recuperare i metadati da un flusso, ad esempio l'autore e il titolo.                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Determinare lo stato di un'operazione di apertura file.                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Eseguire una query e impostare il tempo di analisi per la posizione corrente in un flusso MPEG.                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Controllare quali flussi logici vengono riprodotti e recuperare informazioni su di essi.                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Visualizzare le finestre di dialogo fornite dai codec VFW.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Impostare i parametri di compressione video.                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Controllare il modo in cui il filtro [WM ASF Writer](wm-asf-writer-filter.md) scrive file ASF (Advanced Systems Format). |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Controllare la modalità di scrittura dei file AVI da parte del filtro [Mux AVI.](avi-mux-filter.md)                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Configurare l'interfoliazione quando il filtro AVI Mux scrive file AVI.                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Impostare la risoluzione della codifica nel filtro [DV Video Encoder.](dv-video-encoder-filter.md)                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Downgrade della frequenza dei fotogrammi in un flusso video digitale (DV)                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Impostare la risoluzione di decodifica sul filtro [decodificatore video DV.](dv-video-decoder-filter.md)                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Impostare e recuperare blocchi INFO e DISP nei flussi AVI.                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce](interfaces.md)
</dt> </dl>

 

 




---
description: Interfacce di codifica e decodifica di file
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfacce di codifica e decodifica di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125595"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Interfacce di codifica e decodifica di file

Queste interfacce supportano la codifica e la decodifica dei file.



| Interfaccia                                                    | Descrizione                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Recuperare i metadati da un flusso, ad esempio l'autore e il titolo.                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Determinare lo stato di avanzamento di un'operazione di apertura file.                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Eseguire una query e impostare il tempo di analisi per la posizione corrente in un flusso MPEG.                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Controllare quali flussi logici vengono riprodotti e recuperare le relative informazioni.                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Visualizzare le finestre di dialogo fornite dai codec VFW.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Imposta i parametri di compressione video.                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Controllare il modo in cui il filtro del [writer WM ASF](wm-asf-writer-filter.md) scrive i file di formato Advanced Systems (ASF). |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Controllare il modo in cui il filtro [Mux AVI](avi-mux-filter.md) scrive i file AVI.                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Configurare l'interfoliazione quando il filtro Mux AVI scrive file AVI.                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Impostare la risoluzione della codifica sul filtro del [codificatore video DV](dv-video-encoder-filter.md) .                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Effettuare il downgrade della frequenza dei fotogrammi in un flusso video digitale (DV)                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Impostare la risoluzione della decodifica sul filtro del decodificatore [video DV](dv-video-decoder-filter.md) .                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Impostare e recuperare i blocchi INFO e DISP nei flussi AVI.                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce](interfaces.md)
</dt> </dl>

 

 




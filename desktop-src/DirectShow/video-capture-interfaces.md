---
description: Interfacce di acquisizione video
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfacce di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfee9807a94f381fef3a294dcd405de6fe8b67fafef3ace562309fe5e10d2ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633061"
---
# <a name="video-capture-interfaces"></a>Interfacce di acquisizione video

Queste interfacce supportano l'acquisizione video, usando dispositivi Microsoft® Windows® Driver Model (WDM) o dispositivi Microsoft® Video for Windows® (VFW) legacy.



| Interfaccia                                                        | Descrizione                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Controllare la digitalizzazione video in una scheda di acquisizione video WDM.                                                      |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Controllare la modalità di allocazione dei buffer da parte di un pin.                                                                         |
| [**IAMCopyCaptureFileProgress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Interfaccia di callback per ricevere lo stato di un'operazione di copia file.                                         |
| [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Creare una connessione hardware tra un'origine audio o video WDM e un dispositivo di acquisizione WDM.                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Eseguire una query su un filtro di acquisizione sulle prestazioni di acquisizione.                                                            |
| [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Controllare gli orari di inizio e arresto dei singoli flussi.                                                      |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Eseguire una query e impostare il formato di output del filtro di acquisizione.                                                            |
| [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Visualizzare le finestre di dialogo fornite dai driver di acquisizione VFW.                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Controllare l'immagine da un dispositivo di acquisizione.                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Regolare le qualità di un segnale video, ad esempio luminosità, contrasto, tonalità, saturazione, gamma e nitidezza. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Creare grafici di filtro per l'acquisizione di video.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Specificare il nome e gli attributi di un file di output.                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce di controllo dei dispositivi esterni](external-device-control-interfaces.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 




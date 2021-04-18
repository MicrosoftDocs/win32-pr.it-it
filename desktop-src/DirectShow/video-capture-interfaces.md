---
description: Interfacce di acquisizione video
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfacce di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308961"
---
# <a name="video-capture-interfaces"></a>Interfacce di acquisizione video

Queste interfacce supportano l'acquisizione video, usando i dispositivi Microsoft® Windows® Driver Model (WDM) o il video Microsoft® per i dispositivi Windows® (VFW).



| Interfaccia                                                        | Descrizione                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Controllare la digitalizzazione dei video in una scheda di acquisizione video WDM.                                                      |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Controllare il modo in cui un pin alloca i buffer.                                                                         |
| [**IAMCopyCaptureFileProgress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Interfaccia di callback per ricevere lo stato di avanzamento di un'operazione di copia file.                                         |
| [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Creare una connessione hardware tra un'origine audio o video WDM e un dispositivo di acquisizione WDM.                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Eseguire una query su un filtro di acquisizione sulle prestazioni di acquisizione.                                                            |
| [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Controllare l'ora di inizio e di fine dei singoli flussi.                                                      |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Eseguire una query e impostare il formato di output del filtro di acquisizione.                                                            |
| [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Consente di visualizzare le finestre di dialogo fornite dai driver di acquisizione di VFW.                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Controllare l'immagine da un dispositivo di acquisizione.                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Regolare le qualità di un segnale video, ad esempio luminosità, contrasto, tonalità, saturazione, gamma e nitidezza. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Grafici filtro compilazione per acquisizione video.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Specificare il nome e gli attributi di un file di output.                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce di controllo del dispositivo esterno](external-device-control-interfaces.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 




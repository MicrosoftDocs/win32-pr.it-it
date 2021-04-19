---
description: I seguenti identificatori univoci globali (GUID) definiscono i tipi di nodo per i filtri in modalità kernel. Per trovare il tipo di nodo, eseguire una query sul filtro per l'interfaccia IKsTopologyInfo.
ms.assetid: 0e133ce3-8815-47d1-a5c3-577a98963912
title: Tipi di nodo KS (Ksmedia. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSNODETYPE_DEV_SPECIFIC
- KSNODETYPE_VIDEO_CAMERA_TERMINAL
- KSNODETYPE_VIDEO_INPUT_MTT
- KSNODETYPE_VIDEO_INPUT_TERMINAL
- KSNODETYPE_VIDEO_OUTPUT_MTT
- KSNODETYPE_VIDEO_OUTPUT_TERMINAL
- KSNODETYPE_VIDEO_PROCESSING
- KSNODETYPE_VIDEO_SELECTOR
- KSNODETYPE_VIDEO_STREAMING
api_type:
- HeaderDef
api_location:
- Ksmedia.h
ms.openlocfilehash: eadae4fdd70fd80115ea4e8902ba1bb2aa7bf53b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326271"
---
# <a name="ks-node-types"></a>Tipi di nodo KS

I seguenti identificatori univoci globali (GUID) definiscono i tipi di nodo per i filtri in modalità kernel. Per trovare il tipo di nodo, eseguire una query sul filtro per l'interfaccia [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) .



| GUID                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KSNODETYPE_DEV_SPECIFIC"></span><span id="ksnodetype_dev_specific"></span><dl> <dt>**specifiche di KSNODETYPE \_ dev \_**</dt> </dl>                             | Rappresenta una o più funzioni di elaborazione specifiche del dispositivo. Il nodo ha una connessione di input e una connessione di output.<br/> Il nodo può esporre un'interfaccia COM personalizzata tramite un plug-in KsProxy, se fornito dal produttore del dispositivo.<br/>                                            |
| <span id="KSNODETYPE_VIDEO_CAMERA_TERMINAL"></span><span id="ksnodetype_video_camera_terminal"></span><dl> <dt>**\_ \_ terminale della fotocamera video KSNODETYPE \_**</dt> </dl> | Rappresenta i dati spostati nel dispositivo da un sensore della fotocamera, indipendentemente dal bus USB. Il nodo ha una connessione di output.<br/> Il nodo espone le interfacce [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) e [**ICameraControl**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) per il controllo della fotocamera.<br/> |
| <span id="KSNODETYPE_VIDEO_INPUT_MTT"></span><span id="ksnodetype_video_input_mtt"></span><dl> <dt>**\_MTT di \_ input \_ video KSNODETYPE**</dt> </dl>                   | Rappresenta i dati spostati nel dispositivo da un trasporto multimediale sequenziale, ad esempio un nastro VTR, indipendentemente dal bus USB. Il nodo ha una connessione di output.<br/> Il nodo espone l'interfaccia [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) per il controllo del meccanismo di trasporto.<br/>   |
| <span id="KSNODETYPE_VIDEO_INPUT_TERMINAL"></span><span id="ksnodetype_video_input_terminal"></span><dl> <dt>**\_terminale di \_ input \_ video KSNODETYPE**</dt> </dl>    | Rappresenta i dati spostati nel dispositivo, indipendentemente dal bus USB. Questo nodo, ad esempio, può rappresentare un jack audio analogico o un Jack S/PDIF. Il nodo ha una connessione di output.<br/>                                                                                                             |
| <span id="KSNODETYPE_VIDEO_OUTPUT_MTT"></span><span id="ksnodetype_video_output_mtt"></span><dl> <dt>**\_MTT di \_ output \_ video KSNODETYPE**</dt> </dl>                | Rappresenta i dati spostati dal dispositivo a un trasporto multimediale sequenziale, ad esempio un nastro VTR, indipendentemente dal bus USB. Il nodo ha una connessione di input.<br/> Il nodo espone l'interfaccia [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) per il controllo del meccanismo di trasporto.<br/>      |
| <span id="KSNODETYPE_VIDEO_OUTPUT_TERMINAL"></span><span id="ksnodetype_video_output_terminal"></span><dl> <dt>**\_terminale di \_ output \_ video KSNODETYPE**</dt> </dl> | Rappresenta i dati spostati dal dispositivo, indipendentemente dal bus USB. Questo nodo, ad esempio, può rappresentare un jack audio analogico o un Jack S/PDIF. Il nodo ha una connessione di input.<br/>                                                                                                              |
| <span id="KSNODETYPE_VIDEO_PROCESSING"></span><span id="ksnodetype_video_processing"></span><dl> <dt>**\_elaborazione video \_ KSNODETYPE**</dt> </dl>                 | Rappresenta una o più funzioni di elaborazione video. Il nodo ha una connessione di input e una connessione di output.<br/> Il nodo espone le interfacce [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) e [**IVideoProcAmp**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) per regolare le qualità del segnale video.<br/> |
| <span id="KSNODETYPE_VIDEO_SELECTOR"></span><span id="ksnodetype_video_selector"></span><dl> <dt>**\_selettore video KSNODETYPE \_**</dt> </dl>                       | Rappresenta un meccanismo per selezionare il percorso di input da due o più origini possibili. Il nodo dispone di due o più connessioni di input e una connessione di output.<br/> Il nodo espone l'interfaccia dell' [**eleggente**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) per la selezione tra input.<br/>                               |
| <span id="KSNODETYPE_VIDEO_STREAMING"></span><span id="ksnodetype_video_streaming"></span><dl> <dt>**\_streaming video \_ KSNODETYPE**</dt> </dl>                    | Rappresenta i dati spostati tra l'host e il dispositivo. Per i dispositivi UVC, questo nodo rappresenta un endpoint USB. Gli endpoint di input hanno una connessione di input. gli endpoint di output hanno una connessione di output.<br/>                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ksmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> </dl>

 

 





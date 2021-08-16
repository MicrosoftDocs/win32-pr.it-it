---
description: Specifica la velocità massima di elaborazione del macroblock per un flusso video H.264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: MF_MT_H264_MAX_MB_PER_SEC attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93bce2de0aa4f6c67cc7f6e61c09fde89923467a9211ba9e10642edf5a7f6416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104537"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a>Attributo MF \_ MT \_ H264 \_ MAX MB PER \_ \_ \_ SEC

Specifica la velocità massima di elaborazione del macroblock per un flusso video H.264.

## <a name="data-type"></a>Tipo di dati

**UINT32 \[ \]** archiviato come **UINT8 \[ \]**

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporti per i flussi H.264 trasmessi tramite USB. Il valore dell'attributo è una matrice di valori UINT32, che corrispondono ai campi seguenti nel descrittore del formato video UVC 1.5 H.264.

| Elemento Array | Campo descrittore                                           |
|---------------|------------------------------------------------------------|
| 0             | **dwMaxMBperSecOneResolutionNoScalability**                |
| 1             | **dwMaxMBperSecTwoResolutionsNoScalability**               |
| 2             | **dwMaxMBperSecThreeResolutionsNoScalability**             |
| 3             | **dwMaxMBperSecFourResolutionsNoScalability**              |
| 4             | **dwMaxMBperSecOneResolutionMaxralScalability**          |
| 5             | **dwMaxMBperSecTwoResolutionsRalScalablility**        |
| 6             | **dwMaxMBperSecThreeResolutionsCalcralScalability**       |
| 7             | **dwMaxMBperSecFourResolutionsRalScalability**        |
| 8             | **dwMaxMBperSecOneResolutionMaxralQualityScalability**   |
| 9             | **dwMaxMBperSecTwoResolutionsRalQualityScalability**  |
| 10            | **dwMaxMBperSecThreeResolutionsMaxralQualityScalablity** |
| 11            | **dwMaxMBperSecFourResolutionsRalQualityScalability** |
| 12            | **dwMaxMBperSecOneResolutionFullScalability**              |
| 13            | **dwMaxMBperSecTwoResolutionsFullScalability**             |
| 14            | **dwMaxMBperSecThreeResolutionsFullScalability**           |
| 15            | **dwMaxMBperSecFourResolutionsFullScalability**            |



 

Questo attributo viene usato anche con codificatori [di fotocamera H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 





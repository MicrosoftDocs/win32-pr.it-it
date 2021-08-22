---
description: Modifica la frequenza dei fotogrammi di un flusso video.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Frame Rate Converter DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca4a728f37caa43ee99a0d293d5113e9c26cfb1dcfe51f399482fb614283737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600491"
---
# <a name="frame-rate-converter-dsp"></a>Provider di servizi di conversione frequenza fotogrammi

Modifica la frequenza dei fotogrammi di un flusso video.

## <a name="clsid"></a>CLSID

CLSID \_ CFrameRateConvertDmo

## <a name="interfaces"></a>Interfacce

-   **IMediaObject**
-   **IMFTransform**
-   **Ipropertystore**

## <a name="formats"></a>Formati

-   ARGB 32
-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   IYUV
-   UYVY
-   Y211
-   Y411
-   Y41P
-   YUY2
-   YUYV
-   YV12
-   YVYU

## <a name="properties"></a>Proprietà

-   [MFPKEY \_ CONV \_ INPUTFRAMERATE](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ CONV \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Commenti

Questo DSP modifica la frequenza dei fotogrammi ripetendo o eliminando i fotogrammi.

Per impostazione predefinita, il provider di servizi multimediali ottiene le frequenze dei fotogrammi dai tipi di supporti. Facoltativamente, è possibile specificare le frequenze dei fotogrammi impostando le proprietà MFPKEY \_ CONV \_ INPUTFRAMERATE e MFPKEY \_ CONV \_ OUTPUTFRAMERATE. Questi valori eseguono l'override della frequenza dei fotogrammi specificata nel tipo di supporto. Tuttavia, se si usa questo provider di servizi di distribuzione all'interno Media Foundation pipeline, non è consigliabile impostare queste proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnali digitali](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 





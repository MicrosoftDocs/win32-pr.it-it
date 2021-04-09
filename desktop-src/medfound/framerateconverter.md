---
description: Modifica la frequenza dei fotogrammi di un flusso video.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Convertitore frequenza frame DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749231"
---
# <a name="frame-rate-converter-dsp"></a>Convertitore frequenza frame DSP

Modifica la frequenza dei fotogrammi di un flusso video.

## <a name="clsid"></a>CLSID

\_CFRAMERATECONVERTDMO CLSID

## <a name="interfaces"></a>Interfacce

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

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

-   [MFPKEY \_ conv \_ INPUTFRAMERATE](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ conv \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Commenti

Questo DSP modifica la frequenza dei fotogrammi ripetendo o eliminando i frame.

Per impostazione predefinita, il DSP ottiene le frequenze dei fotogrammi dai tipi di supporto. Facoltativamente, è possibile specificare le frequenze dei fotogrammi impostando \_ le \_ Proprietà MFPKEY CONV INPUTFRAMERATE e MFPKEY \_ conv \_ OUTPUTFRAMERATE. Questi valori eseguono l'override della frequenza dei fotogrammi specificata nel tipo di supporto. Tuttavia, se si usa questo DSP all'interno della pipeline di Media Foundation, è consigliabile non impostare queste proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 





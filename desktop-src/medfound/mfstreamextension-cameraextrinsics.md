---
description: Contiene le estrise della fotocamera per il flusso.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: MFStreamExtension_CameraExtrinsics attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acf76c829383d229df8039bfff5d75234d31e2625f758d1bca254217b6e138c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713541"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a>Attributo MFStreamExtension \_ CameraExtrinsics

Contiene le estrise della fotocamera per il flusso.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).

## <a name="remarks"></a>Commenti

Il valore dell'attributo è [**un oggetto MFCameraExtrinsics.**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                        |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 





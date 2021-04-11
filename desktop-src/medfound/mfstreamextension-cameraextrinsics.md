---
description: Contiene la fotocamera estrinseca per il flusso.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: Attributo MFStreamExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130518"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a>\_Attributo CameraExtrinsics di MFStreamExtension

Contiene la fotocamera estrinseca per il flusso.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).

## <a name="remarks"></a>Commenti

Il valore dell'attributo è un [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 





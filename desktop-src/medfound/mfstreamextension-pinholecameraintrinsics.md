---
description: Contiene gli intrinseci della fotocamera pin tunnel per il flusso.
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: MFStreamExtension_PinholeCameraIntrinsics attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0a77f7d49770e084dfe258169863a713311be02f1711c6f637c7bfc16b4e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973180"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a>Attributo MFStreamExtension \_ PinholeCameraIntrinsics

Contiene gli intrinseci della fotocamera pin tunnel per il flusso.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).

## <a name="remarks"></a>Commenti

Il valore dell'attributo è [**un oggetto MFPinholeCameraIntrinsics.**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                        |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 





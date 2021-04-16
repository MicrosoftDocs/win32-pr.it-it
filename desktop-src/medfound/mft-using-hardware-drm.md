---
description: Specifica se IMFTransform utilizza DRM hardware.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485348"
---
# <a name="mft_using_hardware_drm-attribute"></a>MFT \_ con \_ \_ attributo DRM hardware

Specifica se IMFTransform utilizza DRM hardware.

## <a name="data-type"></a>Tipo di dati

**UInt32** (considerato **bool**)

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Commenti

Se un MFT Decrypter specifica che questo attributo è impostato su 1, utilizza DRM hardware. Se un MFT Decrypter specifica che questo attributo è impostato su 0, non sta utilizzando DRM hardware. Se un MFT Decrypter non specifica questo attributo o lo specifica con un valore diverso, non lo è o non è in grado di indicare se sta utilizzando DRM hardware.


La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Aggiornamento di Windows 10 aprile 2020   <br/>                                       |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 





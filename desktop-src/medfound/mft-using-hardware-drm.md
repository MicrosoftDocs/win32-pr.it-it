---
description: Specifica se IMFTransform usa DRM hardware.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b46760fd5759abdd601269f5905f0649145649713839de5fe6424bc36219c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473551"
---
# <a name="mft_using_hardware_drm-attribute"></a>Attributo \_ \_ DRM MFT USING \_ HARDWARE

Specifica se IMFTransform usa DRM hardware.

## <a name="data-type"></a>Tipo di dati

**UINT32** (trattato come **BOOL**)

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Commenti

Se un decrypter MFT specifica questo attributo impostato su 1, usa DRM hardware. Se un decrypter MFT specifica questo attributo impostato su 0, non usa DRM hardware. Se un decrypter MFT non specifica questo attributo o lo specifica con un valore diverso, non indica (o non è in grado di) indicare se usa DRM hardware.


La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10 Aggiornamento di aprile 2020   <br/>                                       |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 





---
description: Consente al renderer video avanzato (EVR) di migliorare le prestazioni ignorando il secondo campo di ogni fotogramma interlacciato.
ms.assetid: de7efc6a-19ae-4f3a-8675-38fda3c979e2
title: EVRConfig_AllowDropToHalfInterlace attributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfae2bf47e71d1c6cb7dbed60069a79f56cee3249c362acf6c0efc99dc06f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828151"
---
# <a name="evrconfig_allowdroptohalfinterlace-attribute"></a>Attributo \_ AllowDropToHalfInterlace EVRConfig

Consente al renderer video avanzato (EVR) di migliorare le prestazioni ignorando il secondo campo di ogni fotogramma interlacciato.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato nel sink del supporto EVR. Per impostare l'attributo, usare **QueryInterface** per eseguire una query sul sink multimediale EVR per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoMixPrefs \_ AllowDropToHalfInterlace** su EVR. Per una descrizione di questo flag, vedere [**MFVideoMixPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs)

La costante GUID per questo attributo viene esportata da strmiids.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gestione della qualità dei video](video-quality-management.md)
</dt> </dl>

 

 





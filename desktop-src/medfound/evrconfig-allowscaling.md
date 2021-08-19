---
description: Alllows the Enhanced Video Renderer (EVR) to mix the video within a rectangle that is smaller than the output rectangle ,and then scale the result.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: EVRConfig_AllowScaling attributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83323c42ac81d4cce0bb42733bd4246959cf0fc9a58b5705579a86aee9b2bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879425"
---
# <a name="evrconfig_allowscaling-attribute"></a>Attributo AllowScaling di EVRConfig \_

Alllows the Enhanced Video Renderer (EVR) to mix the video within a rectangle that is smaller than the output rectangle ,and then scale the result.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato nel sink del supporto EVR. Per impostare l'attributo, usare **QueryInterface** per eseguire una query sul sink multimediale EVR per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **\_ AllowScaling MFVideoRenderPrefs** nell'EVR. Per [**una descrizione di questo flag, vedere MFVideoRenderPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs)

La costante GUID per questo attributo viene esportata da strmiids.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gestione della qualità video](video-quality-management.md)
</dt> </dl>

 

 





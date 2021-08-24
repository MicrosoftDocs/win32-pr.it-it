---
description: Forza il renderer video avanzato (EVR) a limitare l'output in modo che corrisponda alla larghezza di banda della GPU.
ms.assetid: e81e67d6-aa72-44c1-90e9-72ab18bca1c9
title: EVRConfig_ForceThrottle attributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad09d0c3133039975a04a026ec84233987dfd4033b120a4b8fc6272e2fd72b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346141"
---
# <a name="evrconfig_forcethrottle-attribute"></a>Attributo ForceThrottle di EVRConfig \_

Forza il renderer video avanzato (EVR) a limitare l'output in modo che corrisponda alla larghezza di banda della GPU.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato nel sink del supporto EVR. Per impostare l'attributo, usare **IUnknown::QueryInterface** per eseguire una query sul sink multimediale EVR per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **MFVideoRenderPrefs \_ ForceOutputThrottling** su EVR. Per una descrizione di questo flag, vedere [**MFVideoRenderPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs)

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

 

 





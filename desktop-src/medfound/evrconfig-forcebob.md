---
description: Forza l'uso del renderer video avanzato (EVR) per l'uso della deinterlacing bob.
ms.assetid: 56f808b3-c2eb-46e4-84a1-c478a5db78e7
title: EVRConfig_ForceBob attributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41248eb48f089cf88ecd66dcf823cc83c243b3a2f637aef7633d13ac755c9584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958350"
---
# <a name="evrconfig_forcebob-attribute"></a>Attributo ForceBob EVRConfig \_

Forza l'uso del renderer video avanzato (EVR) per l'uso della deinterlacing bob.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato nel sink del supporto EVR. Per impostare l'attributo, usare **QueryInterface** per eseguire una query sul sink multimediale EVR per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

L'impostazione di questo attributo ha lo stesso effetto dell'impostazione del flag **\_ ForceBob MFVideoMixPrefs** nell'EVR. Per [**una descrizione di questo flag, vedere MFVideoMixPrefs.**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs)

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

 

 





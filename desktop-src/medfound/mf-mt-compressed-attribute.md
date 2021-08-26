---
description: Specifica per un tipo di supporto se i dati multimediali sono compressi.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: MF_MT_COMPRESSED attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afea99ffb0c9f7f9f53fb6edd0b4b87b2ecd4ff4f451e5fd0e56d47a70aee994
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060691"
---
# <a name="mf_mt_compressed-attribute"></a>Attributo \_ MT COMPRESSED di MF \_

Specifica per un tipo di supporto se i dati multimediali sono compressi.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se questo attributo è **TRUE,** il tipo di supporto è un formato compresso. In caso contrario, il tipo di supporto non è compresso o il tipo di compressione non è noto.

Non è garantito che questo attributo sia impostato su **TRUE** per tutti i formati compressi, pertanto le applicazioni in genere non devono basarsi su questo attributo. Il modo più affidabile per determinare se un formato è compresso è mantenere un elenco di formati noti. Se un'applicazione non riconosce un formato, come specificato nell'attributo [**\_ MF MT \_ SUBTYPE,**](mf-mt-subtype-attribute.md) non deve presupporre nulla sulla compressione del formato.

Per determinare se un formato usa la compressione temporale (ovvero alcuni campioni vengono calcolati come delta da esempi precedenti), controllare l'attributo [**\_ MF MT \_ ALL SAMPLES \_ \_ INDEPENDENT.**](mf-mt-all-samples-independent-attribute.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 





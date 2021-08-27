---
description: Specifica le dimensioni, in byte, della sezione di dati di un file ASF (Advanced Systems Format).
ms.assetid: 93a0bf27-23db-4e8a-b471-a42122e8f9aa
title: MF_PD_ASF_DATA_LENGTH attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e0af92a5cbc5647750f65005a195b7beefbc955e8906d8e8ca976783572d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060451"
---
# <a name="mf_pd_asf_data_length-attribute"></a>Attributo MF \_ PD \_ ASF \_ DATA \_ LENGTH

Specifica le dimensioni, in byte, della sezione di dati di un file ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto di ASF.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati asf.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto Intestazione ASF](asf-file-structure.md)
</dt> </dl>

 

 





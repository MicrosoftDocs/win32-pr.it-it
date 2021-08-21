---
description: Specifica il tipo MIME del contenuto.
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: MF_PD_MIME_TYPE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb68e9b45d51b9fe4732957ef60a4496ca57df5be0185f46a7e28204217b4ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059641"
---
# <a name="mf_pd_mime_type-attribute"></a>Attributo MF \_ PD \_ MIME \_ TYPE

Specifica il tipo MIME del contenuto.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione.

Il tipo MIME esposto tramite [System.MIMEType](../properties/props-system-mimetype.md) per i file multimediali può avere una distorsione nella scelta dei tipi MIME adatti per Digital Living Network Alliance (DLNA).

MF \_ PD \_ MIME TYPE e \_ [System.MIMEType](../properties/props-system-mimetype.md) potrebbero non corrispondere sempre.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 

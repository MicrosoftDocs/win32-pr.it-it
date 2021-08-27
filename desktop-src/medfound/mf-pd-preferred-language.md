---
description: Contiene la lingua RFC 1766 preferita dell'origine multimediale.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: MF_PD_PREFERRED_LANGUAGE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cd01a47002bf3cd9419579786ff37df1fc03af940f54b2d2a2bb859d5b97007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740712"
---
# <a name="mf_pd_preferred_language-attribute"></a>Attributo MF \_ PD \_ PREFERRED \_ LANGUAGE

Contiene la lingua RFC 1766 preferita dell'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**Wchar**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes::Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Si applica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Commenti

L'attributo MF \_ PD \_ PREFERRED LANGUAGE è \_ facoltativo. Un'applicazione può impostare questo attributo in un'origine multimediale, ad esempio un'origine di rete, per specificare la lingua preferita.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





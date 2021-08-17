---
description: Contiene un valore definito dal chiamante per un evento METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: MF_EVENT_MFT_CONTEXT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9518853030ec52a687f02ac0288c3fd3ffcf55b676be56c7036b349e1dec9aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104847"
---
# <a name="mf_event_mft_context-attribute"></a>Attributo MF \_ EVENT \_ MFT \_ CONTEXT

Contiene un valore definito dal chiamante per un [evento METransformMarker.](metransformmarker.md)

## <a name="data-type"></a>Tipo di dati

**ULONG \_ PTR** archiviato come **UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Si applica a

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Commenti

Questo attributo viene usato con [l'evento METransformMarker.](metransformmarker.md) Il valore dell'attributo deriva dal *parametro ulParam* del metodo [**IMFTransform::P rocessMessage.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincroni](asynchronous-mfts.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> </dl>

 

 





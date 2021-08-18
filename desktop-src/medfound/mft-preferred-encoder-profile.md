---
description: Contiene le proprietà di configurazione per un codificatore.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: MFT_PREFERRED_ENCODER_PROFILE attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85acf742e518d91c6512b2b887cca910c3b19d21180500bd1180e6972255e54f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722506"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>Attributo MFT \_ PREFERRED \_ ENCODER \_ PROFILE

Contiene le proprietà di configurazione per un codificatore.

## <a name="data-type"></a>Tipo di dati

**[**Attributi IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \* *_ archiviato come _* Iunknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Si applica a

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato sull'oggetto attivazione restituito dalla [**funzione MFCreateTransformActivate.**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) L'attributo si applica solo quando l'oggetto attivazione è configurato per creare un codificatore. Il valore dell'attributo è un puntatore a un archivio di attributi, che contiene le proprietà da impostare nel codificatore.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 





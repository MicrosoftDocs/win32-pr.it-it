---
description: Specifica per un tipo di supporto se ogni campione è indipendente dagli altri campioni nel flusso.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: MF_MT_ALL_SAMPLES_INDEPENDENT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ada34232ccbc7eb30fc9a5bcb64e96542b0375140de426fae951f5e0317c9e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060751"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>Attributo MF \_ MT \_ ALL SAMPLES \_ \_ INDEPENDENT

Specifica per un tipo di supporto se ogni campione è indipendente dagli altri campioni nel flusso.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se questo attributo è **FALSE,** alcuni esempi non possono essere usati senza fare riferimento ad altri esempi nel flusso. Ad esempio, se un formato video contiene fotogrammi differenziali, questo attributo deve essere **FALSE.**

Questo attributo corrisponde al **campo bTemporalCompression** nella DirectShow [**AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

Impostare questo attributo su **TRUE per tutti** i tipi di supporti non compressi.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 

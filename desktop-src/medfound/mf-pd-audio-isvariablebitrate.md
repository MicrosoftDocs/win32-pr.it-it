---
description: Specifica se i flussi audio in una presentazione hanno una velocità in bit variabile.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: MF_PD_AUDIO_ISVARIABLEBITRATE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5c8c15c12bcd867342fb11f5e753c196f9954aea0393b2a461e1804f411339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664191"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a>Attributo MF \_ PD \_ AUDIO \_ ISVARIABLEBITRATE

Specifica se i flussi audio in una presentazione hanno una velocità in bit variabile.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Commenti

Si tratta di un attributo facoltativo per i descrittori di presentazione. Se l'attributo **è TRUE** (diverso da zero), la presentazione contiene almeno un flusso audio VBR (Variable-Bit-Rate). Se l'attributo è **FALSE,** tutti i flussi audio hanno una velocità in bit costante.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





---
description: Specifica se un esempio video contiene un singolo campo o due campi interleaved. Questo attributo si applica agli esempi di supporti.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: MFSampleExtension_SingleField attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747dbeebb9bcc8e773b59467f460b12645ed50ebfbddf5bbf6845119c2bba81d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462901"
---
# <a name="mfsampleextension_singlefield-attribute"></a>Attributo SingleField MFSampleExtension \_

Specifica se un esempio video contiene un singolo campo o due campi interleaved. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Esempio IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Se il valore è **TRUE,** l'esempio contiene un campo. Se il valore è **FALSE** o l'attributo non è impostato, l'esempio contiene un frame completo. Due campi, se interlacciati, o un frame progressivo.

Se il tipo di supporto è fotogrammi progressivi o campi interleaved, questo attributo deve essere **FALSE** o non impostato.

Se il tipo di supporto è un singolo campo, questo attributo deve essere **TRUE.** Impostare [**l'attributo \_ BottomFieldFirst di MFSampleExtension**](mfsampleextension-bottomfieldfirst-attribute.md) nell'esempio per indicare se si tratta del campo superiore o inferiore.

Attualmente il renderer video avanzato (EVR) non supporta il contenuto che passa tra fotogrammi interlacciati e singoli campi.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Interlacciamento video](video-interlacing.md)
</dt> </dl>

 

 





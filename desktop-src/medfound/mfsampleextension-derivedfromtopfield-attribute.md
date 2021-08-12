---
description: Specifica se un fotogramma video deinterlaced è stato derivato dal campo superiore o dal campo inferiore.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: MFSampleExtension_DerivedFromTopField attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 376cc499dd76702abb4c7054014a7c720118f33a732856202c4e654992c30985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241191"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>Attributo DerivedFromTopField di MFSampleExtension \_

Specifica se un fotogramma video deinterlaced è stato derivato dal campo superiore o dal campo inferiore. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Esempio IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Questo attributo è valido solo per gli esempi deinterlaced. Impostare questo attributo se il frame è stato deinterlaced interpolando uno dei campi.

Se il valore è **TRUE,** il campo inferiore è stato interpolato dal campo superiore. Se il valore è **FALSE,** il campo superiore è stato interpolato dal campo inferiore.

Se l'attributo non è impostato, il frame non è stato deinterlaced. Il frame è un frame progressivo vero o è un frame interlacciato.

Questo attributo è informativo. Un deinterlacer software può impostare questo attributo. Se questo attributo è impostato, fornisce un suggerimento per recuperare il campo originale eliminando le righe di analisi interpolate. Ad esempio, se l'attributo è **TRUE,** è possibile recuperare il campo superiore originale eliminando il campo inferiore interpolato.

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

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Interlacciamento video](video-interlacing.md)
</dt> </dl>

 

 





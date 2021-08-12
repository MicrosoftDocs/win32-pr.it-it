---
description: Indica se un fotogramma video è interlacciato o progressivo.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: MFSampleExtension_Interlaced attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d928d42fc2399536d5beee4f4af87cbacaa82171048ad191a4e9fc7ef3e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240648"
---
# <a name="mfsampleextension_interlaced-attribute"></a>Attributo interlacciato MFSampleExtension \_

Indica se un fotogramma video è interlacciato o progressivo. Se **TRUE,** il frame è interlacciato. Se **FALSE,** il frame è progressivo. Se non è impostato, il tipo di supporto descrive l'interlacciamento. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Esempio IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Per il contenuto video che contiene fotogrammi progressivi e interlacciati misti, impostare il tipo di supporto su interlacciato e usare questo attributo in ogni fotogramma per indicare se il fotogramma è progressivo o interlacciato.

Per il contenuto video interamente interlacciato, impostare il tipo di supporto su interlacciato e omettere questo attributo oppure impostarlo su **TRUE** in ogni esempio.

Per il contenuto video completamente progressivo, impostare il tipo di supporto su progressivo e omettere questo attributo oppure impostarlo su **FALSE** in ogni esempio.

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

[**Esempio IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Interlacciamento video](video-interlacing.md)
</dt> </dl>

 

 





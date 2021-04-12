---
description: Stride della superficie predefinita, per un tipo di supporto video non compresso. Stride indica il numero di byte necessari per passare da una riga di pixel a quella successiva.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Attributo MF_MT_DEFAULT_STRIDE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226636"
---
# <a name="mf_mt_default_stride-attribute"></a>\_ \_ Attributo stride predefinito MF mt \_

Stride della superficie predefinita, per un tipo di supporto video non compresso. Stride indica il numero di byte necessari per passare da una riga di pixel a quella successiva.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come un valore **Int32** .

## <a name="remarks"></a>Commenti

Il valore dell'attributo viene archiviato come **UInt32**, ma deve essere eseguito il cast a un valore intero con segno a 32 bit. Stride può essere negativo.

Stride è un valore positivo per le immagini dall'alto verso il basso e negativo per le immagini dal basso verso l'alto.

Questo attributo fornisce lo stride per una rappresentazione *contigua* dell'immagine in memoria; ovvero una rappresentazione senza ulteriori byte di riempimento dopo ogni riga. Se un buffer multimediale supporta l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , usare il metodo [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) per ottenere lo stride effettivo della superficie, che può includere byte di riempimento aggiuntivi.

Per altre informazioni sullo stride della superficie, vedere [immagine stride](image-stride.md).

Per un esempio di come calcolare lo stride predefinito, vedere [buffer video non compressi](uncompressed-video-buffers.md).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Stride immagine](image-stride.md)
</dt> </dl>

 

 





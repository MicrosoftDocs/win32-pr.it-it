---
description: Stride della superficie predefinito per un tipo di supporto video non compresso. Stride è il numero di byte necessari per passare da una riga di pixel a quella successiva.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e130918f62d6ff986ced7dd6449dcc2d381a00fc0d7c0342eeb4afcc03833bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035239"
---
# <a name="mf_mt_default_stride-attribute"></a>Attributo MF \_ MT \_ DEFAULT \_ STRIDE

Stride della superficie predefinito per un tipo di supporto video non compresso. Stride è il numero di byte necessari per passare da una riga di pixel a quella successiva.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considerare come **valore INT32.**

## <a name="remarks"></a>Commenti

Il valore dell'attributo viene archiviato come **UINT32,** ma è necessario eseguire il cast a un valore intero con segno a 32 bit. Stride può essere negativo.

Stride è positivo per le immagini dall'alto verso il basso e negativo per le immagini dal basso verso l'alto.

Questo attributo fornisce lo stride per una *rappresentazione contigua* dell'immagine in memoria. una rappresentazione senza byte di riempimento aggiuntivi dopo ogni riga. Se un buffer multimediale supporta [**l'interfaccia IMF2DBuffer,**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) usare il metodo [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) per ottenere lo stride effettivo della superficie, che potrebbe includere byte di riempimento aggiuntivi.

Per altre informazioni sullo stride della superficie, vedere [Stride dell'immagine.](image-stride.md)

Per un esempio di come calcolare lo stride predefinito, vedere [Buffer video non compressi.](uncompressed-video-buffers.md)

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
</dt> <dt>

[Stride dell'immagine](image-stride.md)
</dt> </dl>

 

 





---
description: Contiene l'anteprima della foto di un IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Attributo MFSampleExtension_PhotoThumbnail (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131115"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>\_Attributo di anteprima MFSampleExtension

Contiene l'anteprima della foto di un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).

## <a name="data-type"></a>Tipo di dati

**IUnknown** archiviato come **IMFMediaBuffer**

L'anteprima viene configurata con **KSPROPERTYSETID \_ ExtendedCameraControl**.

## <a name="remarks"></a>Commenti

Questo attributo è impostato su [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) fornito da MFT0 ed è l'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associato all'anteprima foto.

Il formato dell'anteprima foto può essere JPEG (immagine del tipo principale), NV12 o ARGB32.

Il [ \_ PhotoThumbnailMediaType MFSampleExtension](mfsampleextension-photothumbnailmediatype.md) è necessario per le anteprime per descrivere il tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 

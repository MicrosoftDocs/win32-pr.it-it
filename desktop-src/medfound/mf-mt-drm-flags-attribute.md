---
description: Specifica se un tipo di supporto video richiede l'applicazione della protezione della copia.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: Attributo MF_MT_DRM_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315034"
---
# <a name="mf_mt_drm_flags-attribute"></a>\_ \_ Attributo flag DRM MF mt \_

Specifica se un tipo di supporto video richiede l'applicazione della protezione della copia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro dell'enumerazione [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) .

Questo attributo fornisce un suggerimento per l'applicazione. Non viene utilizzato per applicare la protezione della copia o per specificare il meccanismo di protezione della copia.

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

[MF \_ SD \_ protetto](mf-sd-protected-attribute.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 





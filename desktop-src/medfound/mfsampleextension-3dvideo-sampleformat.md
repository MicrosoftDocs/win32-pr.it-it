---
description: Specifica la modalità di archiviazione di un fotogramma video 3D in un campione multimediale.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: MFSampleExtension_3DVideo_SampleFormat attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6529a08c14846fb1d06cd9b3ed0827a43d1b1ba75310c0379efddadebecdaeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722871"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>Attributo SampleFormat MFSampleExtension \_ 3DVideo \_

Specifica la modalità di archiviazione di un fotogramma video 3D in un campione multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro [**dell'enumerazione MFVideo3DSampleFormat.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat)

Un componente che genera fotogrammi video 3D deve impostare questo attributo su **TRUE** in ogni campione multimediale che contiene un fotogramma 3D. L'attributo viene ignorato [se l'attributo MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) è **FALSE** o non è impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 





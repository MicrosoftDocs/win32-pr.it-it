---
description: Specifica il modo in cui un frame video 3D viene archiviato in un esempio di supporto.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Attributo MFSampleExtension_3DVideo_SampleFormat (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131127"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>MFSampleExtension \_ 3DVideo- \_ attributo SampleFormat

Specifica il modo in cui un frame video 3D viene archiviato in un esempio di supporto.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro dell'enumerazione [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .

Un componente che genera fotogrammi video 3D deve impostare questo attributo su **true** in ogni esempio multimediale che contiene un frame 3D. L'attributo viene ignorato se l'attributo [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) è **false** o non impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[\_3DVideo MFSampleExtension](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 





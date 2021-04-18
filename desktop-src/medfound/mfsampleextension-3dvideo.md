---
description: Specifica se un esempio multimediale contiene un frame video 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Attributo MFSampleExtension_3DVideo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309100"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>\_Attributo 3DVideo di MFSampleExtension

Specifica se un esempio multimediale contiene un frame video 3D.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Se questo attributo è **true**, l'esempio multimediale contiene un frame video con due o più visualizzazioni stereoscopiche. Il valore predefinito è **false**.

Un componente che genera fotogrammi video 3D deve impostare questo attributo su **true** in ogni esempio multimediale che contiene un frame 3D.

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

[MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 





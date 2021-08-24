---
description: Specifica se un campione multimediale contiene un fotogramma video 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: MFSampleExtension_3DVideo attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb959accfb3326e90068a26247eeab25e9aeaddacb720a0dfd64aa6e5b237a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722801"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>Attributo MFSampleExtension \_ 3DVideo

Specifica se un campione multimediale contiene un fotogramma video 3D.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Se questo attributo è **TRUE,** l'esempio multimediale contiene un fotogramma video con due o più visualizzazioni stereoscopiche. Il valore predefinito è **FALSE.**

Un componente che genera fotogrammi video 3D deve impostare questo attributo su **TRUE** in ogni campione multimediale che contiene un fotogramma 3D.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 





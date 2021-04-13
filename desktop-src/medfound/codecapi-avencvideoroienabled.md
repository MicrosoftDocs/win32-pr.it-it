---
description: Indica se \_ l'attributo MFSampleExtension ROIRectangle impostato sull'esempio di input verrà rispettato o meno.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: Proprietà CODECAPI_AVEncVideoROIEnabled (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345e6ba27a983be910f0dc0ea5d3db34191bdcb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342556"
---
# <a name="codecapi_avencvideoroienabled-property"></a>Proprietà AVEncVideoROIEnabled di codecapi \_

Indica se l'attributo [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) impostato sull'esempio di input verrà rispettato o meno.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>Commenti

Il valore predefinito è 0.

Se un codificatore MFT accetta un valore diverso da zero, si prevede che il codificatore rispetterà l'attributo [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) impostato nell'esempio di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                   |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 





---
description: Regola la luminosità.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: MFPKEY_COLOR_BRIGHTNESS proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a43969dff8d743e493916303c31e3d57760a2b025bfadaeaf8cc03e7e25430d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954651"
---
# <a name="mfpkey_color_brightness-property"></a>Proprietà MFPKEY \_ COLOR \_ BRIGHTNESS

Regola la luminosità.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [DSP trasformazione controllo colore](colorcontroltransform.md)

## <a name="remarks"></a>Commenti

La regolazione della luminosità viene eseguita aggiungendo un valore al canale luma.

Questa proprietà ha un intervallo compreso tra -127 e 127. Zero indica che non è stata apportata alcuna modifica alla luminosità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 

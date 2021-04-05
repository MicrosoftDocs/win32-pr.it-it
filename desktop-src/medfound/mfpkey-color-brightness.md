---
description: Regola la luminosità.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: Proprietà MFPKEY_COLOR_BRIGHTNESS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881418"
---
# <a name="mfpkey_color_brightness-property"></a>\_ \_ Proprietà luminosità colore MFPKEY

Regola la luminosità.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [Trasformazione controllo colori DSP](colorcontroltransform.md)

## <a name="remarks"></a>Commenti

La regolazione della luminosità viene eseguita aggiungendo un valore al canale luma.

Questa proprietà ha un intervallo compreso tra-127 e 127. Zero indica che non è presente alcuna modifica alla luminosità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 

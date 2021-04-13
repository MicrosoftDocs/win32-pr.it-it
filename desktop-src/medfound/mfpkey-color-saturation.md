---
description: Regola la saturazione.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: Proprietà MFPKEY_COLOR_SATURATION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528686"
---
# <a name="mfpkey_color_saturation-property"></a>\_ \_ Proprietà saturazione colore MFPKEY

Regola la saturazione.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [Trasformazione controllo colori DSP](colorcontroltransform.md)

## <a name="remarks"></a>Commenti

La regolazione della saturazione viene eseguita moltiplicando i valori CB e CR per una costante.

Questa proprietà ha un intervallo compreso tra-127 e 127. Zero indica che non sono state apportate modifiche alla saturazione.

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

 

 

---
description: Regola il contrasto.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: MFPKEY_COLOR_CONTRAST proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c1c794b10580cbb323d19f52eed7d3bfb5fc6cf96e316d708491025776cfff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954471"
---
# <a name="mfpkey_color_contrast-property"></a>Proprietà MFPKEY \_ COLOR \_ CONTRAST

Regola il contrasto.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [DSP trasformazione controllo colore](colorcontroltransform.md)

## <a name="remarks"></a>Commenti

La regolazione del contrasto viene eseguita moltiplicando i valori YCbCr per un fattore di scala.

Questa proprietà ha un intervallo compreso tra -127 e 127. Zero indica nessuna modifica al contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 

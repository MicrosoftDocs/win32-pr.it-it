---
description: Regola la tonalità.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: MFPKEY_COLOR_HUE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646d9e3ae0e72e11ae8952d28df9e4e3afc4147eaa7983bd1f0e9c82266ca5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954441"
---
# <a name="mfpkey_color_hue-property"></a>Proprietà MFPKEY \_ COLOR \_ HUE

Regola la tonalità.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [DSP trasformazione controllo colore](colorcontroltransform.md)

## <a name="remarks"></a>Commenti

La regolazione della tonalità viene eseguita combinando i valori Cb e Cr. Se Cb e Cr vengono tracciati in uno spazio bidimensionale, la regolazione della tonalità viene eseguita ruotando intorno all'origine.

Questa proprietà ha un intervallo compreso tra -127 e 127. Zero indica che non è stata apportata alcuna modifica alla tonalità.

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

 

 

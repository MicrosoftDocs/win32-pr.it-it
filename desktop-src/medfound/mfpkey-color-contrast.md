---
description: Regola il contrasto.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: Proprietà MFPKEY_COLOR_CONTRAST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310658"
---
# <a name="mfpkey_color_contrast-property"></a>\_ \_ Proprietà contrasto colori MFPKEY

Regola il contrasto.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [Trasformazione controllo colori DSP](colorcontroltransform.md)

## <a name="remarks"></a>Commenti

La regolazione del contrasto viene eseguita moltiplicando i valori YCbCr per un fattore di scala.

Questa proprietà ha un intervallo compreso tra-127 e 127. Zero indica che non vi sono modifiche al contrasto.

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

 

 

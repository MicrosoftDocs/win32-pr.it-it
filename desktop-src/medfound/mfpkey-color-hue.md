---
description: Regola la tonalità.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: Proprietà MFPKEY_COLOR_HUE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131251"
---
# <a name="mfpkey_color_hue-property"></a>\_ \_ Proprietà tonalità colore MFPKEY

Regola la tonalità.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [Trasformazione controllo colori DSP](colorcontroltransform.md)

## <a name="remarks"></a>Commenti

La regolazione Hue viene eseguita combinando i valori CB e CR. Se CB e CR sono tracciati in uno spazio bidimensionale, la regolazione della tonalità viene eseguita ruotando intorno all'origine.

Questa proprietà ha un intervallo compreso tra-127 e 127. Zero indica che la tonalità non è stata modificata.

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

 

 

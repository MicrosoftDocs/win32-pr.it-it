---
description: Struttura che descrive un singolo valore di colore.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317272"
---
# <a name="xps_color"></a>\_colore XPS

Struttura che descrive un singolo valore di colore.

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a>Commenti

Il formato della struttura dipende dal valore di *ColorType*.

<dl>

[**\_tipo di colore XPS \_ \_ sRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))  
[**\_tipo di colore XPS \_ \_**](/previous-versions/windows/desktop/dd372943(v=vs.85))  
[**\_contesto del \_ tipo di colore XPS \_**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]<br/> |
| Intestazione<br/>                   | <dl> <dt>Xpsobjectmodel. h</dt> </dl>                                              |
| IDL<br/>                      | <dl> <dt>XpsObjectModel. idl</dt> </dl>                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 


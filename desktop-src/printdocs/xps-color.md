---
description: Struttura che descrive un singolo valore di colore.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f771bcbb516352b2ef689060c11003808d434be8059d16af78fe8db646c97000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971150"
---
# <a name="xps_color"></a>COLORE \_ XPS

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

Il formato della struttura dipende dal valore di *colorType*.

<dl>

[**TIPO DI COLORE XPS \_ \_ \_ SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))  
[**TIPO DI COLORE XPS \_ \_ \_ SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))  
[**CONTESTO DEL TIPO DI COLORE XPS \_ \_ \_**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e Aggiornamento piattaforma per app desktop Windows Vista \[ \| app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop Windows Server 2008 \[ \| UWP\]<br/> |
| Intestazione<br/>                   | <dl> <dt>Xpsobjectmodel.h</dt> </dl>                                              |
| Idl<br/>                      | <dl> <dt>XpsObjectModel.idl</dt> </dl>                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 


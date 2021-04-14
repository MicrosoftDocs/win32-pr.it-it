---
title: D2D1_TAG (D2d1. h)
description: Valore a 64 bit definito dall'applicazione usato per \ 160; contrassegnare un set di operazioni di rendering.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340573"
---
# <a name="d2d1_tag"></a>\_Tag d2d1

Valore a 64 bit definito dall'applicazione utilizzato per contrassegnare un set di operazioni di rendering.


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a>Commenti

Per impostare un tag prima di una serie di operazioni di rendering, usare il metodo [**ID2D1RenderTarget:: setags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) . Per recuperare il tag corrente, usare il metodo [**ID2D1RenderTarget:: GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**Tag di**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 


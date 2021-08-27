---
title: D2D1_TAG (D2d1.h)
description: Valore a 64 bit definito dall'applicazione usato per contrassegnare un set di operazioni di rendering.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3dbea9f7c86f08a1c3c5df22b419bc5800db473aceed9f9a682a9d2e346a6a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108871"
---
# <a name="d2d1_tag"></a>D2D1 \_ TAG

Valore a 64 bit definito dall'applicazione usato per contrassegnare un set di operazioni di rendering.


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a>Commenti

Per impostare un tag prima di una serie di operazioni di rendering, usare il [**metodo ID2D1RenderTarget::SetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) Per recuperare il tag corrente, usare il [**metodo ID2D1RenderTarget::GetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e Aggiornamento piattaforma per Windows app desktop di Vista \[ \| app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop Windows Server 2008 \[ \| app UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 


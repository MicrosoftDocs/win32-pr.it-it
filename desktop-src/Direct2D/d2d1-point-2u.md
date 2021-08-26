---
title: D2D1_POINT_2U (D2DBaseTypes.h)
description: Rappresenta una coppia di coordinate x e y nello spazio bidimensionale. | D2D1_POINT_2U (D2DBaseTypes.h)
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9fc133cb7f4abd952dd0575e8a3d7af096128ab5e4570b773a4ccc7530364e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108881"
---
# <a name="d2d1_point_2u"></a>D2D1 \_ POINT \_ 2U

Rappresenta una coppia di coordinate x e y nello spazio bidimensionale.


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a>Commenti

I punti in Direct2D sono rappresentati dalle strutture [**D2D1 \_ POINT \_ 2F**](d2d1-point-2f.md) o **D2D1 \_ POINT \_ 2U.** Entrambi contengono una coppia di coordinate x e y nello spazio bidimensionale. La **struttura D2D1 \_ POINT \_ 2F** archivia le coordinate come valori **FLOAT** e la struttura **D2D1 \_ POINT \_ 2U** le archivia come **valori UINT32.**

**D2D1 \_ POINT \_ 2U** è un nuovo nome per il tipo [**D2D \_ POINT \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)già definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e Aggiornamento piattaforma per Windows app desktop di Vista \[ \| app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per Windows app desktop di Windows Server 2008 \[ app desktop \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2DBaseTypes.h (includere D2d1.h)</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PUNTO D2D \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[**PUNTO D2D \_ \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 






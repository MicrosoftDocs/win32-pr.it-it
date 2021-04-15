---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Archivia una coppia ordinata di float, in genere la larghezza e l'altezza di un rettangolo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475868"
---
# <a name="d2d1_size_f"></a>\_Dimensioni d2d1 \_ F

Archivia una coppia ordinata di float, in genere la larghezza e l'altezza di un rettangolo.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Commenti

Analogamente ai punti, le dimensioni rappresentano un altro concetto di grafica importante. In Direct2D le dimensioni sono rappresentate dalle **strutture \_ d2d1 \_ F** o [**d2d1 \_ size \_ U**](d2d1-size-u.md) . Entrambi contengono una coppia ordinata di numeri, in genere la larghezza e l'altezza di un rettangolo. La struttura **d2d1 della \_ dimensione \_ F** contiene una coppia ordinata di valori **float** e la struttura **\_ \_ U d2d1 size** contiene una coppia ordinata di valori **UInt32** .

**D2d1 \_ SIZE \_ f** è un nuovo nome per un tipo già definito **D2D \_ size \_ f**. Per un elenco dei campi forniti da **d2d1 \_ size \_ f**, vedere **D2D \_ size \_ f**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2DBaseTypes. h (include D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dimensioni D2D \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**D2D1 \_ dimensioni \_ U**](d2d1-size-u.md)
</dt> <dt>

[**D2D1 \_ punto \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 


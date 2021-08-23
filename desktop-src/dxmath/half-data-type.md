---
description: Alias di uint16 t contenente un numero a virgola mobile a 16 bit costituito da un bit di segno, un esponente distorto a 5 bit e una \_ mantissa a 10 bit.
ms.assetid: E84E0EBA-5C34-41AA-84DB-7A65EBDCAD15
title: Tipo di dati HALF (DirectXPackedVector.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b7288324ae5935a23e67a35f402ab6041da55073915d812b39096cab30733
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985041"
---
# <a name="half-data-type"></a>Tipo di dati HALF

Alias di **uint16 \_ t** contenente un numero a virgola mobile a 16 bit costituito da un bit di segno, un esponente distorto a 5 bit e una mantissa a 10 bit.


```C++
typedef uint16_t HALF;
```



## <a name="remarks"></a>Commenti

Il tipo di dati HALF è equivalente al formato binario 16 IEEE 754.

HALF \_ MIN = 6,10352e-5f

HALF \_ MAX = 65504.f

Per altre informazioni sul tipo di dati HALF, vedere [Formato a virgola mobile a mezza precisione.](https://en.wikipedia.org/wiki/Half_precision_floating-point_format)

**Spazio** dei nomi: usare DirectX::P ackedVector

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con Windows SDK per Windows 8. Supportato per app desktop Win32, app Windows Store e app Windows Phone 8.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXPackedVector.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di libreria DirectXMath](ovw-xnamath-reference-types.md)
</dt> </dl>

 

 





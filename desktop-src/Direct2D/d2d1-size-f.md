---
title: D2D1_SIZE_F (D2DBaseTypes.h)
description: Archivia una coppia ordinata di valori float, in genere la larghezza e l'altezza di un rettangolo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7068319c161d7d6b288da6d3a451d8cdfdda715b9890160d17cc7fe872322381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087761"
---
# <a name="d2d1_size_f"></a>D2D1 \_ SIZE \_ F

Archivia una coppia ordinata di valori float, in genere la larghezza e l'altezza di un rettangolo.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Commenti

Come i punti, le dimensioni sono un altro concetto di grafica importante. In Direct2D le dimensioni sono rappresentate dalle **strutture D2D1 \_ SIZE \_ F** o [**D2D1 \_ SIZE \_ U.**](d2d1-size-u.md) Entrambi contengono una coppia ordinata di numeri, in genere la larghezza e l'altezza di un rettangolo. La **struttura D2D1 \_ SIZE \_ F** contiene una coppia ordinata di valori **FLOAT** e la struttura **D2D1 \_ SIZE \_ U** contiene una coppia ordinata di **valori UINT32.**

**D2D1 \_ SIZE \_ F** è un nuovo nome per un tipo **D2D SIZE F già \_ \_ definito.** Per un elenco dei campi forniti da **D2D1 \_ SIZE \_ F,** vedere **D2D \_ SIZE \_ F**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e l'aggiornamento della piattaforma per Windows app desktop di Vista \[ \| per le app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e Aggiornamento della piattaforma per app desktop Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2DBaseTypes.h (includere D2d1.h)</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DIMENSIONI D2D \_ \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**D2D1 \_ SIZE \_ U**](d2d1-size-u.md)
</dt> <dt>

[**D2D1 \_ POINT \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 


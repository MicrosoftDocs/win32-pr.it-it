---
description: Flag che indica se i requisiti del buffer sono stati modificati.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Membro CBaseAllocator:: m_bChanged (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331556"
---
# <a name="cbaseallocatorm_bchanged-member"></a>Membro bChanged di CBaseAllocator:: m \_

Flag che indica se i requisiti del buffer sono stati modificati. Il metodo [**CBaseAllocator:: seproperties**](cbaseallocator-setproperties.md) imposta il valore su **true**. In una classe derivata, il metodo virtuale pure [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) deve impostare di nuovo il valore su **false**. Una volta allocati i buffer, non è necessario riallocarli mentre *m \_ BChanged* è **false**.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 





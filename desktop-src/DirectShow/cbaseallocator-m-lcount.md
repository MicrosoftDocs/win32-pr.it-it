---
description: Numero di buffer da fornire.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Membro CBaseAllocator:: m_lCount (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329872"
---
# <a name="cbaseallocatorm_lcount-member"></a>Membro lCount di CBaseAllocator:: m \_

Numero di buffer da fornire. Il metodo [**CBaseAllocator:: seproperties**](cbaseallocator-setproperties.md) imposta questo valore. I buffer non vengono allocati fino a quando non viene chiamato il metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) . Il numero corrente di buffer allocati viene specificato dalla variabile membro [**CBaseAllocator:: m \_ lAllocated**](cbaseallocator-m-lallocated.md) .

## <a name="syntax"></a>Sintassi


```C++
long m_lCount;
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

 

 





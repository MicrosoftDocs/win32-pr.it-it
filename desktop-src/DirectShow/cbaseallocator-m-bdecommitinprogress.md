---
description: Flag che indica se un'operazione di decommit è in corso.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Membro CBaseAllocator:: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326204"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>Membro bDecommitInProgress di CBaseAllocator:: m \_

Flag che indica se un'operazione di decommit è in corso. Il valore è **true** dopo la chiamata del metodo [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , ma prima del rilascio di tutti i buffer. Se il valore è **true**, il metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) ha esito negativo. Inoltre, l'allocatore non deve eliminare se stesso mentre il valore è **true**.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bDecommitInProgress;
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

 

 





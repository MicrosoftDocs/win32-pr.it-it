---
description: Puntatore al blocco di memoria che contiene i buffer.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: Membro CMemAllocator::m_pBuffer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fa9c56c5a90c1fa3fde7dda4bca82cd3f473a591db9e2e24f0b1d141c6aa33e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155983"
---
# <a name="cmemallocatorm_pbuffer-member"></a>Membro CMemAllocator::m \_ pBuffer

Puntatore al blocco di memoria che contiene i buffer.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a>Osservazioni

I buffer di esempio vengono calcolati come offset da questo puntatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 





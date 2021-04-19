---
description: Puntatore al blocco di memoria che contiene i buffer.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: 'Membro CMemAllocator:: m_pBuffer (Amfilter. h)'
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
ms.openlocfilehash: 8ae988474196e323cde24305b0e389ac69f0f10d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333601"
---
# <a name="cmemallocatorm_pbuffer-member"></a>Membro pBuffer di CMemAllocator:: m \_

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
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 





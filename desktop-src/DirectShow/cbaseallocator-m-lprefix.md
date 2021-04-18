---
description: Prefisso di ogni buffer, in byte.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Membro CBaseAllocator:: m_lPrefix (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325787"
---
# <a name="cbaseallocatorm_lprefix-member"></a>Membro lPrefix di CBaseAllocator:: m \_

Prefisso di ogni buffer, in byte. Se il valore è diverso da zero, ogni puntatore del buffer restituito dal metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) è preceduto da un blocco di byte di dimensioni *m \_ lPrefix*. Questo blocco di memoria viene chiamato *prefisso*. La variabile membro [**CBaseAllocator:: m \_ lSize**](cbaseallocator-m-lsize.md) non include il valore del prefisso.

## <a name="syntax"></a>Sintassi


```C++
long m_lPrefix;
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

 

 





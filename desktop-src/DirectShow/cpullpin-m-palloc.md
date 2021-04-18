---
description: La \_ variabile membro pAlloc m è un puntatore all'interfaccia IMemAllocator dell'allocatore di memoria.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Membro CPullPin:: m_pAlloc (Pullpin. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331164"
---
# <a name="cpullpinm_palloc-member"></a>Membro pAlloc di CPullPin:: m \_

La `m_pAlloc` variabile membro è un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore di memoria.

## <a name="syntax"></a>Sintassi


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Osservazioni

Il metodo [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) imposta questa variabile membro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 





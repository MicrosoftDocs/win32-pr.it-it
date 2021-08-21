---
description: La variabile \_ membro m pAlloc è un puntatore all'interfaccia IMemAllocator dell'allocatore di memoria.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: Membro CPullPin::m_pAlloc (Pullpin.h)
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
ms.openlocfilehash: 76abcdadf24006d545a8e8cf51205a99656a634094487104b9bad5d9b553c33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073455"
---
# <a name="cpullpinm_palloc-member"></a>Membro CPullPin::m \_ pAlloc

La `m_pAlloc` variabile membro è un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore di memoria.

## <a name="syntax"></a>Sintassi


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Osservazioni

Il [**metodo CPullPin::D ecideAllocator**](cpullpin-decideallocator.md) imposta questa variabile membro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 





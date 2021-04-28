---
description: Membro CUnknown::m_cRef - Conteggio dei riferimenti.
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: Membro CUnknown::m_cRef (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3f6be7d09149f651bce8d1042b7f3e3a5dc9307
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084579"
---
# <a name="cunknownm_cref-member"></a>Membro cRef CUnknown::m \_

Conteggio dei riferimenti.

## <a name="syntax"></a>Sintassi


```C++
LONG m_cRef;
```



## <a name="remarks"></a>Osservazioni

Usare questa variabile membro se si esegue l'override [**del metodo NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) [**o NonDelegatingRelease.**](cunknown-nondelegatingrelease.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 





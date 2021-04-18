---
description: Conteggio riferimenti.
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'Membro CUnknown:: m_cRef (ComBase. h)'
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
ms.openlocfilehash: 94ff5d88ca48feeb46a8b0411a55d6261aefcf6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331449"
---
# <a name="cunknownm_cref-member"></a>Membro cref di CUnknown:: m \_

Conteggio riferimenti.

## <a name="syntax"></a>Sintassi


```C++
LONG m_cRef;
```



## <a name="remarks"></a>Osservazioni

Usare questa variabile membro se si esegue l'override del metodo [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) o [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 





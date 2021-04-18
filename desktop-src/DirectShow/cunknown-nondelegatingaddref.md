---
description: "Il metodo NonDelegatingAddRef incrementa il conteggio dei riferimenti nell'oggetto. Questo metodo implementa il metodo INonDelegatingUnknown:: NonDelegatingAddRef."
ms.assetid: abb6ee51-8fb8-4307-b127-b3667260e35a
title: Metodo CUnknown. NonDelegatingAddRef (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingAddRef
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f97260c03f0931e94e8ce6de8b7816789b2fe66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331448"
---
# <a name="cunknownnondelegatingaddref-method"></a>CUnknown. NonDelegatingAddRef, metodo

Il `NonDelegatingAddRef` metodo incrementa il conteggio dei riferimenti nell'oggetto. Questo metodo implementa il metodo **INonDelegatingUnknown:: NonDelegatingAddRef** .

## <a name="syntax"></a>Sintassi


```C++
ULONG NonDelegatingAddRef();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il conteggio dei riferimenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 





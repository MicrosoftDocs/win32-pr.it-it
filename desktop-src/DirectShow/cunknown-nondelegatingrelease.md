---
description: Decrementa il conteggio dei riferimenti sull'oggetto. Questo metodo implementa il metodo INonDelegatingUnknown::NonDelegatingRelease.
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Metodo CUnknown.NonDelegatingRelease (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ac5145e1776602c5bb358805c45ec271766fe918b7924d948e286ae32b31794
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821955"
---
# <a name="cunknownnondelegatingrelease-method"></a>Metodo CUnknown.NonDelegatingRelease

Decrementa il conteggio dei riferimenti sull'oggetto. Questo metodo implementa il **metodo INonDelegatingUnknown::NonDelegatingRelease.**

## <a name="syntax"></a>Sintassi


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il conteggio dei riferimenti.

## <a name="remarks"></a>Commenti

Quando il conteggio dei riferimenti raggiunge lo zero, l'oggetto si elimina.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 





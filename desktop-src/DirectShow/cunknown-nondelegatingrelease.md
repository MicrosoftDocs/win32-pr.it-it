---
description: "Decrementa il conteggio dei riferimenti nell'oggetto. Questo metodo implementa il metodo INonDelegatingUnknown:: NonDelegatingRelease."
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Metodo CUnknown. NonDelegatingRelease (ComBase. h)
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
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331445"
---
# <a name="cunknownnondelegatingrelease-method"></a>CUnknown. NonDelegatingRelease, metodo

Decrementa il conteggio dei riferimenti nell'oggetto. Questo metodo implementa il metodo **INonDelegatingUnknown:: NonDelegatingRelease** .

## <a name="syntax"></a>Sintassi


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il conteggio dei riferimenti.

## <a name="remarks"></a>Commenti

Quando il conteggio dei riferimenti raggiunge zero, l'oggetto viene eliminato automaticamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 





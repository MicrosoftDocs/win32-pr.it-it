---
description: Il metodo CurrentMediaType Recupera il tipo di supporto per la connessione al pin corrente.
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Metodo CTransformOutputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee9ee15c3cda2baf8ab8d6e9cb0ec3c797e91a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330847"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a>CTransformOutputPin. CurrentMediaType, metodo

Il `CurrentMediaType` metodo recupera il tipo di supporto per la connessione al pin corrente.

## <a name="syntax"></a>Sintassi


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento alla variabile membro [**CBasePin:: m \_ mt**](cbasepin-m-mt.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 





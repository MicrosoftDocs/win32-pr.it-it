---
description: Il metodo CurrentMediaType Recupera il tipo di supporto per la connessione al pin corrente.
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: Metodo CTransformInputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59feca88e896b2a81a352b693e57ceaa5388d452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328802"
---
# <a name="ctransforminputpincurrentmediatype-method"></a>CTransformInputPin. CurrentMediaType, metodo

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



 

 





---
description: Il metodo GetSampleSize recupera le dimensioni del campione.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Metodo CMediaType. GetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324006"
---
# <a name="cmediatypegetsamplesize-method"></a>CMediaType. GetSampleSize, metodo

Il `GetSampleSize` metodo recupera le dimensioni del campione.

## <a name="syntax"></a>Sintassi


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se la dimensione del campione è fissa, restituisce le dimensioni del campione in byte. In caso contrario, restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 





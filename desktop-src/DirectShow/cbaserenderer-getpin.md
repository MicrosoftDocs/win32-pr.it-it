---
description: Il metodo GetPin recupera un PIN.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Metodo CBaseRenderer. GetPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325519"
---
# <a name="cbaserenderergetpin-method"></a>CBaseRenderer. GetPin, metodo

Il `GetPin` metodo recupera un PIN.

## <a name="syntax"></a>Sintassi


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero del PIN specificato. Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il puntatore [**\_ pInputPin CBaseRenderer:: m**](cbaserenderer-m-pinputpin.md) .

## <a name="remarks"></a>Commenti

Questo metodo implementa il metodo [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) , che è virtuale puro nella classe **CBaseFilter** . Il filtro supporta esattamente un pin (il pin di input). La prima volta che questo metodo viene chiamato, crea il PIN come nuovo oggetto [**CRendererInputPin**](crendererinputpin.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





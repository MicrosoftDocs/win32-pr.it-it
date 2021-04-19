---
description: 'Il metodo serate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking:: SetValue.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Metodo CPosPassThru. serate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ada5c8bc8d265b33e1d4b243bdfd0cf8bf03a7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328502"
---
# <a name="cpospassthrusetrate-method"></a>CPosPassThru. serate (metodo)

Il `SetRate` metodo imposta la velocità di riproduzione. Questo metodo implementa il metodo [**IMediaSeeking::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) SetValue.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dRate* 
</dt> <dd>

Velocità di riproduzione. Non deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ INVALIDARG se *drate* è zero. In caso contrario, restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 





---
description: 'Il metodo GetPreroll recupera la quantità di dati che verranno accodati prima della posizione iniziale. Questo metodo implementa il metodo IMediaSeeking:: GetPreroll.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Metodo CPosPassThru. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329756"
---
# <a name="cpospassthrugetpreroll-method"></a>CPosPassThru. GetPreroll, metodo

Il `GetPreroll` metodo recupera la quantità di dati che verranno accodati prima della posizione iniziale. Questo metodo implementa il metodo [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pllPreroll* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di preregistrazione, in unità del formato dell'ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 





---
description: 'Il metodo StartAt comunica al pin quando iniziare a consegnare i dati. Questo metodo implementa il metodo IAMStreamControl:: StartAt.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Metodo CBaseStreamControl. StartAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324028"
---
# <a name="cbasestreamcontrolstartat-method"></a>CBaseStreamControl. StartAt, metodo

Il `StartAt` metodo informa il PIN quando iniziare a consegnare i dati. Questo metodo implementa il metodo [**IAMStreamControl:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ptStart* 
</dt> <dd>

Puntatore a un valore di [**\_ ora di riferimento**](reference-time.md) che specifica quando il PIN deve iniziare a consegnare i dati.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Specifica un valore da inviare insieme alla notifica di avvio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 





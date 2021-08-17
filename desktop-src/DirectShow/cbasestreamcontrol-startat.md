---
description: Il metodo StartAt indica al pin quando iniziare a recapitare i dati. Questo metodo implementa il metodo IAMStreamControl::StartAt.
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Metodo CBaseStreamControl.StartAt (Strmctl.h)
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
ms.openlocfilehash: b40570933e7eed054694b2da927d71e077b86941aea816ff2ca6de5c91372b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814111"
---
# <a name="cbasestreamcontrolstartat-method"></a>Metodo CBaseStreamControl.StartAt

Il `StartAt` metodo indica al pin quando iniziare a recapitare i dati. Questo metodo implementa il [**metodo IAMStreamControl::StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat)

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

Puntatore a un [**valore \_ REFERENCE TIME**](reference-time.md) che specifica quando il pin deve iniziare a recapitare i dati.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Specifica un valore da inviare insieme alla notifica di avvio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 





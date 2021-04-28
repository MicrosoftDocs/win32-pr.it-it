---
description: "Metodo CPosPassThru.GetTimeFormat: il metodo GetTimeFormat recupera il formato dell'ora corrente. Questo metodo implementa il metodo IMediaSeeking::GetTimeFormat."
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Metodo CPosPassThru.GetTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903d1c6163d4cad5c5b9ca22213b02542bb3da49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085589"
---
# <a name="cpospassthrugettimeformat-method"></a>Metodo CPosPassThru.GetTimeFormat

Il `GetTimeFormat` metodo recupera il formato dell'ora corrente. Questo metodo implementa il [**metodo IMediaSeeking::GetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a una variabile che riceve un GUID di formato ora.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> <dt>

[**GUID di formato ora**](time-format-guids.md)
</dt> </dl>

 

 





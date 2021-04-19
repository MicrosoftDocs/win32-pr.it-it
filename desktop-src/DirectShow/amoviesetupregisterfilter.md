---
description: Obsoleta. In alternativa, usare AMovieSetupRegisterFilter2.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Funzione AMovieSetupRegisterFilter (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329165"
---
# <a name="amoviesetupregisterfilter-function"></a>AMovieSetupRegisterFilter (funzione)

Obsoleta. In alternativa, usare [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*psetupdata* 
</dt> <dd>

Riservato.

</dd> <dt>

*pIFM* 
</dt> <dd>

Riservato.

</dd> <dt>

*bRegister* 
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dllsetup. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni di installazione DLL**](dll-setup-functions.md)
</dt> </dl>

 

 





---
description: Il metodo IsUsingTimeFormat determina se un formato di ora specificato è il formato attualmente in uso.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Metodo CSourceSeeking. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329496"
---
# <a name="csourceseekingisusingtimeformat-method"></a>CSourceSeeking. IsUsingTimeFormat, metodo

Il `IsUsingTimeFormat` metodo determina se un formato di ora specificato è il formato attualmente in uso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a un GUID del formato ora. Vedere [**GUID del formato ora**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Il formato specificato non è quello corrente.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Il formato specificato è il formato corrente.<br/>     |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null** .<br/>                      |



 

## <a name="remarks"></a>Commenti

L'unico formato di ora supportato dalla classe base è il \_ tempo medio di formato dell'ora \_ \_ (unità 100-nanosecondi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 





---
description: Il metodo IsUsingTimeFormat determina se un formato di ora specificato è il formato attualmente in uso.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Metodo CSourceSeeking.IsUsingTimeFormat (Ctlutil.h)
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
ms.openlocfilehash: b930746102bc43e3549b4565a7591f4ac5fee8cc6503d9fb6aadcbe1659a52f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054241"
---
# <a name="csourceseekingisusingtimeformat-method"></a>Metodo CSourceSeeking.IsUsingTimeFormat

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

Puntatore a un GUID di formato ora. Vedere [**GUID di formato dell'ora.**](time-format-guids.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Il formato specificato non è il formato corrente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il formato specificato è il formato corrente.<br/>     |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Argomento del puntatore **NULL.**<br/>                      |



 

## <a name="remarks"></a>Commenti

L'unico formato di ora supportato dalla classe di base è TIME \_ FORMAT \_ MEDIA TIME \_ (unità di 100 nanosecondi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 





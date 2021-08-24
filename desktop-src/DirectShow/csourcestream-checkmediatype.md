---
description: Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico. Questo metodo implementa il metodo CBasePin::CheckMediaType virtuale puro.
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Metodo CSourceStream.CheckMediaType (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb900d4de448b59eadb4cfd4de28aebf3ac07845fff6a2769c003d37cac846a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633931"
---
# <a name="csourcestreamcheckmediatype-method"></a>Metodo CSourceStream.CheckMediaType

Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico. Questo metodo implementa il metodo [**CBasePin::CheckMediaType virtuale**](cbasepin-checkmediatype.md) puro.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                            | Descrizione                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Questo pin supporta questo tipo di supporto.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Il pin non supporta questo tipo di supporto.<br/> |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il pin supporta un singolo tipo di supporto. Questo metodo recupera il tipo supportato chiamando la versione a parametro singolo del metodo [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) e lo confronta con il tipo proposto. Se il pin supporta più di un tipo di supporto, eseguire l'override di questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 





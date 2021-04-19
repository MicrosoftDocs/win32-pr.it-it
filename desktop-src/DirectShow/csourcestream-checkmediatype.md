---
description: 'Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico. Questo metodo implementa il Metodo CBasePin:: CheckMediaType virtuale puro.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Metodo CSourceStream. CheckMediaType (source. h)
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
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329032"
---
# <a name="csourcestreamcheckmediatype-method"></a>CSourceStream. CheckMediaType, metodo

Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico. Questo metodo implementa il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtuale puro.

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

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                            | Descrizione                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Questo pin supporta questo tipo di supporto.<br/>        |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Il PIN non supporta questo tipo di supporto.<br/> |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il pin supporta un solo tipo di supporto. Questo metodo recupera il tipo supportato chiamando la versione a parametro singolo del metodo [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) e lo confronta con il tipo proposto. Se il pin supporta più di un tipo di supporto, eseguire l'override di questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 





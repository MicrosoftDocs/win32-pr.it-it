---
description: Questo operatore consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'Metodo CMediaType. CMediaType:: operator = (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 748ad2efae39fc6a7b26c39d10351c44a5cee8a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332325"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a>Metodo CMediaType. CMediaType:: operator = (mtype. h)

Questo operatore consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.

## <a name="syntax"></a>Sintassi


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Riferimento a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un riferimento all'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 





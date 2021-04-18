---
description: Il metodo FindPin Recupera il pin con l'identificatore specificato.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Metodo CBaseRenderer. FindPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329383"
---
# <a name="cbaserendererfindpin-method"></a>CBaseRenderer. FindPin, metodo

Il `FindPin` metodo recupera il pin con l'identificatore specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id* 
</dt> <dd>

Puntatore a una stringa di caratteri wide a terminazione null che identifica il PIN. Deve essere L "in".

</dd> <dt>

*ppPin* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN. Se il metodo ha esito negativo, *\* ppPin* è impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>         | Argomento puntatore **null** .<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ trovato**</dt> </dl> | Non trovato.<br/>                 |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseFilter:: FindPin**](cbasefilter-findpin.md) . Il solo pin del filtro (il pin di input) è denominato "in".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





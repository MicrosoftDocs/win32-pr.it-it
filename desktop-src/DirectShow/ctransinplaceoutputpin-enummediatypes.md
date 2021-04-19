---
description: 'Il metodo EnumMediaTypes enumera i tipi di supporto preferiti del PIN. Questo metodo implementa il metodo IPin:: EnumMediaTypes.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Metodo CTransInPlaceOutputPin. EnumMediaTypes (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d214004412264272c64d0efaf20a5da7e1ca3cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326178"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>CTransInPlaceOutputPin. EnumMediaTypes, metodo

Il `EnumMediaTypes` metodo enumera i tipi di supporto preferiti del PIN. Questo metodo implementa il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* 
</dt> <dd>

Riceve un puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                                 |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>         | Memoria insufficiente.<br/>                     |
| <dl> <dt>**\_puntatore E**</dt> </dl>             | Puntatore **null** .<br/>                        |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il pin di input del filtro non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce l'interfaccia **IEnumMediaTypes** dal pin di output a Monte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 





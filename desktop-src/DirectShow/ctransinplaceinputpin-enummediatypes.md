---
description: 'Il metodo EnumMediaTypes enumera i tipi di supporto preferiti del PIN. Questo metodo implementa il metodo IPin:: EnumMediaTypes.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Metodo CTransInPlaceInputPin. EnumMediaTypes (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa634fa695eb0007b49fc1c36c730c7fbde361b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326201"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a>CTransInPlaceInputPin. EnumMediaTypes, metodo

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



| Codice restituito                                                                                           | Descrizione                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>         | Memoria insufficiente.<br/>             |
| <dl> <dt>**\_puntatore E**</dt> </dl>             | Puntatore **null** .<br/>                |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il pin di output non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce l'interfaccia **IEnumMediaTypes** dal pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 





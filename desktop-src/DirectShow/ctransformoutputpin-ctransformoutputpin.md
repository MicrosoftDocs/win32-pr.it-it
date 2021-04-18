---
description: Metodo del costruttore.
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: Costruttore CTransformOutputPin. CTransformOutputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 730149ae67abb2924174954bb8b620a02cfae2b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330848"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a>Costruttore CTransformOutputPin. CTransformOutputPin

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CTransformOutputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObjectName* 
</dt> <dd>

Stringa contenente il nome di debug dell'oggetto. Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pTransformFilter* 
</dt> <dd>

Puntatore al filtro che ha creato questo pin, che deve essere un oggetto [**CTransformFilter**](ctransformfilter.md) .

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto. Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*pName* 
</dt> <dd>

Stringa di caratteri wide contenente il nome del PIN.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il parametro *pname* specifica il nome del PIN, restituito dal metodo [**Ipin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . Tuttavia, la stringa non viene utilizzata per l'identificatore del PIN. L'identificatore del PIN per questa classe è sempre "out". Per ulteriori informazioni, vedere [**QueryId**](ctransformoutputpin-queryid.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 





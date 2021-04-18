---
description: Metodo del costruttore.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Costruttore CTransformInputPin. CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39b99e3e2cf1437c1b35f68d9863a692746bd98d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328808"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>Costruttore CTransformInputPin. CTransformInputPin

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CTransformInputPin(
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

Il parametro *pname* specifica il nome del PIN, restituito dal metodo [**Ipin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . Tuttavia, la stringa non viene utilizzata per l'identificatore del PIN. L'identificatore del PIN per questa classe è sempre "in". Per ulteriori informazioni, vedere [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 





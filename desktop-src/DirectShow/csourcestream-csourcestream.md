---
description: Metodo del costruttore.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Costruttore CSourceStream. CSourceStream (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327116"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Costruttore CSourceStream. CSourceStream

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObjectName* 
</dt> <dd>

Puntatore a una stringa contenente il nome di debug del PIN.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto. Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*PM* 
</dt> <dd>

Puntatore al filtro [**CSource**](csource.md) che ha creato questo pin.

</dd> <dt>

*pName* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del PIN.

</dd> </dl>

## <a name="remarks"></a>Commenti

La stringa specificata nel parametro *pObjectName* viene utilizzata solo a scopo di debug. Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).

La stringa specificata nel parametro *pname* è il nome restituito dal metodo [**Ipin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . La `CSourceStream` classe non usa questo nome per l'identificatore del pin restituito dal metodo [**CSourceStream:: QueryId**](csourcestream-queryid.md) . Al contrario, **QueryId** calcola un identificatore del PIN in base al numero del PIN. Gli identificatori di pin supportano la persistenza del grafo. Per ulteriori informazioni, vedere [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).

Il costruttore aggiunge automaticamente il PIN al filtro proprietario chiamando [**CSource:: AddPin**](csource-addpin.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 





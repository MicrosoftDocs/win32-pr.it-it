---
description: 'Costruttore CSourceStream.CSourceStream : metodo costruttore.'
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Costruttore CSourceStream.CSourceStream (Source.h)
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
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085189"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Costruttore CSourceStream.CSourceStream

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

Puntatore a una stringa contenente il nome di debug del segnaposto.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto . Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*Pms* 
</dt> <dd>

Puntatore al [**filtro CSource**](csource.md) che ha creato questo segnaposto.

</dd> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del segnaposto.

</dd> </dl>

## <a name="remarks"></a>Commenti

La stringa specificata nel *parametro pObjectName* viene usata solo a scopo di debug. Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)

La stringa specificata nel *parametro pName* è il nome restituito dal [**metodo IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) La `CSourceStream` classe non usa questo nome per l'identificatore pin restituito dal metodo [**CSourceStream::QueryId.**](csourcestream-queryid.md) QueryId calcola **invece** un identificatore pin in base al numero di pin. Gli identificatori pin supportano la persistenza del grafo. Per altre informazioni, vedere [**IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)

Il costruttore aggiunge automaticamente il pin al filtro proprietario chiamando [**CSource::AddPin**](csource-addpin.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 





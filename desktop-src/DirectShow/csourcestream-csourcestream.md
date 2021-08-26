---
description: 'Costruttore CSourceStream.CSourceStream : metodo del costruttore.'
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
ms.openlocfilehash: e02827c74ef4c5461a5777221e1839846b855a4b2f4cd27d97ce913399787ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053851"
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

Puntatore a una stringa contenente il nome di debug del pin.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto . Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*Pms* 
</dt> <dd>

Puntatore al [**filtro CSource**](csource.md) che ha creato questo pin.

</dd> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del segnaposto.

</dd> </dl>

## <a name="remarks"></a>Commenti

La stringa specificata nel *parametro pObjectName* viene usata solo a scopo di debug. Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).

La stringa specificata nel *parametro pName* è il nome restituito dal [**metodo IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) La `CSourceStream` classe non usa questo nome per l'identificatore pin restituito dal metodo [**CSourceStream::QueryId.**](csourcestream-queryid.md) QueryId  calcola invece un identificatore pin in base al numero pin. Gli identificatori pin supportano la persistenza del grafo. Per altre informazioni, vedere [**IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)

Il costruttore aggiunge automaticamente il pin al filtro proprietario chiamando [**CSource::AddPin**](csource-addpin.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 





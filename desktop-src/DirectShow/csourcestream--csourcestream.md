---
description: 'Distruttore CSourceStream.~CSourceStream : metodo del distruttore.'
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Distruttore CSourceStream.~CSourceStream (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085209"
---
# <a name="csourcestreamcsourcestream-destructor"></a>Distruttore CSourceStream.~CSourceStream

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
~CSourceStream();
```



## <a name="remarks"></a>Osservazioni

Il distruttore rimuove automaticamente il segnaposto dal filtro proprietario chiamando [**CSource::RemovePin**](csource-removepin.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 





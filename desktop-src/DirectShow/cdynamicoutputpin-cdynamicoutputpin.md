---
description: Metodo del costruttore.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Costruttore CDynamicOutputPin. CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f45a2fee25796f39c7d8b358b1ac83e4a5b1daa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333454"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a>Costruttore CDynamicOutputPin. CDynamicOutputPin

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObjectName* 
</dt> <dd>

Puntatore a una stringa che contiene il nome dell'oggetto. Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntatore al filtro che ha creato questo pin.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntatore a un blocco [**CCritSec**](ccritsec.md) , usato per serializzare le modifiche di stato. Usare la stessa sezione critica del blocco del filtro, [ **CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md)

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto. Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*pName* 
</dt> <dd>

Puntatore a una stringa di caratteri wide contenente l'identificatore del PIN. Per ulteriori informazioni, vedere [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 





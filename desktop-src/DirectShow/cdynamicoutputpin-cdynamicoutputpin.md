---
description: 'Costruttore CDynamicOutputPin.CDynamicOutputPin : metodo del costruttore.'
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Costruttore CDynamicOutputPin.CDynamicOutputPin (Amfilter.h)
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
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099309"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a>Costruttore CDynamicOutputPin.CDynamicOutputPin

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

Puntatore a una stringa contenente il nome dell'oggetto. Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntatore al filtro che ha creato questo segnaposto.

</dd> <dt>

*Plock* 
</dt> <dd>

Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato. Usare la stessa sezione critica del blocco del filtro, [ **CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto . Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa di caratteri wide contenente l'identificatore pin. Per altre informazioni, vedere [**IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 





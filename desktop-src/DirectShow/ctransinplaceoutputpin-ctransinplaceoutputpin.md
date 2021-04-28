---
description: Costruttore CTransInPlaceOutputPin.CTransInPlaceOutputPin - Metodo costruttore.
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: Costruttore CTransInPlaceOutputPin.CTransInPlaceOutputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b63ee3aa52bc0363bcab90275be4148659b3bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094709"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a>Costruttore CTransInPlaceOutputPin.CTransInPlaceOutputPin

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObjectName* 
</dt> <dd>

Stringa contenente il nome di debug dell'oggetto. Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntatore al filtro che ha creato questo pin, che deve essere un [**oggetto CTransInPlaceFilter.**](ctransinplacefilter.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto . Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*Pname* 
</dt> <dd>

Stringa di caratteri wide contenente il nome del pin.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il *parametro pName* specifica il nome del pin, restituito dal metodo [**IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) Tuttavia, la stringa non viene usata per l'identificatore pin. L'identificatore pin per questa classe è sempre "Out". Per altre informazioni, vedere [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 





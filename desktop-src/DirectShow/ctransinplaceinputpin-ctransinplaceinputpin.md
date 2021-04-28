---
description: Costruttore CTransInPlaceInputPin.CTransInPlaceInputPin - Metodo costruttore.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Costruttore CTransInPlaceInputPin.CTransInPlaceInputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f97c89142e43691c91b2a4c0d04721d9112ed49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084759"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a>Costruttore CTransInPlaceInputPin.CTransInPlaceInputPin

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CTransInPlaceInputPin(
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

Il *parametro pName* specifica il nome del pin, restituito dal metodo [**IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) Tuttavia, questa stringa non viene usata per l'identificatore pin. L'identificatore pin per questa classe è sempre In. Per altre informazioni, vedere [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 





---
description: 'Costruttore CTransformOutputPin.CTransformOutputPin : metodo costruttore.'
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: Costruttore CTransformOutputPin.CTransformOutputPin (Transfrm.h)
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
ms.openlocfilehash: a1f7cb9dd811c878eba258a6087e00a85d4c24a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084869"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a>Costruttore CTransformOutputPin.CTransformOutputPin

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

Stringa contenente il nome di debug dell'oggetto. Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*pTransformFilter* 
</dt> <dd>

Puntatore al filtro che ha creato questo segnaposto, che deve essere un [**oggetto CTransformFilter.**](ctransformfilter.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo. Inizializzare il valore su S \_ OK prima di creare l'oggetto . Il valore viene modificato solo se si verifica un errore.

</dd> <dt>

*Pname* 
</dt> <dd>

Stringa di caratteri wide contenente il nome del segnaposto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il *parametro pName* specifica il nome del pin, restituito dal [**metodo IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) Tuttavia, la stringa non viene usata per l'identificatore pin. L'identificatore pin per questa classe è sempre "Out". Per altre informazioni, vedere [**QueryId.**](ctransformoutputpin-queryid.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 





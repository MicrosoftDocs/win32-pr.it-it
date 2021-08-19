---
description: 'Costruttore CTransformInputPin.CTransformInputPin : metodo costruttore.'
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Costruttore CTransformInputPin.CTransformInputPin (Transfrm.h)
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
ms.openlocfilehash: 76c19a883e7cfb416e557a23cf2a689e46dab36641ffc98cde5cbe5fe460f686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053571"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>Costruttore CTransformInputPin.CTransformInputPin

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

Stringa contenente il nome di debug dell'oggetto . Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)

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

Il *parametro pName* specifica il nome del pin, restituito dal [**metodo IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) Tuttavia, la stringa non viene usata per l'identificatore pin. L'identificatore pin per questa classe è sempre "In". Per altre informazioni, vedere [**QueryId.**](ctransforminputpin-queryid.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 





---
description: 'Costruttore CBaseMediaFilter.CBaseMediaFilter : metodo del costruttore.'
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Costruttore CBaseMediaFilter.CBaseMediaFilter (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096319"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>Costruttore CBaseMediaFilter.CBaseMediaFilter

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa contenente il nome dell'oggetto.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Plock* 
</dt> <dd>

Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato.

</dd> <dt>

*Clsid* 
</dt> <dd>

Identificatore di classe dell'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se un altro oggetto contiene o aggrega `CBaseMediaFilter` l'oggetto, il **blocco CCritSec** potrebbe essere esterno all'oggetto. `CBaseMediaFilter` In tal caso, passare un puntatore al blocco in *pLock*.

In caso contrario, è possibile:

-   Derivare una classe che eredita sia `CBaseMediaFilter` che **CCritSec**. Per *pLock*, passare il puntatore this.
-   Derivare una classe che eredita `CBaseMediaFilter` e contiene una variabile membro **CCritSec.** Per *pLock*, passare l'indirizzo di tale variabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 





---
description: Metodo del costruttore.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Costruttore CBaseMediaFilter. CBaseMediaFilter (Amfilter. h)
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
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325671"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>Costruttore CBaseMediaFilter. CBaseMediaFilter

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

*pName* 
</dt> <dd>

Puntatore a una stringa che contiene il nome dell'oggetto.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **null**.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntatore a un blocco [**CCritSec**](ccritsec.md) , usato per serializzare le modifiche di stato.

</dd> <dt>

*CLSID* 
</dt> <dd>

Identificatore di classe dell'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se un altro oggetto contiene o aggrega l' `CBaseMediaFilter` oggetto, il blocco **CCritSec** potrebbe essere esterno all' `CBaseMediaFilter` oggetto. In tal caso, passare un puntatore al blocco in *pLock*.

In caso contrario, è possibile:

-   Derivare una classe che eredita sia che `CBaseMediaFilter` **CCritSec**. Per *pLock*, passare il puntatore this.
-   Derivare una classe che eredita `CBaseMediaFilter` e contiene una variabile membro **CCritSec** . Per *pLock*, passare l'indirizzo della variabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 





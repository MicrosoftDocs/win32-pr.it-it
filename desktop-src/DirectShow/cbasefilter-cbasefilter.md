---
description: Costruttore CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ) - Metodo costruttore.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Costruttore CBaseFilter.CBaseFilter(const *TCHAR, LPUNKNOWN, CCritSec,* REFCLSID, HRESULT*) (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120109"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a>Costruttore CBaseFilter.CBaseFilter(const \* TCHAR, LPUNKNOWN, CCritSec, \* REFCLSID, \* HRESULT)

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa contenente il nome del filtro, a scopo di debug.

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

Identificatore di classe (CLSID) del filtro.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Il costruttore ignora questo parametro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per l'oggetto sezione critica, è in genere necessario eseguire una delle operazioni seguenti:

-   Derivare una classe che eredita **sia CBaseFilter** che **CCritSec.** Per *pLock*, passare il `this` puntatore .
-   Derivare una classe che eredita **CBaseFilter** e contiene una **variabile membro CCritSec.** Per *pLock*, passare l'indirizzo di tale variabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





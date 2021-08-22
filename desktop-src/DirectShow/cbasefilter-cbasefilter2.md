---
description: Costruttore CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID) - Metodo costruttore.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Costruttore CBaseFilter.CBaseFilter(const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID) (Amfilter.h)
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
ms.openlocfilehash: 8455e78096af7bc2ca82a2b7634ceac14b2bdf6e918f62f8ae0fa64308f4b9a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640651"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a>Costruttore CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseFilter(
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

</dd> </dl>

## <a name="remarks"></a>Commenti

Per l'oggetto sezione critica, in genere è necessario eseguire una delle operazioni seguenti:

-   Derivare una classe che eredita **sia CBaseFilter che** **CCritSec.** Per *pLock*, passare il `this` puntatore .
-   Derivare una classe che eredita **CBaseFilter** e contiene una **variabile membro CCritSec.** Per *pLock*, passare l'indirizzo di tale variabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





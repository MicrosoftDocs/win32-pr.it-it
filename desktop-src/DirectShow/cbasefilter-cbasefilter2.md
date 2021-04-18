---
description: Metodo del costruttore.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Costruttore CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID) (Amfilter. h)
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
ms.openlocfilehash: 40ac48a1fd28b9b50a8f1fa9c698ea5db49d97b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325080"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a>Costruttore CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)

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

*pName* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del filtro, a scopo di debug.

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

Identificatore di classe (CLSID) del filtro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per l'oggetto sezione critica, in genere si esegue una delle operazioni seguenti:

-   Derivare una classe che eredita sia **CBaseFilter** che **CCritSec**. Per *pLock*, passare il `this` puntatore.
-   Derivare una classe che eredita **CBaseFilter** e contiene una variabile membro **CCritSec** . Per *pLock*, passare l'indirizzo della variabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





---
description: Il metodo CreateInstance crea una nuova istanza di questo oggetto.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Metodo CSystemClock. CreateInstance (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333712"
---
# <a name="csystemclockcreateinstance-method"></a>Metodo CSystemClock. CreateInstance

Il `CreateInstance` metodo crea una nuova istanza di questo oggetto.

## <a name="syntax"></a>Sintassi


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** di aggregazione.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una nuova istanza di questo oggetto.

## <a name="remarks"></a>Commenti

Il class factory chiama questo metodo per creare l'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Sysclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 





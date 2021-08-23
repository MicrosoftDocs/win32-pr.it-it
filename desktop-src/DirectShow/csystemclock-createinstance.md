---
description: Il metodo CreateInstance crea una nuova istanza di questo oggetto.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Metodo CSystemClock.CreateInstance (Sysclock.h)
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
ms.openlocfilehash: 63626804ad4d067e5067170e0fc17cc83c179a906c0e625bb02a3ffb8a4ef197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687331"
---
# <a name="csystemclockcreateinstance-method"></a>Metodo CSystemClock.CreateInstance

Il `CreateInstance` metodo crea una nuova istanza di questo oggetto .

## <a name="syntax"></a>Sintassi


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Punk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown aggregata.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una nuova istanza di questo oggetto .

## <a name="remarks"></a>Commenti

L class factory chiama questo metodo per creare l'oggetto .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Sysclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 





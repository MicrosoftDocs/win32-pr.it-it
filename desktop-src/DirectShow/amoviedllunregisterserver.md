---
description: 'Funzione AMovieDllUnregisterServer : obsoleta. In alternativa, usare AMovieDllRegisterServer2.'
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Funzione AMovieDllUnregisterServer (Dllsetup.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099929"
---
# <a name="amoviedllunregisterserver-function"></a>Funzione AMovieDllUnregisterServer

Obsoleta. In [**alternativa, usare AMovieDllRegisterServer2.**](amoviedllregisterserver2.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dllsetup.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni di installazione dll**](dll-setup-functions.md)
</dt> </dl>

 

 





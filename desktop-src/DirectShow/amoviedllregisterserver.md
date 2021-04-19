---
description: Obsoleta. In alternativa, usare AMovieDllRegisterServer2.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Funzione AMovieDllRegisterServer (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330321"
---
# <a name="amoviedllregisterserver-function"></a>AMovieDllRegisterServer (funzione)

Obsoleta. In alternativa, usare [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dllsetup. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni di installazione DLL**](dll-setup-functions.md)
</dt> </dl>

 

 





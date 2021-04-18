---
description: La funzione AMovieDllRegisterServer2 registra e Annulla la registrazione dei filtri.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: Funzione AMovieDllRegisterServer2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331711"
---
# <a name="amoviedllregisterserver2-function"></a>AMovieDllRegisterServer2 (funzione)

La funzione **AMovieDllRegisterServer2** registra e Annulla la registrazione dei filtri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bRegister* 
</dt> <dd>

**True** indica che registra il filtro, **false** indica che è stata annullata la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Usare questa funzione per impostare i filtri. Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dllsetup. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni di installazione DLL**](dll-setup-functions.md)
</dt> </dl>

 

 





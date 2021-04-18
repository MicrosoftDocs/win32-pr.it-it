---
description: Il metodo Unregister rimuove il filtro dal registro di sistema.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Metodo CBaseFilter. Unregister (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b46e74e4009f6767788fa120984eca0e89fb551
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326939"
---
# <a name="cbasefilterunregister-method"></a>Metodo CBaseFilter. Unregister

Il `Unregister` metodo rimuove il filtro dal registro di sistema.

> [!Note]  
> Questo metodo è obsoleto. È necessario annullare la registrazione dei nuovi filtri tramite la funzione [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) . Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





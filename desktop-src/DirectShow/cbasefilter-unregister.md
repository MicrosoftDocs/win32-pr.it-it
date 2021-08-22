---
description: Il metodo Unregister rimuove il filtro dal Registro di sistema.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Metodo CBaseFilter.Unregister (Amfilter.h)
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
ms.openlocfilehash: c57d08c77c9c420cdc45b158a19fa610231f53f6b409d8b650953de0de8381a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317901"
---
# <a name="cbasefilterunregister-method"></a>Metodo CBaseFilter.Unregister

Il `Unregister` metodo rimuove il filtro dal Registro di sistema.

> [!Note]  
> Questo metodo è obsoleto. È necessario annullare la registrazione dei nuovi filtri usando la [**funzione AMovieDllRegisterServer2.**](amoviedllregisterserver2.md) Per altre informazioni, vedere [Come registrare DirectShow filtri](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





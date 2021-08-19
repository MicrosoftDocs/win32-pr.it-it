---
description: Il metodo Register aggiunge il filtro al Registro di sistema.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Metodo CBaseFilter.Register (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168d84d3bfc90fb710ae65a3b887eeb5575db407361a256c48161f0f7968a53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403524"
---
# <a name="cbasefilterregister-method"></a>Metodo CBaseFilter.Register

Il `Register` metodo aggiunge il filtro al Registro di sistema.

> [!Note]  
> Questo metodo è obsoleto. I nuovi filtri devono essere registrati usando la [**funzione AMovieDllRegisterServer2.**](amoviedllregisterserver2.md) Per altre informazioni, vedere [Come registrare DirectShow filtri](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT Register();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                  |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Non sono disponibili informazioni di registrazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





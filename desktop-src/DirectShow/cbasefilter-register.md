---
description: Il metodo Register aggiunge il filtro al registro di sistema.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Metodo CBaseFilter. Register (Amfilter. h)
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
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331660"
---
# <a name="cbasefilterregister-method"></a>Metodo CBaseFilter. Register

Il `Register` metodo aggiunge il filtro al registro di sistema.

> [!Note]  
> Questo metodo è obsoleto. I nuovi filtri devono essere registrati tramite la funzione [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) . Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT Register();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                  |
| <dl> <dt>**S \_ false**</dt> </dl> | Non sono disponibili informazioni sulla registrazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





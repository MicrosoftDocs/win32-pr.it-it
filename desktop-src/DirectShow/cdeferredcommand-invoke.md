---
description: Il metodo Invoke fornisce l'accesso ai metodi e alle proprietà esposti da un oggetto .
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Metodo CDeferredCommand.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1df087e71ba03ef67ea250235a4ef8a9ef5e6623efe67594381111de6088cf7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074375"
---
# <a name="cdeferredcommandinvoke-method"></a>Metodo CDeferredCommand.Invoke

Il `Invoke` metodo fornisce l'accesso ai metodi e alle proprietà esposti da un oggetto .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce VFW \_ E \_ ALREADY \_ CANCELLED se m **\_ pQueue** è **NULL.** In caso contrario, restituisce **il valore HRESULT** risultante da una chiamata a **IDispatch::GetTypeInfo** o **IUnknown::QueryInterface**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 





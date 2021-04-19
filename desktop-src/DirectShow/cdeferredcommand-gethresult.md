---
description: Il Metodo GetHRESULT Recupera il valore HRESULT dal comando richiamato.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Metodo CDeferredCommand. GetHRESULT (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333475"
---
# <a name="cdeferredcommandgethresult-method"></a>CDeferredCommand. GetHRESULT, metodo

Il `GetHResult` metodo recupera il valore **HRESULT** dal comando richiamato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phrResult* 
</dt> <dd>

Puntatore al valore **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ Interrompi se **m \_ pQueue** è **null**. In caso contrario, restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IDeferredCommand:: GetHRESULT**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 





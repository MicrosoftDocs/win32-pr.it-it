---
description: Richiama il metodo chiamato quando l'operazione asincrona specificata segnala lo stato di avanzamento.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: Metodo IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 141f79398e1f9f250b402df130daa728c8e2f0e5f78702d7866dbe9a202b5978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323120"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>Metodo IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke

Richiama il metodo chiamato quando l'operazione asincrona specificata segnala lo stato di avanzamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*asyncInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\***

Azione asincrona che segnala il completamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>           |
| Server minimo supportato<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 

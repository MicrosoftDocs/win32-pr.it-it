---
description: Richiama il metodo che viene chiamato quando l'operazione asincrona specificata segnala lo stato di avanzamento.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'IAsyncOperationWithProgressCompletedHandler<TResult, TProgress metodo>:: Invoke'
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
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129235"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>IAsyncOperationWithProgressCompletedHandler<TResult, TProgress metodo>:: Invoke

Richiama il metodo che viene chiamato quando l'operazione asincrona specificata segnala lo stato di avanzamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AsyncInfo* \[ in\]
</dt> <dd>

Tipo: **[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _

Azione asincrona che segnala il completamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>           |
| Server minimo supportato<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 

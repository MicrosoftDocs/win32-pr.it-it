---
title: Metodo IWMDRMEventGenerator CancelAsyncOperation (Wmdrmsdk.h)
description: Il metodo CancelAsyncOperation annulla un'operazione asincrona.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Metodo CancelAsyncOperation windows Media Format
- Metodo CancelAsyncOperation windows Media Format , interfaccia IWMDRMEventGenerator
- Interfaccia IWMDRMEventGenerator windows Media Format, metodo CancelAsyncOperation
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ca44fa141d21caeed1d0f16da65a1db61fe319e2b9424600275563e6c5d52f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847158"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>Metodo IWMDRMEventGenerator::CancelAsyncOperation

Il **metodo CancelAsyncOperation** annulla un'operazione asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cancelCancelationCookie* \[ Pollici\]
</dt> <dd>

Puntatore al cookie di annullamento che identifica l'operazione asincrona da annullare. Questo cookie viene fornito dal metodo utilizzato per avviare l'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 






---
title: Metodo IWMDRMEventGenerator CancelAsyncOperation (wmdrmsdk. h)
description: Il metodo CancelAsyncOperation Annulla un'operazione asincrona.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Metodo CancelAsyncOperation Windows Media Format
- Metodo CancelAsyncOperation Windows Media Format, interfaccia IWMDRMEventGenerator
- Interfaccia IWMDRMEventGenerator-formato Windows Media, metodo CancelAsyncOperation
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
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328535"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>Metodo IWMDRMEventGenerator:: CancelAsyncOperation

Il metodo **CancelAsyncOperation** Annulla un'operazione asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*punkCancelationCookie* \[ in\]
</dt> <dd>

Puntatore al cookie di annullamento che identifica l'operazione asincrona da annullare. Questo cookie viene fornito dal metodo utilizzato per avviare l'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 






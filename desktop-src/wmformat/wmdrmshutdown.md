---
title: Funzione WMDRMShutdown (wmdrmsdk. h)
description: La funzione WMDRMShutdown rilascia le risorse usate dalle API estese del client Windows Media DRM.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Formato Windows Media della funzione WMDRMShutdown
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324809"
---
# <a name="wmdrmshutdown-function"></a>WMDRMShutdown (funzione)

La funzione **WMDRMShutdown** rilascia le risorse usate dalle API estese del client Windows Media DRM.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Per evitare perdite di memoria, è necessario chiamare questa funzione per ogni chiamata della funzione [**WMDRMStartup**](wmdrmstartup.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni**](drm-functions.md)
</dt> </dl>

 

 






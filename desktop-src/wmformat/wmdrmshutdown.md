---
title: Funzione WMDRMShutdown (Wmdrmsdk.h)
description: La funzione WMDRMShutdown rilascia le risorse usate dalle API estese del client Windows Media DRM.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Formato windows Media della funzione WMDRMShutdown
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
ms.openlocfilehash: f80f0f7264cd0962cb642f0877ccd044e777c3e9f269f87fcffc0037dcc0836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930368"
---
# <a name="wmdrmshutdown-function"></a>Funzione WMDRMShutdown

La **funzione WMDRMShutdown** rilascia le risorse usate dalle API estese del client Windows Media DRM.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Per evitare perdite di memoria, è necessario chiamare questa funzione per ogni chiamata della [**funzione WMDRMStartup.**](wmdrmstartup.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni**](drm-functions.md)
</dt> </dl>

 

 






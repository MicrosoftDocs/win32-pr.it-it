---
title: Funzione WMDRMCreateProvider (wmdrmsdk. h)
description: La funzione WMDRMCreateProvider crea un class factory in grado di creare gli altri oggetti delle API estese del client Windows Media DRM.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Formato Windows Media della funzione WMDRMCreateProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325533"
---
# <a name="wmdrmcreateprovider-function"></a>WMDRMCreateProvider (funzione)

La funzione **WMDRMCreateProvider** crea un class factory in grado di creare gli altri oggetti delle API estese del client Windows Media DRM. Questa funzione non richiede una libreria stub di Microsoft e crea oggetti che non supportano le funzionalità DRM protette.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDRMProvider* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IWMDRMProvider**](iwmdrmprovider.md) dell'oggetto appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 






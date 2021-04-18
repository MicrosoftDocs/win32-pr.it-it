---
title: Funzione WMDRMCreateProtectedProvider (wmdrmsdk. h)
description: La funzione WMDRMCreateProtectedProvider crea un class factory in grado di creare gli altri oggetti delle API estese del client Windows Media DRM.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Formato Windows Media della funzione WMDRMCreateProtectedProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324816"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>WMDRMCreateProtectedProvider (funzione)

La funzione **WMDRMCreateProtectedProvider** crea un class factory in grado di creare gli altri oggetti delle API estese del client Windows Media DRM. Questa funzione richiede una libreria stub di Microsoft e crea oggetti che supportano le funzionalità DRM protette.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
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



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProvider**](wmdrmcreateprovider.md)
</dt> </dl>

 

 






---
title: Metodo GetURL IWMDRMNonSilentLicenseAquisition (Wmdrmsdk.h)
description: Il metodo GetURL recupera l'URL in cui deve essere pubblicata la richiesta di licenza.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Metodo GetURL windows Media Format
- Metodo GetURL windows Media Format , interfaccia IWMDRMNonSilentLicenseAquisition
- IWMDRMNonSilentLicenseAquisition interface windows Media Format , Metodo GetURL
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7979d82363b21b58563a606c31a99d069a60a3bc5b2da162a7339513c2867bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084708"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>Metodo IWMDRMNonSilentLicenseAquisition::GetURL

Il **metodo GetURL** recupera l'URL in cui deve essere pubblicata la richiesta di licenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrURL* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve l'URL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

[**Interfaccia IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 






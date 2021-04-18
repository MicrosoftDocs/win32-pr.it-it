---
title: Metodo IWMDRMNonSilentLicenseAquisition GetURL (wmdrmsdk. h)
description: Il metodo GetURL recupera l'URL a cui deve essere inviata la richiesta di licenza.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Metodo GetURL Windows Media Format
- Metodo GetURL Windows Media Format, interfaccia IWMDRMNonSilentLicenseAquisition
- Interfaccia IWMDRMNonSilentLicenseAquisition-formato Windows Media, Metodo GetURL
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
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325547"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>Metodo IWMDRMNonSilentLicenseAquisition:: GetURL

Il metodo **getURL** recupera l'URL a cui deve essere inviata la richiesta di licenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrURL* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve l'URL.

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

[**Interfaccia IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 






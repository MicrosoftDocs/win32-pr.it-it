---
title: Metodo IWMDRMNonSilentLicenseAquisition GetChallenge (Wmdrmsdk.h)
description: Il metodo GetChallenge recupera la richiesta di licenza che deve essere pubblicata nel server licenze.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Metodo GetChallenge per Windows Media Format
- Metodo GetChallenge windows Media Format, interfaccia IWMDRMNonSilentLicenseAquisition
- Interfaccia IWMDRMNonSilentLicenseAquisition windows Media Format , metodo GetChallenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf495652033bdb5201f2b4e5bd9dc1d6a222cc3ebdf4ec6438fe391ed06fac85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027519"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>Metodo IWMDRMNonSilentLicenseAquisition::GetChallenge

Il **metodo GetChallenge** recupera la richiesta di licenza da pubblicare nel server licenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrChallenge* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve la richiesta di licenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

 

 






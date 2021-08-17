---
title: Metodo IWMDRMLicense GetLicenseProperty (Wmdrmsdk.h)
description: Il metodo GetLicenseProperty recupera una proprietà dalla licenza corrente.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Metodo GetLicenseProperty windows Media Format
- Metodo GetLicenseProperty windows Media Format , interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense windows Media Format , metodo GetLicenseProperty
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167fc0aa050765700805b4339e68142fa5d1eb7fc99e010c7393095dd9aa5c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084841"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>Metodo IWMDRMLicense::GetLicenseProperty

Il **metodo GetLicenseProperty** recupera una proprietà dalla licenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Nome della proprietà da recuperare. Impostare su una delle costanti nella tabella seguente:



| Costante                   | Descrizione                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRMNet \_ Revocation | Usare per ottenere l'Windows di revoca di Media DRM per i dispositivi di rete per la licenza corrente.                        |
| g \_ wszWMDRM \_ SAPLEVEL      | Usare per ottenere il livello DIS (Secure Audio Path) necessario per riprodurre il contenuto coperto dalla licenza corrente.                |
| g \_ wszWMDRM \_ SAPRequired   | Usare per verificare se la licenza corrente richiede l'uso di SAP per riprodurre il contenuto.                               |
| g \_ wszWMDRM \_ SOURCEID      | Usare per ottenere l'identificatore di origine per la licenza corrente.                                                            |
| g \_ wszWMDRM \_ PRIORITY      | Usare per ottenere la priorità della licenza corrente. Le licenze con priorità più alta vengono applicate prima delle licenze con priorità inferiore. |
| g \_ wszWMDRM \_ UplinkID      | Usare per ottenere l'ID chiave della licenza radice nella catena di licenze a cui appartiene la licenza corrente.                  |



 

</dd> <dt>

*ppropVariant* \[ Cambio\]
</dt> <dd>

Riceve il valore della proprietà.

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

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 






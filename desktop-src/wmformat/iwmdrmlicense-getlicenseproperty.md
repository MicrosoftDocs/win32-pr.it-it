---
title: Metodo IWMDRMLicense GetLicenseProperty (wmdrmsdk. h)
description: Il metodo GetLicenseProperty recupera una proprietà dalla licenza corrente.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Metodo GetLicenseProperty Windows Media Format
- Metodo GetLicenseProperty Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetLicenseProperty
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
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325567"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>Metodo IWMDRMLicense:: GetLicenseProperty

Il metodo **GetLicenseProperty** recupera una proprietà dalla licenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* \[ in\]
</dt> <dd>

Nome della proprietà da recuperare. Impostare su una delle costanti nella tabella seguente:



| Costante                   | Descrizione                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| \_revoca g wszWMDRMNet \_ | Utilizzare per ottenere Windows Media DRM per i dispositivi di rete elenco di revoche per la licenza corrente.                        |
| g \_ wszWMDRM \_ SAPLEVEL      | Usare per ottenere il livello SAP (Secure Audio Path) necessario per riprodurre il contenuto coperto dalla licenza corrente.                |
| g \_ wszWMDRM \_ SAPRequired   | Usare per verificare se la licenza corrente richiede l'uso di SAP per riprodurre il contenuto.                               |
| g \_ wszWMDRM \_ SOURCEID      | Utilizzare per ottenere l'identificatore di origine per la licenza corrente.                                                            |
| g \_ \_ priorità wszWMDRM      | Usare per ottenere la priorità della licenza corrente. Le licenze con priorità più alta vengono applicate prima delle licenze con priorità più bassa. |
| g \_ wszWMDRM- \_ LinkId      | Usare per ottenere l'ID chiave della licenza radice nella catena di licenze a cui appartiene la licenza corrente.                  |



 

</dd> <dt>

*ppropVariant* \[ out\]
</dt> <dd>

Riceve il valore della proprietà.

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

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 






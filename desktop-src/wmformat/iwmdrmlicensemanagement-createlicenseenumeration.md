---
title: Metodo IWMDRMLicenseManagement CreateLicenseEnumeration (Wmdrmsdk.h)
description: Il metodo CreateLicenseEnumeration crea un oggetto enumeratore licenze con cui è possibile ottenere informazioni sulle licenze nell'archivio licenze locale.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Metodo CreateLicenseEnumeration windows Media Format
- Metodo CreateLicenseEnumeration windows Media Format , interfaccia IWMDRMLicenseManagement
- Metodo CreateLicenseEnumeration dell'interfaccia IWMDRMLicenseManagement windows Media Format
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e442870961735d09c786a21ed1ea8be765e8f0c59b3f760278be9316daa0bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881081"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>Metodo IWMDRMLicenseManagement::CreateLicenseEnumeration

Il **metodo CreateLicenseEnumeration** crea un oggetto enumeratore licenze con cui è possibile ottenere informazioni sulle licenze nell'archivio licenze locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLicenseFilter* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura WMDRM \_ LICENSE \_ FILTER**](wmdrm-license-filter.md) contenente i parametri di filtro per l'elenco di licenze nell'enumeratore.

</dd> <dt>

*pEnumerator* \[ Cambio\]
</dt> <dd>

Puntatore che riceve l'indirizzo [**dell'interfaccia IWMDRMLicense**](iwmdrmlicense.md) dell'oggetto enumeratore di licenza appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM RIV TROPPO \_ \_ \_ PICCOLO**</dt> </dl> | È necessario un elenco di revoche di contenuto aggiornato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Enumerazione delle licenze nell'archivio licenze locale**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






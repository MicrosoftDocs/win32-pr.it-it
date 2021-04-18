---
title: Metodo IWMDRMLicenseManagement CreateLicenseEnumeration (wmdrmsdk. h)
description: Il metodo CreateLicenseEnumeration crea un oggetto enumeratore di licenze con il quale è possibile ottenere informazioni sulle licenze nell'archivio licenze locale.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Metodo CreateLicenseEnumeration Windows Media Format
- Metodo CreateLicenseEnumeration Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo CreateLicenseEnumeration
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
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325107"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>Metodo IWMDRMLicenseManagement:: CreateLicenseEnumeration

Il metodo **CreateLicenseEnumeration** crea un oggetto enumeratore di licenze con il quale è possibile ottenere informazioni sulle licenze nell'archivio licenze locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLicenseFilter* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ \_ filtro delle licenze WMDRM**](wmdrm-license-filter.md) contenente i parametri di filtro per l'elenco di licenze nell'enumeratore.

</dd> <dt>

*pEnumerator* \[ out\]
</dt> <dd>

Puntatore che riceve l'indirizzo dell'interfaccia [**IWMDRMLicense**](iwmdrmlicense.md) dell'oggetto enumeratore licenze appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt> </dl> | È necessario un elenco di revoche di contenuti aggiornato.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Enumerazione delle licenze nell'archivio licenze locale**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






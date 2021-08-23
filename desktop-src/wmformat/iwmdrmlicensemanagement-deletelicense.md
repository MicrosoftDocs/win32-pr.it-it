---
title: Metodo IWMDRMLicenseManagement DeleteLicense (Wmdrmsdk.h)
description: Il metodo DeleteLicense rimuove una licenza dall'archivio licenze locale temporaneo.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Metodo DeleteLicense windows Media Format
- Metodo DeleteLicense windows Media Format , interfaccia IWMDRMLicenseManagement
- IWMDRMLicenseManagement interface windows Media Format , DeleteLicense method
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977f7eaef1d6c8a505ce55d7d1683d7c9f4dabff5e59df7d8845773eefdff696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707941"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>Metodo IWMDRMLicenseManagement::D eleteLicense

Il **metodo DeleteLicense** rimuove una licenza dall'archivio licenze locale temporaneo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrKID* \[ Pollici\]
</dt> <dd>

ID chiave (KID) della licenza da eliminare.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag di opzione di eliminazione della licenza. Impostare su uno dei valori nella tabella seguente.



| Valore                                    | Descrizione                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ DELETE \_ LICENSE \_ IMMEDIATELY      | Specifica che la licenza deve essere rimossa immediatamente dall'archivio.                                                                                                                              |
| WMDRM \_ DELETE \_ LICENSE \_ MARK \_ FOR \_ PURGE | Specifica che la licenza deve essere contrassegnata per l'eliminazione, ma non deve essere rimossa dall'archivio fino a quando non viene chiamato il metodo [**CleanLicenseStore.**](iwmdrmlicensemanagement-cleanlicensestore.md) |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Il metodo è riuscito.<br/>                                                                                    |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | La licenza specificata non esiste nell'archivio.<br/> oppure<br/> L'archivio non è stato trovato.<br/> |



 

## <a name="remarks"></a>Commenti

Per eliminare le licenze dall'archivio licenze locale permanente, è necessario usare la revoca delle licenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






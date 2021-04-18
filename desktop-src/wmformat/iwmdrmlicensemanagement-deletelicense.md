---
title: Metodo IWMDRMLicenseManagement DeleteLicense (wmdrmsdk. h)
description: Il metodo DeleteLicense rimuove una licenza dall'archivio licenze locale temporaneo.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Metodo DeleteLicense Windows Media Format
- Metodo DeleteLicense Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo DeleteLicense
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
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329280"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>IWMDRMLicenseManagement::D Metodo eleteLicense

Il metodo **DeleteLicense** rimuove una licenza dall'archivio licenze locale temporaneo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrKID* \[ in\]
</dt> <dd>

ID chiave (KID) della licenza da eliminare.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag dell'opzione di eliminazione delle licenze. Impostare su uno dei valori riportati nella tabella seguente.



| Valore                                    | Descrizione                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ eliminare \_ immediatamente la licenza \_      | Specifica che la licenza deve essere rimossa immediatamente dall'archivio.                                                                                                                              |
| WMDRM \_ eliminare \_ il \_ contrassegno \_ di licenza per l' \_ eliminazione | Specifica che la licenza deve essere contrassegnata per l'eliminazione, ma non deve essere rimossa dall'archivio fino a quando non viene chiamato il metodo [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) . |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Il metodo è riuscito.<br/>                                                                                    |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | La licenza specificata non esiste nell'archivio.<br/> oppure<br/> L'archivio non è stato trovato.<br/> |



 

## <a name="remarks"></a>Commenti

Per eliminare le licenze dall'archivio licenze locale permanente, è necessario utilizzare la revoca delle licenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






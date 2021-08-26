---
title: Metodo IWMDRMLicenseManagement ProcessLicenseRevocationResponse (Wmdrmsdk.h)
description: Il metodo ProcessLicenseRevocationResponse revoca le licenze dall'archivio licenze locale. Questo metodo usa un BLOB di revoca delle licenze ricevuto da un server di revoca delle licenze per identificare le licenze da revocare.
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- Metodo ProcessLicenseRevocationResponse windows Media Format
- Metodo ProcessLicenseRevocationResponse in formato Windows Media, interfaccia IWMDRMLicenseManagement
- Metodo ProcessLicenseRevocationResponse dell'interfaccia IWMDRMLicenseManagement windows Media Format
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseRevocationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d58c33f79db575dec37d7d2ac51e3c65b10416b9ca35a50084f36a56693854be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930311"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>Metodo IWMDRMLicenseManagement::P rocessLicenseRevocationResponse

Il **metodo ProcessLicenseRevocationResponse** revoca le licenze dall'archivio licenze locale. Questo metodo usa un BLOB di revoca delle licenze ricevuto da un server di revoca delle licenze per identificare le licenze da revocare.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessLicenseRevocationResponse(
  [in]  BYTE  *pbSignedLRB,
  [in]  DWORD cbSignedLRB,
  [out] BYTE  **ppbSignedACK,
  [out] DWORD *pcbSignedACK
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbSignedLRB* \[ Pollici\]
</dt> <dd>

BLOB di revoca delle licenze ricevuto dal server di revoca delle licenze in risposta a una richiesta di verifica generata chiamando il [**metodo CreateLicenseRevocationChallenge.**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md)

</dd> <dt>

*cbSignedLRB* \[ Pollici\]
</dt> <dd>

Dimensioni dell'LRB in byte.

</dd> <dt>

*ppbSignedACK* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'indirizzo dell'acknowledgement di revoca della licenza. L'acknowledgement deve essere inviato al servizio di revoca delle licenze. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree.**

</dd> <dt>

*pcbSignedACK* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni dell'acknowledgement in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






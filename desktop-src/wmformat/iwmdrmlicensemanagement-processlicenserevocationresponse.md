---
title: Metodo IWMDRMLicenseManagement ProcessLicenseRevocationResponse (wmdrmsdk. h)
description: Il metodo ProcessLicenseRevocationResponse revoca le licenze dall'archivio licenze locale. Questo metodo utilizza un BLOB di revoca delle licenze (LRB) ricevuto da un server di revoca delle licenze per identificare le licenze da revocare.
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- Metodo ProcessLicenseRevocationResponse Windows Media Format
- Metodo ProcessLicenseRevocationResponse Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo ProcessLicenseRevocationResponse
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
ms.openlocfilehash: 534ead406107957971bbf1501dff2850478fae08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329271"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>IWMDRMLicenseManagement::P metodo rocessLicenseRevocationResponse

Il metodo **ProcessLicenseRevocationResponse** revoca le licenze dall'archivio licenze locale. Questo metodo utilizza un BLOB di revoca delle licenze (LRB) ricevuto da un server di revoca delle licenze per identificare le licenze da revocare.

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

*pbSignedLRB* \[ in\]
</dt> <dd>

BLOB di revoca delle licenze (LRB) ricevuto dal server di revoca delle licenze in risposta a una richiesta di verifica generata chiamando il metodo [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .

</dd> <dt>

*cbSignedLRB* \[ in\]
</dt> <dd>

Dimensioni del LRB in byte.

</dd> <dt>

*ppbSignedACK* \[ out\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'indirizzo della conferma della revoca delle licenze. Il riconoscimento deve essere inviato al servizio di revoca delle licenze. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.

</dd> <dt>

*pcbSignedACK* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni in byte del riconoscimento.

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
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






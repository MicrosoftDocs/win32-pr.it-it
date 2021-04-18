---
title: Metodo IWMDRMLicenseManagement CreateLicenseRevocationChallenge (wmdrmsdk. h)
description: Il metodo CreateLicenseRevocationChallenge genera una richiesta di revoca delle licenze.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Metodo CreateLicenseRevocationChallenge Windows Media Format
- Metodo CreateLicenseRevocationChallenge Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo CreateLicenseRevocationChallenge
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328189"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>Metodo IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge

Il metodo **CreateLicenseRevocationChallenge** genera una richiesta di revoca delle licenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbMachineID* \[ in\]
</dt> <dd>

Identificatore computer specificato dall'utente. Questo valore viene utilizzato per eseguire una query per una licenza nel server e deve essere conforme a qualsiasi formato utilizzato dal server licenze.

</dd> <dt>

*cbMachineID* \[ in\]
</dt> <dd>

Dimensione, in byte, dell'identificatore del computer.

</dd> <dt>

*pbChallenge* \[ in\]
</dt> <dd>

Dati di richiesta specificati dall'utente. Questi dati, oltre all'identificatore del computer, vengono utilizzati per eseguire una query sul server licenze per la revoca delle licenze.

</dd> <dt>

*cbChallenge* \[ in\]
</dt> <dd>

Dimensioni, in byte, dei dati della richiesta di verifica.

</dd> <dt>

*ppbChallengeOutput* \[ out\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'indirizzo dell'output della richiesta di verifica. Questo buffer corrisponde ai dati inviati al servizio di revoca delle licenze. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.

</dd> <dt>

*pcbChallengeOutput* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve la dimensione dei dati di output della richiesta di verifica allocata, in byte.

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

 

 






---
title: Metodo IWMDRMLicenseManagement CreateLicenseRevocationChallenge (Wmdrmsdk.h)
description: Il metodo CreateLicenseRevocationChallenge genera una richiesta di revoca della licenza.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Metodo CreateLicenseRevocationChallenge windows Media Format
- Metodo CreateLicenseRevocationChallenge windows Media Format , interfaccia IWMDRMLicenseManagement
- Metodo CreateLicenseRevocationChallenge dell'interfaccia IWMDRMLicenseManagement windows Media Format, CreateLicenseRevocationChallenge
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
ms.openlocfilehash: 851233229d7dde113cf21cfb38419067679843b34ae59ece0e32e326c2a91c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846955"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>Metodo IWMDRMLicenseManagement::CreateLicenseRevocationChallenge

Il **metodo CreateLicenseRevocationChallenge** genera una richiesta di revoca della licenza.

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

*pbMachineID* \[ Pollici\]
</dt> <dd>

Identificatore del computer specificato dall'utente. Questo valore viene usato per eseguire query su una licenza nel server e deve essere conforme al formato usato dal server licenze.

</dd> <dt>

*cbMachineID* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, dell'identificatore del computer.

</dd> <dt>

*pbChallenge* \[ Pollici\]
</dt> <dd>

Dati di richiesta specificati dall'utente. Questi dati, oltre all'identificatore del computer, vengono usati per eseguire query sul server licenze per ottenere le licenze da revocare.

</dd> <dt>

*cbChallenge* \[ Pollici\]
</dt> <dd>

Dimensioni, in byte, dei dati di richiesta.

</dd> <dt>

*ppbChallengeOutput* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'indirizzo dell'output di richiesta. Questo buffer è i dati inviati al servizio di revoca delle licenze. Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.

</dd> <dt>

*pcbChallengeOutput* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve le dimensioni in byte dei dati di output della richiesta di richiesta allocati.

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
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






---
title: Metodo IWMDRMDecrypt Decrypt (Wmdrmsdk.h)
description: Il metodo Decrypt decrittografa un buffer di dati sul posto.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Metodo di decrittografia windows Media Format
- Metodo decrypt windows Media Format , interfaccia IWMDRMDecrypt
- Interfaccia IWMDRMDecrypt windows Media Format , metodo Decrypt
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be82ec976da39103698b93a09b3d5235c8c8ee712783ca8284dc7b18c6a8a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027748"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>Metodo IWMDRMDecrypt::D ecrypt

Il **metodo Decrypt** decrittografa un buffer di dati sul posto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbData* \[ in, out\]
</dt> <dd>

Dati da decrittografare. Se il metodo ha esito positivo, questi dati vengono decrittografati al ritorno.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Dimensioni dei dati in byte.

</dd> <dt>

*pWMCryptoData* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura WMDRMCryptoData**](wmdrmcryptodata.md) contenente parametri aggiuntivi. Può essere **NULL** se il contenuto è stato crittografato usando i parametri predefiniti.

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

[**Interfaccia IWMDRMDecrypt**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 






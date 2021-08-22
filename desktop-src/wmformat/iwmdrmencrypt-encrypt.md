---
title: Metodo IWMDRMEncrypt Encrypt (Wmdrmsdk.h)
description: Il metodo Encrypt crittografa un buffer di dati sul posto.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Metodo Encrypt per Windows Media Format
- Metodo Encrypt in formato Windows Media, interfaccia IWMDRMEncrypt
- Interfaccia IWMDRMEncrypt in formato windows Media, metodo Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb49b2857c23bb11b5e4d091dece820bb833b2b4e77224558f2d7972885445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027739"
---
# <a name="iwmdrmencryptencrypt-method"></a>Metodo IWMDRMEncrypt::Encrypt

Il **metodo Encrypt** crittografa un buffer di dati sul posto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbData* \[ in, out\]
</dt> <dd>

Dati da crittografare. Se il metodo ha esito positivo, i dati vengono crittografati al ritorno.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Dimensioni dei dati in byte.

</dd> <dt>

*pWMCryptoData* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura WMDRMCryptoData**](wmdrmcryptodata.md) contenente parametri aggiuntivi. Impostare su **NULL per** usare i valori di crittografia predefiniti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

[**Interfaccia IWMDRMEncrypt**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 






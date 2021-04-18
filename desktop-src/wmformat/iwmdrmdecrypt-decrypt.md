---
title: Metodo Decrypt IWMDRMDecrypt (wmdrmsdk. h)
description: Il metodo Decrypt decrittografa un buffer di dati sul posto.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Metodo Decrypt Windows Media Format
- Metodo di decrittografia Windows Media Format, interfaccia IWMDRMDecrypt
- Interfaccia IWMDRMDecrypt-formato Windows Media, metodo Decrypt
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
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324294"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>IWMDRMDecrypt::D Metodo ecrypt

Il metodo **Decrypt** decrittografa un buffer di dati sul posto.

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

*pbData* \[ in uscita\]
</dt> <dd>

Dati da decrittografare. Se il metodo ha esito positivo, questi dati vengono decrittografati al ritorno.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Dimensioni dei dati in byte.

</dd> <dt>

*pWMCryptoData* \[ in\]
</dt> <dd>

Puntatore a una struttura [**WMDRMCryptoData**](wmdrmcryptodata.md) che contiene parametri aggiuntivi. Può essere **null** se il contenuto è stato crittografato usando i parametri predefiniti.

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

[**Interfaccia IWMDRMDecrypt**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 






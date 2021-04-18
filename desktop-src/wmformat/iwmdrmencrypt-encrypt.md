---
title: Metodo Encrypt IWMDRMEncrypt (wmdrmsdk. h)
description: Il metodo Encrypt crittografa un buffer di dati sul posto.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Metodo Encrypt formato Windows Media
- Metodo Encrypt formato Windows Media, interfaccia IWMDRMEncrypt
- Interfaccia IWMDRMEncrypt-formato Windows Media, metodo Encrypt
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
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324287"
---
# <a name="iwmdrmencryptencrypt-method"></a>Metodo IWMDRMEncrypt:: Encrypt

Il metodo **Encrypt** crittografa un buffer di dati sul posto.

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

*pbData* \[ in uscita\]
</dt> <dd>

Dati da crittografare. Se il metodo ha esito positivo, i dati vengono crittografati al ritorno.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Dimensioni dei dati in byte.

</dd> <dt>

*pWMCryptoData* \[ in\]
</dt> <dd>

Puntatore a una struttura [**WMDRMCryptoData**](wmdrmcryptodata.md) che contiene parametri aggiuntivi. Impostare su **null** per usare i valori di crittografia predefiniti.

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

[**Interfaccia IWMDRMEncrypt**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 






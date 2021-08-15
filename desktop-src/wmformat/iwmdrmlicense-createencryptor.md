---
title: Metodo IWMDRMLicense CreateEncryptor (Wmdrmsdk.h)
description: Il metodo CreateEncryptor crea un oggetto encryptor usando le impostazioni della licenza corrente.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Metodo CreateEncryptor windows Media Format
- Metodo CreateEncryptor windows Media Format , interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense windows Media Format , metodo CreateEncryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481e33b6a3d4ffff3805ccc14f45b06a12ad2296fdaaedf13608f3a519c6ed10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433660"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>Metodo IWMDRMLicense::CreateEncryptor

Il **metodo CreateEncryptor** crea un oggetto encryptor usando le impostazioni della licenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEncryptor* \[ Cambio\]
</dt> <dd>

Riceve un puntatore [**all'interfaccia IWMDRMEncrypt**](iwmdrmencrypt.md) dell'oggetto appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ TOO \_ SMALL**</dt> </dl> | È necessario un elenco di revoche di contenuto aggiornato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 






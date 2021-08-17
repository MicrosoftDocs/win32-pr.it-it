---
title: Metodo IWMDRMLicense CreateDecryptor (Wmdrmsdk.h)
description: Il metodo CreateDecryptor crea un oggetto decryptor usando le impostazioni della licenza corrente.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Metodo CreateDecryptor windows Media Format
- Metodo CreateDecryptor windows Media Format , interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense windows Media Format , metodo CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ac7e6bb1e9d4f9e5e7c706c0a9e3518f62b1068ed743dc795554dd43ac61e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027709"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>Metodo IWMDRMLicense::CreateDecryptor

Il **metodo CreateDecryptor** crea un oggetto decryptor usando le impostazioni della licenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDecryptor* \[ Cambio\]
</dt> <dd>

Riceve un puntatore [**all'interfaccia IWMDRMDecrypt**](iwmdrmdecrypt.md) dell'oggetto appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM RIV TROPPO \_ \_ \_ PICCOLO**</dt> </dl> | È necessario un elenco di revoche di contenuto aggiornato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Createencryptor**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 






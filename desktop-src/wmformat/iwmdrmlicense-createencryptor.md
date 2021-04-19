---
title: Metodo IWMDRMLicense al CreateDecryptor (wmdrmsdk. h)
description: Il metodo al CreateDecryptor crea un oggetto di crittografia utilizzando le impostazioni della licenza corrente.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Metodo al CreateDecryptor Windows Media Format
- Metodo al CreateDecryptor Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo al CreateDecryptor
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
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328531"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>Metodo IWMDRMLicense:: al CreateDecryptor

Il metodo **al CreateDecryptor** crea un oggetto di crittografia utilizzando le impostazioni della licenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEncryptor* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IWMDRMEncrypt**](iwmdrmencrypt.md) dell'oggetto appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt> </dl> | È necessario un elenco di revoche di contenuti aggiornato.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 






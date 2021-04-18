---
title: Metodo IWMDRMLicense CreateDecryptor (wmdrmsdk. h)
description: Il metodo CreateDecryptor crea un oggetto di decrittografia utilizzando le impostazioni della licenza corrente.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Metodo CreateDecryptor Windows Media Format
- Metodo CreateDecryptor Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo CreateDecryptor
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
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324285"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>Metodo IWMDRMLicense:: CreateDecryptor

Il metodo **CreateDecryptor** crea un oggetto di decrittografia utilizzando le impostazioni della licenza corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDecryptor* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IWMDRMDecrypt**](iwmdrmdecrypt.md) dell'oggetto appena creato.

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

[**Al CreateDecryptor**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 






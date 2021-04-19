---
title: Metodo Encrypt IWMSecureBuffer (wmdrmsdk. h)
description: Il metodo Encrypt crittografa un puntatore di dati.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Metodo Encrypt formato Windows Media
- Metodo Encrypt formato Windows Media, interfaccia IWMSecureBuffer
- Interfaccia IWMSecureBuffer-formato Windows Media, metodo Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333621"
---
# <a name="iwmsecurebufferencrypt-method"></a>Metodo IWMSecureBuffer:: Encrypt

Il metodo **Encrypt** crittografa un puntatore di dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSecureChannel* \[ in\]
</dt> <dd>

Puntatore a un'interfaccia di canale sicura che contiene il puntatore ai dati da crittografare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per crittografare i puntatori dati in modo che possano essere inviati attraverso i limiti DLL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Decrypt**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**Interfaccia IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 






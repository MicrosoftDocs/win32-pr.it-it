---
title: Metodo Decrypt IWMSecureBuffer (wmdrmsdk. h)
description: Il metodo Decrypt decrittografa un puntatore a dati crittografato chiamando il metodo Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Metodo Decrypt Windows Media Format
- Metodo di decrittografia Windows Media Format, interfaccia IWMSecureBuffer
- Interfaccia IWMSecureBuffer-formato Windows Media, metodo Decrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333623"
---
# <a name="iwmsecurebufferdecrypt-method"></a>IWMSecureBuffer::D Metodo ecrypt

Il metodo **Decrypt** decrittografa un puntatore a dati crittografato chiamando il metodo [**Encrypt**](iwmsecurebuffer-encrypt.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSecureChannel* \[ in\]
</dt> <dd>

Puntatore a un'interfaccia di canale sicura che contiene il puntatore ai dati crittografati.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Crittografare**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**Interfaccia IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 






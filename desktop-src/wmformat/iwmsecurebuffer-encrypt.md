---
title: Metodo IWMSecureBuffer Encrypt (Wmdrmsdk.h)
description: Il metodo Encrypt crittografa un puntatore ai dati.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Crittografare il metodo windows Media Format
- Metodo Encrypt windows Media Format , interfaccia IWMSecureBuffer
- Interfaccia IWMSecureBuffer windows Media Format , metodo Encrypt
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
ms.openlocfilehash: c8e5badce8249e5d6b9d2460fec0e72ef4ca4b81f5b8ffa0d3edd83729f98bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808311"
---
# <a name="iwmsecurebufferencrypt-method"></a>Metodo IWMSecureBuffer::Encrypt

Il **metodo Encrypt** crittografa un puntatore ai dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSecureChannel* \[ Pollici\]
</dt> <dd>

Puntatore a un'interfaccia del canale sicuro contenente il puntatore ai dati da crittografare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Usare questo metodo per crittografare i puntatori ai dati in modo che possano essere inviati attraverso i limiti della DLL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Decrittografare**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**Interfaccia IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 






---
title: Metodo IWMSecureBuffer Decrypt (Wmdrmsdk.h)
description: Il metodo Decrypt decrittografa un puntatore ai dati crittografato chiamando il metodo Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Decrittografare il metodo windows Media Format
- Decrittografare il metodo windows Media Format , interfaccia IWMSecureBuffer
- Interfaccia IWMSecureBuffer windows Media Format , metodo Decrypt
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
ms.openlocfilehash: bb9867cb6476ab0a2838903c906f662032e14dfb0d4fa0547b045672e03b6ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930101"
---
# <a name="iwmsecurebufferdecrypt-method"></a>Metodo IWMSecureBuffer::D ecrypt

Il **metodo Decrypt** decrittografa un puntatore ai dati crittografato chiamando il metodo [**Encrypt.**](iwmsecurebuffer-encrypt.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSecureChannel* \[ Pollici\]
</dt> <dd>

Puntatore a un'interfaccia di canale protetta contenente il puntatore ai dati crittografati.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Crittografare**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**Interfaccia IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 






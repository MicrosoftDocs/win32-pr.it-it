---
description: Il \_ metodo Get AddressType ottiene il tipo di indirizzo.
ms.assetid: b2ff6303-6beb-429c-ad1a-2f729749e5db
title: 'Metodo ITConnection:: get_AddressType (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d015b0b395f0219fa9a7af2ca7002f242cfaa1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328225"
---
# <a name="itconnectionget_addresstype-method"></a>Metodo ITConnection:: Get \_ AddressType

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ addressType** ottiene il tipo di indirizzo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AddressType(
  [out] BSTR *ppAddressType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAddressType* \[ out\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il tipo di indirizzo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppAddressType* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                   |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppAddressType* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> <dt>

[**ITConnection::p UT \_ AddressType**](itconnection-put-addresstype.md)
</dt> </dl>

 


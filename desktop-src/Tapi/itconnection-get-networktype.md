---
description: Il \_ metodo Get NetworkType ottiene il tipo di rete.
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: 'Metodo ITConnection:: get_NetworkType (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31189ec0e3b42e3ed249cd0c62365b1f8c793908
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326511"
---
# <a name="itconnectionget_networktype-method"></a>Metodo ITConnection:: Get \_ NetworkType

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ NetworkType** ottiene il tipo di rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppNetworkType* \[ out\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il tipo di rete.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppNetworkType* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                   |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppNetworkType* .

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

[**ITConnection::p UT \_ NetworkType**](itconnection-put-networktype.md)
</dt> </dl>

 


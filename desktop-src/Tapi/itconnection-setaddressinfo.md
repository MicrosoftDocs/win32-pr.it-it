---
description: Il metodo SetAddressInfo imposta le informazioni sull'indirizzo.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: Metodo ITConnection::SetAddressInfo (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d90fd6e92e115966df709626b7b58c739d292fedca4fb855999bc3fd8cd853b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774931"
---
# <a name="itconnectionsetaddressinfo-method"></a>Metodo ITConnection::SetAddressInfo

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo SetAddressInfo** imposta le informazioni sull'indirizzo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStartAddress* \[ Pollici\]
</dt> <dd>

Puntatore a un **BSTR** contenente l'indirizzo iniziale.

</dd> <dt>

*NumAddresses* \[ Pollici\]
</dt> <dd>

Numero di indirizzi da utilizzare per la sessione.

</dd> <dt>

*Ttl* \[ Pollici\]
</dt> <dd>

[*Ambito TTL (Time to Live)*](t-tapgloss.md) per le trasmissioni sugli indirizzi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pStartAddress,* *NumAddresses* o *Ttl* non è valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>                  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                                   |



 

## <a name="remarks"></a>Commenti

L'applicazione deve [**usare SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il *parametro pStartAddress* e [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Connessione IT**](itconnection.md)
</dt> </dl>

 


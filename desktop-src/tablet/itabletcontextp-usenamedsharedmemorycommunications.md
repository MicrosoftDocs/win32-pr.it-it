---
description: Imposta la comunicazione di memoria condivisa per il contesto del tablet.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: Metodo ITabletContextP::UseNamedSharedMemoryCommunications
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: a8ce5d4dde7f3fd678e4ac748a0f148750344a1e5e8da9f6481ad25eafa016a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712231"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a>Metodo ITabletContextP::UseNamedSharedMemoryCommunications

Imposta la comunicazione di memoria condivisa per il contesto del tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pid* \[ Pollici\]
</dt> <dd>

ID del processo del client che accede alla memoria condivisa.

</dd> <dt>

*pszCallerSid* \[ Pollici\]
</dt> <dd>

Identificatore di sicurezza del chiamante della funzione.

</dd> <dt>

*pszCallerIntegritySid* \[ Pollici\]
</dt> <dd>

Identificatore di sicurezza in grado di verificare l'integrità della funzione chiamante.

</dd> <dt>

*pdwEventMoreDataId* \[ Cambio\]
</dt> <dd>

Intero utilizzato per costruire il nome di un evento. L'evento indica se sono presenti più dati.

</dd> <dt>

*pdwEventClientReadyId* \[ Cambio\]
</dt> <dd>

Intero utilizzato per costruire il nome di un evento. L'evento segnala che il client è pronto per ricevere dati. L'evento viene segnalato dopo l'elaborazione di nuovi dati.

</dd> <dt>

*pdwMutexAccessId* \[ Cambio\]
</dt> <dd>

Puntatore all'identificatore di accesso della memoria condivisa.

</dd> <dt>

*pdwFileMappingId* \[ Cambio\]
</dt> <dd>

Intero che identifica la memoria condivisa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il **metodo UseNamedSharedMemoryCommunications** fa parte del protocollo di memoria condivisa di Tablet PC. Un client senza privilegi elevati passa un ID di sicurezza (SID) e un ID di sicurezza a livello di integrità (IL-SID) in modo che il servizio Tablet possa utilizzare gli elenchi di controllo di accesso (ACL) per accedere agli oggetti di memoria condivisa. Se il client dispone di privilegi elevati, deve usare UseSharedMemoryCommunications, ovvero l'API che viene chiamata se il servizio dispone già di privilegi elevati.

La [**struttura SHAREDMEMORY \_ HEADER**](sharedmemory-header.md) archivia l'intestazione shared memory.

Viene [**eseguito il cast della struttura SHAREDMEMORY \_ HEADER**](sharedmemory-header.md) dai dati a cui fa riferimento il mapping del file. I dati del pacchetto non elaborati seguono **l'intestazione \_ SHAREDMEMORY**. I dati dei pacchetti non elaborati possono essere letti dalla memoria condivisa quando viene generato l'evento a cui fa riferimento *pdwEventClientReadyId.*

Nell'elenco seguente viene descritta la sequenza di eventi per l'accesso e l'uso della memoria condivisa.

1.  Il client genera l'evento clientReady.
2.  Il client attende l'evento moreData.
3.  Il client acquisisce il mutex.
4.  Il client legge i dati dei pacchetti dalla sezione della memoria condivisa che segue l'intestazione . I numeri di serie vengono visualizzati nella memoria condivisa dopo i dati del pacchetto.
5.  Il client gestisce i dati a seconda del valore di **dwEvent**.
6.  Il client scrive -1 (0xFFFFFFFF) in **dwEvent**.
7.  Il client rilascia il mutex.
8.  Il client genera l'evento clientReady.

I nomi degli eventi vengono creati tramite la formattazione dell'output di questo metodo. Le definizioni seguenti possono essere usate in combinazione con sprintf o l'equivalente per creare i nomi degli eventi.


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



In ogni definizione la sezione %d viene sostituita con l'ID del processo e la sezione %u viene sostituita con l'intero restituito in *pdwEventMoreDataId* o *pdwEventClientReadyId*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[**ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 





---
description: Consente di accedere alla memoria condivisa tra i thread del tablet.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'Metodo ITabletContextP:: UseSharedMemoryCommunications'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319167"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a>Metodo ITabletContextP:: UseSharedMemoryCommunications

Consente di accedere alla memoria condivisa tra i thread del tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PID* \[ in\]
</dt> <dd>

ID del processo.

</dd> <dt>

*phEventMoreData* \[ out\]
</dt> <dd>

Handle di evento che segnala quando i nuovi dati sono disponibili per l'elaborazione.

</dd> <dt>

*phEventClientReady* \[ out\]
</dt> <dd>

Handle di evento restituito utilizzato per segnalare che il client è pronto per la ricezione dei dati. Segnalato dopo l'elaborazione di nuovi dati.

</dd> <dt>

*phMutexAccess* \[ out\]
</dt> <dd>

Mutex che concede l'accesso alla memoria condivisa.

</dd> <dt>

*phFileMapping* \[ out\]
</dt> <dd>

Puntatore al blocco di memoria condivisa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo **UseSharedMemoryCommunications** viene utilizzato come parte del protocollo di memoria condivisa di Tablet PC. Poiché il servizio wisptis ha un livello di integrità elevato, può archiviare e accedere ai dati archiviati nella memoria condivisa senza dover elevare i propri privilegi.

Viene eseguito il cast della struttura dell' [**\_ intestazione SHAREDMEMORY**](sharedmemory-header.md) dai dati a cui fa riferimento il mapping del file e i dati dei pacchetti non elaborati seguono l' **\_ intestazione SHAREDMEMORY**. I dati dei pacchetti non elaborati possono essere letti dalla memoria condivisa quando viene generato l'evento a cui fa riferimento *pdwEventClientReady* .

Nell'elenco seguente viene descritta la sequenza di eventi per l'accesso e l'utilizzo della memoria condivisa.

-   Il client imposta l'evento clientReady.
-   Il client attende l'evento moreData.
-   Il client acquisisce il mutex.
-   Il client legge i dati dei pacchetti dalla sezione della memoria condivisa dopo l'intestazione e i numeri di serie dopo i pacchetti.
-   Il client gestisce i dati in base al valore di **dwEvent**.
-   Il client scrive-1 (0xFFFFFFFF) in **dwEvent**.
-   Il client rilascia il mutex.
-   Il client imposta l'evento clientReady.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 





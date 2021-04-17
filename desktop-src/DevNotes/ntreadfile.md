---
description: Legge i dati da un file aperto.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Funzione NtReadFile (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523177"
---
# <a name="ntreadfile-function"></a>NtReadFile (funzione)

Legge i dati da un file aperto.

Questa funzione è l'equivalente della modalità utente per la funzione [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentata in Windows Driver Kit (WDK).

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Filehandle* \[ in\]
</dt> <dd>

Handle per l'oggetto file. Questo handle viene creato da una chiamata riuscita a [**NTCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) o [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).

</dd> <dt>

*Evento* \[ in, facoltativo\]
</dt> <dd>

Facoltativamente, un handle a un oggetto evento da impostare sullo stato segnalato dopo il completamento dell'operazione di lettura. Il dispositivo e i driver intermedi devono impostare questo parametro su **null**.

</dd> <dt>

*ApcRoutine* \[ in, facoltativo\]
</dt> <dd>

Questo parametro è riservato. Il puntatore del dispositivo e i driver intermedi devono essere impostati su **null**.

</dd> <dt>

*ApcContext* \[ in, facoltativo\]
</dt> <dd>

Questo parametro è riservato. Il puntatore del dispositivo e i driver intermedi devono essere impostati su **null**.

</dd> <dt>

*IoStatusBlock* \[ out\]
</dt> <dd>

Puntatore a una struttura di [**\_ \_ blocco di stato io**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) che riceve lo stato di completamento finale e le informazioni sull'operazione di lettura richiesta. Il membro **Information** riceve il numero di byte effettivamente letti dal file.

</dd> <dt>

*Buffer* \[ out\]
</dt> <dd>

Puntatore a un buffer allocato dal chiamante che riceve i dati letti dal file.

</dd> <dt>

*Lunghezza* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta il *buffer*.

</dd> <dt>

*ByteOffset* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una variabile che specifica l'offset di byte iniziale nel file in cui inizierà l'operazione di lettura. Se viene effettuato un tentativo di lettura oltre la fine del file, **NtReadFile** restituisce un errore.

Se la chiamata a [**NTCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) imposta uno dei flag *createOptions* file di avviso i/o sincrono file \_ O file di i \_ \_ \_ \_ /o sincrono \_ , gestione i/O mantiene la posizione del file corrente. In tal caso, il chiamante di **NtReadFile** può specificare che venga utilizzato l'offset della posizione corrente del file anziché un valore *ByteOffset* esplicito. Questa specifica può essere eseguita utilizzando uno dei metodi seguenti:

-   Specificare un puntatore a un **valore \_ Integer grande** con il membro **HighPart** impostato su-1 e il membro **LowPart** impostato sul file di valori definito dal sistema \_ utilizzare la posizione del puntatore del \_ file \_ \_ .

-   Passare un puntatore **null** per *ByteOffset*.

**NtReadFile** aggiorna la posizione corrente del file aggiungendo il numero di byte letti quando viene completata l'operazione di lettura, se usa la posizione del file corrente gestita dal gestore di i/O.

Anche quando gestione i/O gestisce la posizione corrente del file, il chiamante può reimpostare questa posizione passando un valore *ByteOffset* esplicito a **NtReadFile**. In questo modo viene automaticamente modificata la posizione del file corrente in quel valore di *ByteOffset* , viene eseguita l'operazione di lettura e quindi la posizione viene aggiornata in base al numero di byte effettivamente letti. Questa tecnica fornisce al chiamante il servizio di ricerca e lettura atomiche.

</dd> <dt>

*Chiave* \[ di in, facoltativo\]
</dt> <dd>

Il puntatore del dispositivo e i driver intermedi devono essere impostati su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtReadFile** restituisce \_ l'esito positivo dello stato o il codice di errore NTSTATUS appropriato.

## <a name="remarks"></a>Commenti

I chiamanti di **NtReadFile** devono avere già chiamato [**NTCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) con i dati di lettura del file \_ o il \_ \_ valore di lettura generico impostato nel parametro *desiredAccess* .

Se la chiamata precedente a [**NTCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) impostano \_ il \_ \_ flag di buffering intermedio nel parametro *createOptions* su **NTCreateFile**, i parametri *length* e *ByteOffset* per **NtReadFile** devono essere multipli delle dimensioni del settore. Per ulteriori informazioni, vedere **NTCreateFile**.

**NtReadFile** inizia la lettura dal *ByteOffset* specificato o dalla posizione corrente del file nel *buffer* specificato. Termina l'operazione di lettura in una delle condizioni seguenti:

-   Il buffer è pieno perché il numero di byte specificato dal parametro *length* è stato letto. Pertanto, non è possibile inserire più dati nel buffer senza un overflow.

-   Viene raggiunta la fine del file durante l'operazione di lettura, pertanto non sono presenti altri dati nel file da trasferire nel buffer.

Se il chiamante ha aperto il file con il flag SYNCHRONIZE impostato in *desiredAccess*, il thread chiamante può eseguire la sincronizzazione fino al completamento dell'operazione di lettura in attesa dell'handle di file, *filehandle*. L'handle viene segnalato ogni volta che viene completata un'operazione di I/O eseguita nell'handle. Tuttavia, il chiamante non deve attendere un handle che è stato aperto per l'accesso sincrono al file, ovvero un avviso di i/o sincrono di file \_ \_ o file di i \_ /o \_ sincrono \_ \_ . In questo caso, **NtReadFile** attende per conto del chiamante e non restituisce alcun risultato fino a quando l'operazione di lettura non viene completata. Il chiamante può attendere in modo sicuro l'handle di file solo se vengono soddisfatte tutte e tre le condizioni seguenti:

-   L'handle è stato aperto per l'accesso asincrono, ovvero non \_ \_ \_  è stato specificato alcun flag i/o sincrono dei file.

-   L'handle viene utilizzato solo per un'operazione di I/O alla volta.

-   **NtReadFile** ha restituito lo stato \_ in sospeso.

Un driver deve chiamare **NtReadFile** nel contesto del processo di sistema se sussistono le condizioni seguenti:

-   Il driver ha creato l'handle di file che passa a **NtReadFile**.

-   **NtReadFile** invierà una notifica al driver del completamento i/O per mezzo di un evento creato dal driver.

-   **NtReadFile** invierà una notifica al driver del completamento i/O per mezzo di una routine di callback APC che il driver passa a **NtReadFile**.

Gli handle di file e di evento sono validi solo nel contesto di processo in cui vengono creati gli handle. Pertanto, per evitare problemi di sicurezza, il driver deve creare qualsiasi handle di file o evento che passa a **NtReadFile** nel contesto del processo di sistema piuttosto che del contesto del processo in cui si trova il driver.

Analogamente, **NtReadFile** deve essere chiamato nel contesto del processo di sistema se notifica al driver il completamento i/o per mezzo di un APC, perché APC vengono sempre attivati nel contesto del thread che rilascia la richiesta di i/o. Se il driver chiama **NtReadFile** nel contesto di un processo diverso da quello del sistema, l'APC potrebbe essere ritardato per un periodo illimitato o potrebbe non essere attivato.

Per ulteriori informazioni sull'utilizzo dei file, vedere [utilizzo di file in un driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).

I chiamanti di **NtReadFile** devono essere in esecuzione al livello livello IRQL = passive \_ e [con APC kernel speciale abilitato](/windows-hardware/drivers/kernel/disabling-apcs).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                    |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Intestazione<br/>                   | <dl> <dt>WDM. h (include WDM. h, ntddk. h o Ntifs. h)</dt> </dl>                   |
| Libreria<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll (modalità utente)</dt> </dl>                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**KeInitializeEvent**](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[**NtQueryInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[**NtSetInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[**NtWriteFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 

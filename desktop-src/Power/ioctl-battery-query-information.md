---
description: Recupera un'ampia gamma di informazioni per la batteria.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION codice di controllo (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: a48514b81ddf5d8f7c0d84d4404eb01752413e73ade43db089fbb6dade673bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143534"
---
# <a name="ioctl_battery_query_information-control-code"></a>CODICE DI CONTROLLO DELLE \_ INFORMAZIONI SULLE QUERY DELLA \_ \_ BATTERIA IOCTL

Recupera un'ampia gamma di informazioni per la batteria.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle della batteria su cui devono essere restituite le informazioni. Per recuperare un handle di dispositivo, chiamare [**la funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo in cui eseguirla. Usare **IOCTL \_ BATTERY QUERY INFORMATION \_ \_ per** questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a una [**struttura BATTERY \_ QUERY \_ INFORMATION.**](battery-query-information-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni del buffer di input, in byte.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore al buffer restituito. Il tipo di dati (e quindi le dimensioni) del buffer restituito dipende dalle informazioni richieste nel membro **BATTERY \_ QUERY INFORMATION \_ \_ LEVEL** della struttura [**BATTERY QUERY INFORMATION \_ \_ di**](battery-query-information-str.md) input.

Nella tabella seguente vengono illustrati i dati restituiti da un determinato livello di informazioni.



| Livello informazioni                 | Dati restituiti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | **Stringa Unicode** con terminazione Null che specifica il nome della batteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | Valore **ULONG** che specifica il tempo di esecuzione stimato della batteria, espresso in secondi. Se la frequenza di svuotamento fornita nel membro **AtRate** della struttura [**BATTERY QUERY \_ \_ INFORMATION**](battery-query-information-str.md) è zero, questo calcolo si basa sulla frequenza corrente di svuotamento. Se **AtRate** è diverso da zero, il tempo restituito è il tempo di esecuzione previsto per la frequenza specificata. Se il tempo stimato è sconosciuto (ad esempio, la batteria non viene scaricata e **AtRate** è zero), viene restituito **BATTERY UNKNOWN \_ \_ TIME.** Si noti che questo valore non è molto accurato in alcuni sistemi a batteria. Il valore può variare notevolmente a seconda del consumo di energia corrente, che potrebbe essere influenzato dall'attività del disco e da altri fattori. Non esiste alcun meccanismo di notifica per le modifiche apportate a questo valore. |
| **BatteryGranularityInformation** | Matrice a lunghezza variabile di strutture [**BATTERY \_ REPORTING \_ SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) che contiene la granularità dei report per la capacità della batteria restituita da [**IOCTL \_ BATTERY QUERY \_ \_ STATUS**](ioctl-battery-query-status.md). Vengono restituite più voci quando la granularità dipende dalla capacità attuale della batteria. Vedere **BATTERY REPORTING SCALE \_ \_ per** l'interpretazione della matrice di voci. Il numero di voci è indicato dalla dimensione del buffer restituito e può essere calcolato come (*lpBytesReturned/sizeof* (**BATTERY REPORTING \_ \_ SCALE**)). Il numero massimo di voci che verranno restituite è quattro.                                                                                                |
| **BatteryInformation**            | Struttura [**BATTERY \_ INFORMATION.**](battery-information-str.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | Struttura [**BATTERY \_ MANUFACTURE \_ DATE.**](battery-manufacture-date-str.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | **Stringa Unicode** con terminazione Null contenente il nome del produttore della batteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | **Stringa Unicode** con terminazione Null che contiene il numero di serie della batteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | **ULONG** che contiene la temperatura corrente della batteria, in 10° di grado Kelvin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | **Stringa Unicode** con terminazione Null che identifica in modo univoco la batteria. Questo valore può essere usato per tenere traccia di una batteria specifica. Nel caso di batterie intelligenti, questo ID sarà la concatenazione del nome del produttore, del nome del dispositivo, della data di produzione e di una rappresentazione stampabile del numero di serie. Questo valore non deve essere visualizzato all'utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output. A seconda del livello di informazioni dei dati richiesti, può trattarsi di un buffer di dimensioni variabili.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati restituiti nel buffer *lpOutBuffer,* in byte.

Se il buffer di output è troppo piccolo per restituire dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore **ERROR INSUFFICIENT \_ \_ BUFFER** e il numero di byte restituiti è zero.

Se *lpOverlapped* è **NULL** (I/O non sovrapposto), *lpBytesReturned* non può essere **NULL.**

Se *lpOverlapped* non è **NULL** (I/O sovrapposto), *lpBytesReturned* può essere **NULL.** Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la [**funzione GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Se *hDevice è* associato a una porta di completamento I/O, è possibile ottenere il numero di byte restituiti chiamando la [**funzione GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice è* stato aperto con il flag **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida. In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona). Se il dispositivo è stato aperto con il flag **FILE \_ FLAG \_ OVERLAPPED** e *lpOverlapped* è **NULL,** la funzione ha esito negativo in modi imprevedibili.

Se *hDevice* è stato aperto senza specificare il flag **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non restituisce alcun valore fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione non riesce o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Alcune informazioni sulle batterie sono facoltative o potrebbero non essere importanti per alcune batterie. Se il particolare tipo di dati richiesto non è disponibile per la batteria corrente, viene **restituito ERROR \_ INVALID \_ FUNCTION.**

Tutte le richieste di informazioni sulla batteria verranno completate con lo stato **ERROR \_ FILE NOT \_ \_ FOUND** ogni volta che l'elemento **BatteryTag** della richiesta non corrisponde a quello del tag della batteria corrente. Ciò garantisce che le informazioni sulla batteria restituite corrispondano a quella della batteria richiesta. Per altre [informazioni, vedere Tag](battery-information.md) della batteria.

## <a name="remarks"></a>Commenti

Questa batteria IOCTL recupera un'ampia gamma di informazioni per la batteria. La struttura del parametro di input [**BATTERY \_ QUERY \_ INFORMATION**](battery-query-information-str.md)indica il tipo di informazioni da restituire e il momento in cui devono essere restituite le informazioni sulla batteria. Il tipo di dati e il contenuto del buffer di output variano in base ai dati richiesti.

Per informazioni sulle implicazioni dell'I/O sovrapposto su questa operazione, vedere la sezione Osservazioni [**dell'argomento DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="examples"></a>Esempio

Per un esempio, vedere [Enumerazione dei dispositivi a batteria.](enumerating-battery-devices.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>BatClass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sulla batteria](battery-information.md)
</dt> <dt>

[Codici di controllo del risparmio energia](power-management-control-codes.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**INFORMAZIONI \_ SULLE QUERY SULLA \_ BATTERIA**](battery-query-information-str.md)
</dt> <dt>

[**SCALA DI \_ SEGNALAZIONE \_ DELLA BATTERIA**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**STATO DELLA \_ QUERY SULLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**TAG DI QUERY DELLA BATTERIA IOCTL \_ \_ \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**INFORMAZIONI SUL \_ SET DI \_ BATTERIA IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 


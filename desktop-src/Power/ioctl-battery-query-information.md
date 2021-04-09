---
description: Recupera una serie di informazioni per la batteria.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: Codice di controllo IOCTL_BATTERY_QUERY_INFORMATION (Poclass. h)
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
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967495"
---
# <a name="ioctl_battery_query_information-control-code"></a>\_Codice di \_ \_ controllo delle informazioni sulle query della batteria IOCTL

Recupera una serie di informazioni per la batteria.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

Handle per la batteria in cui devono essere restituite le informazioni. Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla. Usare **\_ \_ \_ le informazioni sulle query della batteria IOCTL** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a una struttura [**di \_ \_ informazioni sulle query della batteria**](battery-query-information-str.md) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di input.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore al buffer restituito. Il tipo di dati (e, di conseguenza, le dimensioni) del buffer restituito dipende dalle informazioni richieste nel membro **del \_ \_ \_ livello di informazioni** della query della batteria [**di \_ \_ input.**](battery-query-information-str.md)

La tabella seguente mostra i dati restituiti da un determinato livello di informazioni.



| Livello informazioni                 | Dati restituiti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | Stringa Unicode con terminazione **null** che specifica il nome della batteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | **ULONG** che specifica il tempo di esecuzione della batteria stimato, in secondi. Se la frequenza di svuotamento fornita nel membro **AtRate** della struttura di [**\_ \_ informazioni sulle query della batteria**](battery-query-information-str.md) è zero, questo calcolo è basato sulla velocità attuale di svuotamento. Se **AtRate** è diverso da zero, l'ora restituita è il tempo di esecuzione previsto per la velocità specificata. Se il tempo stimato è sconosciuto (ad esempio, la batteria non viene ricaricata e **AtRate** è zero), viene restituita l' **\_ \_ ora della batteria sconosciuta** . Si noti che questo valore non è molto accurato in alcuni sistemi a batteria. Il valore può variare notevolmente a seconda del consumo di energia attuale, che può essere influenzato dall'attività del disco e da altri fattori. Non esiste alcun meccanismo di notifica delle modifiche in questo valore. |
| **BatteryGranularityInformation** | Matrice a lunghezza variabile di strutture [**di \_ \_ scalabilità di report della batteria**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) che contiene la granularità dei report per la capacità della batteria restituita dallo [**\_ \_ \_ stato della query della batteria IOCTL**](ioctl-battery-query-status.md). Quando la granularità dipende dalla capacità attuale della batteria, vengono restituite più voci. Vedere la pagina relativa alla **\_ \_ scalabilità dei report batteria** per l'interpretazione della matrice di voci. Il numero di voci è indicato dalla dimensione del buffer restituito e può essere calcolato come (*lpBytesReturned* /sizeof (**\_ \_ scala di report della batteria**)). Il numero massimo di voci che verranno restituite è quattro.                                                                                                |
| **BatteryInformation**            | Struttura [**\_ delle informazioni sulla batteria**](battery-information-str.md) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | Struttura [**della \_ \_ Data di produzione della batteria**](battery-manufacture-date-str.md) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | Stringa Unicode con terminazione **null** che contiene il nome del produttore della batteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | Stringa Unicode con terminazione **null** che contiene il numero di serie della batteria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | **ULONG** che contiene la temperatura corrente della batteria, in decimi di grado Kelvin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | Stringa Unicode con terminazione **null** che identifica in modo univoco la batteria. Questo valore può essere usato per tenere traccia di una batteria specifica. Nel caso di batterie intelligenti, questo ID sarà la concatenazione del nome del produttore, del nome del dispositivo, della data di produzione e di una rappresentazione stampabile del numero di serie. Questo valore non può essere visualizzato all'utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output. A seconda del livello di informazioni dei dati richiesti, può trattarsi di un buffer di dimensioni variabili.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve la dimensione dei dati restituiti nel buffer *lpOutBuffer* , in byte.

Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il **\_ \_ buffer insufficiente** nell'errore del codice di errore e il numero di byte restituito è zero.

Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**.

Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**. Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* è stato aperto con il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida. In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona). Se il dispositivo è stato aperto con il flag **file \_ \_ sovrapposto** e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.

Se *hDevice* è stato aperto senza specificare il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non viene restituita fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Alcune informazioni sulle batterie sono facoltative o potrebbero non essere significative per alcune batterie. Se il tipo specifico di dati richiesti non è disponibile per la batteria corrente, viene restituita la **\_ \_ funzione Error non valida** .

Tutte le richieste di informazioni sulla batteria vengono completate con lo stato del **file di errore \_ \_ non \_ trovato** ogni volta che l'elemento **BatteryTag** della richiesta non corrisponde a quello del tag della batteria corrente. In questo modo si garantisce che le informazioni della batteria restituita corrispondano a quelle della batteria richiesta. Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) .

## <a name="remarks"></a>Commenti

Questo comando IOCTL batteria recupera una serie di informazioni per la batteria. La struttura del parametro di input, [**\_ \_ informazioni sulle query della batteria**](battery-query-information-str.md), indica il tipo di informazioni da restituire e quando devono essere restituite le informazioni sulla batteria. Il tipo di dati e il contenuto del buffer di output variano in base ai dati richiesti.

Per le implicazioni dell'I/O sovrapposto in questa operazione, vedere la sezione Osservazioni dell'argomento [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="examples"></a>Esempio

Per un esempio, vedere [enumerazione dei dispositivi a batteria](enumerating-battery-devices.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>BatClass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sulla batteria](battery-information.md)
</dt> <dt>

[Codici di controllo del risparmio energia](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_informazioni sulle query della batteria \_**](battery-query-information-str.md)
</dt> <dt>

[**\_ \_ scalabilità report batteria**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**\_stato della \_ query della batteria IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_tag di \_ query della batteria IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_ \_ informazioni sui set di batterie IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 


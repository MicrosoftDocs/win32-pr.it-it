---
description: La funzione AddJob aggiunge un processo di stampa all'elenco dei processi di stampa che possono essere pianificati dallo spooler di stampa. La funzione recupera il nome del file che è possibile usare per archiviare il processo.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Funzione AddJob (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de99b0866e8cd7ec8486d2a3f15f95194b4350008a43fe4db8ae82d970684c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950751"
---
# <a name="addjob-function"></a>Funzione AddJob

La **funzione AddJob** aggiunge un processo di stampa all'elenco dei processi di stampa che possono essere pianificati dallo spooler di stampa. La funzione recupera il nome del file che è possibile usare per archiviare il processo.

> [!NOTE]
> In Windows 8 e versioni successive, non è consigliabile usare **AddJob** direttamente perché in alcuni casi,ad esempio la stampa in una coda con File: o PORTPROMPT: dove **AddJob avrà** esito negativo. È invece consigliabile usare l'API di stampa [GDI,](gdi-printing.md)l'API di stampa [XPS,](xps-printing.md) [**StartDocPrinter**](startdocprinter.md)o il metodo appropriato dal [**Windows. Spazio dei nomi Graphics.Printing,**](/uwp/api/Windows.Graphics.Printing) a seconda dello scenario di stampa.
>
> Se si tenta di stampare in una coda usando **File:** o **PORTPROMPT:**, **AddJob** restituirà l'errore NOT \_ SUPPORTED.

## <a name="syntax"></a>Sintassi

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle che specifica la stampante per il processo di stampa. Deve trattarsi di una stampante locale configurata come stampante con spooling. Se *hPrinter è* un handle per una connessione remota alla stampante o se la stampante è configurata per la stampa diretta, la **funzione AddJob** ha esito negativo. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Versione della struttura dei dati delle informazioni del processo di stampa archiviata dalla funzione nel buffer a cui punta *pData.* Impostare questo parametro su uno.

</dd> <dt>

*pData* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una struttura di [**dati ADDJOB \_ INFO \_ 1**](addjob-info-1.md) e una stringa di percorso.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pData.* Il buffer deve essere sufficientemente grande da contenere una [**struttura ADDJOB \_ INFO \_ 1**](addjob-info-1.md) e una stringa di percorso.

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni totali, in byte, della struttura di dati [**ADDJOB \_ INFO \_ 1**](addjob-info-1.md) più la stringa di percorso. Se questo valore è minore o uguale a *cbBuf* e la funzione ha esito positivo, si tratta del numero effettivo di byte scritti nel buffer a cui punta *pData*. Se questo numero è maggiore di *cbBuf*, il buffer è troppo piccolo ed è necessario chiamare di nuovo la funzione con una dimensione del buffer almeno uguale a \* *pcbNeeded*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

È possibile chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il file di spooling specificato dal membro **Path** della struttura [**ADDJOB \_ INFO \_ 1**](addjob-info-1.md) e quindi chiamare la [**funzione WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per scrivere i dati del processo di stampa. Al termine, chiamare la funzione [**ScheduleJob**](schedulejob.md) per notificare lo spooler di stampa che il processo di stampa può ora essere pianificato dallo spooler per la stampa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddJobW** (Unicode) **e AddJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ADDJOB \_ INFO \_ 1**](addjob-info-1.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[API di stampa GDI](gdi-printing.md)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Processo di pianificazione**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Windows. Graphics.Printing**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[API di stampa XPS](xps-printing.md)
</dt> </dl>

 


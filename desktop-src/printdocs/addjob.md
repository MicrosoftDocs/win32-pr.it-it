---
description: La funzione AddJob aggiunge un processo di stampa all'elenco dei processi di stampa che possono essere pianificati dallo spooler di stampa. La funzione recupera il nome del file che è possibile usare per archiviare il processo.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Funzione AddJob (winspool. h)
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
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756410"
---
# <a name="addjob-function"></a>AddJob (funzione)

La funzione **AddJob** aggiunge un processo di stampa all'elenco dei processi di stampa che possono essere pianificati dallo spooler di stampa. La funzione recupera il nome del file che è possibile usare per archiviare il processo.

> [!NOTE]
> Nei sistemi operativi Windows 8 e versioni successive, non è consigliabile usare direttamente **AddJob** perché esistono casi, ad esempio la stampa in una coda con file: o PORTPROMPT:) dove **AddJob** avrà esito negativo. Si consiglia invece di utilizzare l' [API di stampa GDI](gdi-printing.md), l' [API di stampa XPS](xps-printing.md), [**StartDocPrinter**](startdocprinter.md)o il metodo appropriato dallo spazio dei nomi [**Windows. graphics. Printing**](/uwp/api/Windows.Graphics.Printing) , a seconda dello scenario di stampa.
>
> Se si tenta di stampare in una coda usando **file:** o **PORTPROMPT:**, **ADDJOB** restituirà l' \_ errore non supportato.

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

*hPrinter* \[ in\]
</dt> <dd>

Handle che specifica la stampante per il processo di stampa. Deve trattarsi di una stampante locale configurata come stampante con spooling. Se *hPrinter* è un handle per una connessione stampante remota o se la stampante è configurata per la stampa diretta, la funzione **AddJob** ha esito negativo. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura di dati del processo di stampa che la funzione archivia nel buffer a cui punta *pData*. Impostare questo parametro su uno.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una struttura di dati [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e una stringa di percorso.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pData*. Il buffer deve essere sufficientemente grande da contenere una struttura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e una stringa di percorso.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni totali, in byte, della struttura di dati [**ADDJOB \_ info \_ 1**](addjob-info-1.md) più la stringa di percorso. Se questo valore è minore o uguale a *cbBuf* e la funzione ha esito positivo, si tratta del numero effettivo di byte scritti nel buffer a cui punta *pData*. Se questo numero è maggiore di *cbBuf*, il buffer è troppo piccolo ed è necessario chiamare nuovamente la funzione con una dimensione del buffer almeno pari a \* *pcbNeeded*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

È possibile chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il file dello spooler specificato dal membro **path** della struttura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) , quindi chiamare la funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per scrivere i dati del processo di stampa. Al termine di questa operazione, chiamare la funzione [**ScheduleJob**](schedulejob.md) per notificare allo spooler di stampa che il processo di stampa può essere pianificato dallo spooler per la stampa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddJobW** (Unicode) e **AddJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ADDJOB \_ info \_ 1**](addjob-info-1.md)
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

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Windows. graphics. Printing**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[API di stampa XPS](xps-printing.md)
</dt> </dl>

 


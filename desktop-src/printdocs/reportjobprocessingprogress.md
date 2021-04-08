---
description: Segnala al servizio spooler di stampa se un processo di stampa XPS si trova nella fase di spooling o di rendering e quale parte dell'elaborazione è attualmente in corso.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Funzione ReportJobProcessingProgress (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967941"
---
# <a name="reportjobprocessingprogress-function"></a>ReportJobProcessingProgress (funzione)

Segnala al servizio spooler di stampa se un processo di stampa XPS si trova nella fase di spooling o di rendering e quale parte dell'elaborazione è attualmente in corso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*printerHandle* \[ in\]
</dt> <dd>

Handle della stampante per il quale la funzione deve recuperare informazioni. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*jobId* \[in\]
</dt> <dd>

Identifica il processo di stampa per il quale recuperare i dati. Usare la funzione [**AddJob**](addjob.md) o la funzione [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) per ottenere un identificatore del processo di stampa.

</dd> <dt>

*jobOperation* 
</dt> <dd>

Specifica se il processo si trova nella fase di spooling o nella fase di rendering.

</dd> <dt>

*jobProgress* 
</dt> <dd>

Specifica la parte dell'elaborazione attualmente in corso. Questo valore si riferisce agli eventi in fase di spooling o di rendering, a seconda del valore di *jobOperation*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.

Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

> [!Note]  
> **ReportJobProcessingProgress** segnala lo stato di avanzamento del processo di stampa XPS solo se il processo di stampa si trova nella fase di spooling o di rendering. **ReportJobProcessingProgress** avrà esito negativo se viene chiamato quando il processo di stampa XPS non si trova nella fase di spooling o di rendering.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EPrintXPSJobOperation**](eprintxpsjoboperation.md)
</dt> <dt>

[**EPrintXPSJobProgress**](eprintxpsjobprogress.md)
</dt> </dl>

 


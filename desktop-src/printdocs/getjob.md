---
description: La funzione GetJob recupera informazioni su un processo di stampa specificato.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: Funzione GetJob (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 26665d6141ea36adbe8aeeca0555bc6a5e918cb5213a4fb7a6dbd315eac92a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949082"
---
# <a name="getjob-function"></a>Funzione GetJob

La **funzione GetJob** recupera informazioni su un processo di stampa specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per cui vengono recuperati i dati del processo di stampa. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*JobId* \[ Pollici\]
</dt> <dd>

Identifica il processo di stampa per il quale recuperare i dati. Usare la [**funzione AddJob**](addjob.md) o [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) per ottenere un identificatore del processo di stampa.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Tipo di informazioni restituite nel buffer *pJob.* Se *Level* è 1, *pJob* riceve una [**struttura JOB INFO \_ \_ 1.**](job-info-1.md) Se *Level* è 2, *pJob* riceve una [**struttura JOB INFO \_ \_ 2.**](job-info-2.md)

</dd> <dt>

*pJob* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una struttura [**JOB \_ INFO \_ 1**](job-info-1.md) o [**JOB INFO \_ \_ 2**](job-info-2.md) contenente informazioni sul processo. Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui puntano i membri della struttura.

Per determinare le dimensioni del buffer necessarie, chiamare **GetJob** con *cbBuf* impostato su zero. **GetJob** ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR INSUFFICIENT BUFFER e il \_ parametro \_ *pcbNeeded* restituisce le dimensioni, in byte, del buffer necessario per contenere la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, della matrice.

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a un valore che specifica il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetJobW** (Unicode) e **GetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL PROCESSO \_ 1**](job-info-1.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL PROCESSO \_ 2**](job-info-2.md)
</dt> <dt>

[**Processo di pianificazione**](schedulejob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 


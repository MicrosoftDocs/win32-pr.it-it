---
description: La funzione EnumJobs recupera le informazioni su un set specificato di processi di stampa per una stampante specificata.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Funzione EnumJobs (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232523"
---
# <a name="enumjobs-function"></a>EnumJobs (funzione)

La funzione **EnumJobs** recupera le informazioni su un set specificato di processi di stampa per una stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per l'oggetto stampante i cui processi di stampa vengono enumerati dalla funzione. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*FirstJob* \[ in\]
</dt> <dd>

Posizione in base zero all'interno della coda di stampa del primo processo di stampa da enumerare. Ad esempio, un valore pari a 0 indica che l'enumerazione deve iniziare dal primo processo di stampa nella coda di stampa. il valore 9 indica che l'enumerazione deve iniziare al decimo processo di stampa nella coda di stampa.

</dd> <dt>

*Nojobs* \[ in\]
</dt> <dd>

Numero totale di processi di stampa da enumerare.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Tipo di informazioni restituite nel buffer di *pJob* .



| Valore                                                                                                | Significato                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pJob* riceve una matrice di strutture di [**informazioni sul processo \_ \_ 1**](job-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pJob* riceve una matrice di strutture di [**informazioni sul processo \_ \_ 2**](job-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pJob* riceve una matrice di strutture di [**informazioni sul processo \_ \_ 3**](job-info-3.md)<br/> |



 

</dd> <dt>

*pJob* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture di informazioni sul processo [**\_ \_ 1**](job-info-1.md), [**informazioni sul processo \_ \_ 2**](job-info-2.md)o [**informazioni sul processo \_ \_ 3**](job-info-3.md) . Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa o altri dati a cui fanno riferimento i membri della struttura.

Per determinare le dimensioni del buffer richieste, chiamare **EnumJobs** con *cbBuf* impostato su zero. **EnumJobs** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pJob* .

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte copiati se la funzione ha esito positivo. Se la funzione ha esito negativo, la variabile riceve il numero di byte necessari.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture di informazioni di processo [**\_ \_ 1**](job-info-1.md), [**informazioni sul processo \_ \_ 2**](job-info-2.md)o [**informazioni sul processo \_ \_ 3**](job-info-3.md) restituite nel buffer *pJob* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

La [**struttura \_ info processo \_ 1**](job-info-1.md) contiene informazioni generali sul processo di stampa. la struttura di informazioni sul [**processo \_ \_ 2**](job-info-2.md) contiene informazioni molto più dettagliate. La [**struttura \_ informazioni \_ sul processo 3**](job-info-3.md) contiene informazioni sulla modalità di collegamento dei processi.

Per determinare il numero di processi di stampa nella coda della stampante, chiamare la funzione [**GetPrinter**](getprinter.md) con il parametro *Level* impostato su 2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumJobsW** (Unicode) e **EnumJobsA** (ANSI)<br/>                                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Informazioni processo \_ 1**](job-info-1.md)
</dt> <dt>

[**Informazioni sul processo \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**Informazioni sul processo \_ \_ 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 


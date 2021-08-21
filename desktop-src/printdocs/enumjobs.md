---
description: La funzione EnumJobs recupera informazioni su un set specificato di processi di stampa per una stampante specificata.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Funzione EnumJobs (Winspool.h)
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
ms.openlocfilehash: 57c8416b1c1f5820f632271b0ef0973c76a14be9ef08f24b217ebee441fb29d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056511"
---
# <a name="enumjobs-function"></a>Funzione EnumJobs

La **funzione EnumJobs** recupera informazioni su un set specificato di processi di stampa per una stampante specificata.

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto stampante i cui processi di stampa vengono enumerati dalla funzione. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*FirstJob* \[ Pollici\]
</dt> <dd>

Posizione in base zero all'interno della coda di stampa del primo processo di stampa da enumerare. Ad esempio, il valore 0 specifica che l'enumerazione deve iniziare in corrispondenza del primo processo di stampa nella coda di stampa. Il valore 9 specifica che l'enumerazione deve iniziare in corrispondenza del decimo processo di stampa nella coda di stampa.

</dd> <dt>

*NoJobs* \[ Pollici\]
</dt> <dd>

Numero totale di processi di stampa da enumerare.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Tipo di informazioni restituite nel buffer *pJob.*



| Valore                                                                                                | Significato                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pJob* riceve una matrice di [**strutture JOB INFO \_ \_ 1**](job-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pJob* riceve una matrice di [**strutture JOB INFO \_ \_ 2**](job-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pJob* riceve una matrice di [**strutture JOB INFO \_ \_ 3**](job-info-3.md)<br/> |



 

</dd> <dt>

*pJob* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture [**JOB \_ INFO \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2**](job-info-2.md)o [**JOB INFO \_ \_ 3.**](job-info-3.md) Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa o altri dati a cui puntano i membri della struttura.

Per determinare le dimensioni del buffer necessarie, chiamare **EnumJobs** con *cbBuf* impostato su zero. **EnumJobs** ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR INSUFFICIENT BUFFER e il parametro \_ \_ *pcbNeeded* restituisce le dimensioni, in byte, del buffer necessario per contenere la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pJob.*

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte copiati se la funzione ha esito positivo. Se la funzione ha esito negativo, la variabile riceve il numero di byte necessari.

</dd> <dt>

*pcReturned* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture [**JOB \_ INFO \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2**](job-info-2.md)o [**JOB INFO \_ \_ 3**](job-info-3.md) restituite nel buffer *pJob.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

La [**struttura JOB INFO \_ \_ 1**](job-info-1.md) contiene informazioni generali sul processo di stampa. La [**struttura JOB INFO \_ \_ 2**](job-info-2.md) contiene informazioni molto più dettagliate. La [**struttura JOB INFO \_ \_ 3**](job-info-3.md) contiene informazioni sulla modalità di collegamento dei processi.

Per determinare il numero di processi di stampa nella coda della stampante, chiamare la [**funzione GetPrinter**](getprinter.md) con il *parametro Level* impostato su 2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumJobsW** (Unicode) ed **EnumJobsA** (ANSI)<br/>                                               |



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

[**INFORMAZIONI \_ SUL PROCESSO \_ 1**](job-info-1.md)
</dt> <dt>

[**JOB \_ INFO \_ 2**](job-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL PROCESSO \_ 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 


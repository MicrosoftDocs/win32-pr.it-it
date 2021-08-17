---
description: La funzione ScheduleJob richiede che lo spooler di stampa pianifica un processo di stampa specificato per la stampa.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Funzione ScheduleJob (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 9a09d3e67b4be422f10db7761f28a2aa873e9bd0d84ec2c09de23ae20c7cea4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470226"
---
# <a name="schedulejob-function"></a>Funzione ScheduleJob

La **funzione ScheduleJob** richiede che lo spooler di stampa pianifica un processo di stampa specificato per la stampa.

## <a name="syntax"></a>Sintassi


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per il processo di stampa. Deve trattarsi di una stampante locale configurata come stampante con spooling. Se *hPrinter è* un handle per una connessione remota della stampante o se la stampante è configurata per la stampa diretta, la **funzione ScheduleJob** ha esito negativo. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

*hPrinter* deve essere lo stesso handle di stampante specificato nella chiamata ad [**AddJob**](addjob.md) che ha ottenuto l'identificatore del processo di stampa *dwJobID.*

</dd> <dt>

*dwJobID* \[ Pollici\]
</dt> <dd>

Processo di stampa da programmare. Per ottenere questo identificatore del processo di stampa, chiamare [**la funzione AddJob.**](addjob.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

È necessario chiamare correttamente la [**funzione AddJob**](addjob.md) prima di chiamare la **funzione ScheduleJob.** **AddJob** ottiene l'identificatore del processo di stampa passato a **ScheduleJob** *come dwJobID*. Entrambe le chiamate devono usare lo stesso valore *per hPrinter*.

La **funzione ScheduleJob** verifica la presenza di un file di spooling valido. Se è presente un file di spooling non valido o se è vuoto, **ScheduleJob** elimina sia il file di spooling che la voce corrispondente del processo di stampa nello spooler di stampa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 





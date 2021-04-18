---
description: La funzione FlushPrinter Invia un buffer alla stampante per cancellarla da uno stato temporaneo.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Funzione FlushPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528998"
---
# <a name="flushprinter-function"></a>FlushPrinter (funzione)

La funzione **FlushPrinter** Invia un buffer alla stampante per cancellarla da uno stato temporaneo.

## <a name="syntax"></a>Sintassi


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per l'oggetto Printer. Deve corrispondere allo stesso handle utilizzato, in una chiamata [**WritePrinter**](writeprinter.md) precedente, dal driver della stampante.

</dd> <dt>

*pbuf* \[ in\]
</dt> <dd>

Puntatore a una matrice di byte che contiene i dati da scrivere sulla stampante.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, della matrice a cui punta *pbuf*.

</dd> <dt>

*pcWritten* \[ out\]
</dt> <dd>

Puntatore a un valore che riceve il numero di byte di dati scritti nella stampante.

</dd> <dt>

*cSleep* \[ in\]
</dt> <dd>

Tempo, in millisecondi, per il quale la riga di I/O nella porta della stampante deve rimanere inattiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

**FlushPrinter** deve essere chiamato solo se [**WritePrinter**](writeprinter.md) ha avuto esito negativo, lasciando la stampante in uno stato temporaneo. Ad esempio, la stampante potrebbe entrare in uno stato temporaneo quando il processo viene interrotto e il driver della stampante ha inviato parzialmente dati non elaborati alla stampante.

**FlushPrinter** può inoltre specificare un periodo di inattività durante il quale lo spooler di stampa non pianifica alcun processo nella porta stampante corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 





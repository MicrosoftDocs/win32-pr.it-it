---
description: La funzione ReadPrinter recupera i dati dalla stampante specificata.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: Funzione ReadPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ddbdfc03b80557583c60f461f0c7e3a6fe2473fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314000"
---
# <a name="readprinter-function"></a>ReadPrinter (funzione)

La funzione **ReadPrinter** recupera i dati dalla stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per l'oggetto stampante per il quale recuperare i dati. Utilizzare la funzione [**OpenPrinter**](openprinter.md) per recuperare un handle di oggetto Printer. Usare il formato: PrinterName, job xxxx.

</dd> <dt>

*pbuf* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve i dati della stampante.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pbuf* .

</dd> <dt>

*pNoBytesRead* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte di dati copiati nella matrice a cui punta *pbuf* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

**ReadPrinter** restituisce un errore se il dispositivo o la stampante non è bidirezionale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 





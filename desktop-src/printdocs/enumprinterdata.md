---
description: La funzione EnumPrinterData enumera i dati di configurazione per una stampante specificata.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Funzione EnumPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227349"
---
# <a name="enumprinterdata-function"></a>EnumPrinterData (funzione)

La funzione **EnumPrinterData** enumera i dati di configurazione per una stampante specificata.

Per recuperare i dati di configurazione in una singola chiamata, utilizzare la funzione [**EnumPrinterDataEx**](enumprinterdataex.md) .

## <a name="syntax"></a>Sintassi


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante i cui dati di configurazione devono essere ottenuti. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Valore di indice che specifica il valore dei dati di configurazione da recuperare.

Impostare questo parametro su zero per la prima chiamata a **EnumPrinterData** per un handle di stampante specificato. Quindi incrementare di uno il parametro per le chiamate successive che interessano la stessa stampante, finché la funzione non restituisce un errore di \_ \_ altri \_ elementi. Per ulteriori informazioni, vedere la sezione Osservazioni riportata di seguito.

Se si usa la tecnica descritta nelle descrizioni dei parametri *cbValueName* e *cbData* per ottenere valori di dimensioni del buffer adeguati, impostando entrambi i parametri su zero in una prima chiamata a **EnumPrinterData** per un handle di stampante specificato, il valore di *dwIndex* non è rilevante per la chiamata. Impostare *dwIndex* su zero nella chiamata successiva a **EnumPrinterData** per avviare il processo di enumerazione effettivo.

I valori dei dati di configurazione non sono ordinati. I nuovi valori avranno un indice arbitrario. Ciò significa che la funzione **EnumPrinterData** può restituire valori in qualsiasi ordine.

</dd> <dt>

*pValueName* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve il nome del valore dei dati di configurazione, incluso un carattere null di terminazione.

</dd> <dt>

*cbValueName* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pValueName*.

Se si desidera che il sistema operativo fornisca una dimensione del buffer adeguata, impostare questo parametro e il parametro *cbData* su zero per la prima chiamata a **EnumPrinterData** per un handle di stampante specificato. Quando la funzione restituisce, la variabile a cui punta *pcbValueName* conterrà una dimensione del buffer sufficientemente grande da poter enumerare correttamente tutti i nomi dei valori dei dati di configurazione della stampante.

</dd> <dt>

*pcbValueName* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte archiviati nel buffer a cui punta *pValueName*.

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato. Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](/windows/desktop/SysInfo/registry-value-types). Il parametro *pType* può essere **null** se il codice di tipo non è obbligatorio.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve il valore dei dati di configurazione.

Questo parametro può essere **null** se il valore dei dati di configurazione non è obbligatorio.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pData*.

Se si desidera che il sistema operativo fornisca una dimensione del buffer adeguata, impostare questo parametro e il parametro *cbValueName* su zero per la prima chiamata a **EnumPrinterData** per un handle di stampante specificato. Quando la funzione restituisce, la variabile a cui punta *pcbData* conterrà una dimensione del buffer sufficientemente grande da poter enumerare correttamente tutti i nomi dei valori dei dati di configurazione della stampante.

</dd> <dt>

*pcbData* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte archiviati nel buffer a cui punta *pData*.

Questo parametro può essere **null** se *pData* è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.

La funzione restituisce un errore se non sono presenti altri \_ \_ \_ valori dei dati di configurazione da recuperare per un handle di stampante specificato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

**EnumPrinterData** recupera i dati di configurazione della stampante impostati dalla funzione [**SetPrinterData**](setprinterdata.md) . I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipizzati. La funzione **EnumPrinterData** ottiene uno di questi valori, il nome e il codice del tipo, ogni volta che viene chiamato. Chiamare la funzione **EnumPrinterData** più volte in successione per ottenere tutti i valori dei dati di configurazione di una stampante.

I dati di configurazione della stampante vengono archiviati nel registro di sistema. Durante l'enumerazione dei dati di configurazione della stampante, è consigliabile evitare di chiamare le funzioni del registro di sistema che potrebbero modificare i dati.

Se si vuole che il sistema operativo fornisca una dimensione del buffer adeguata, chiamare prima **EnumPrinterData** con i parametri *cbValueName* e *cbData* impostati su zero, come indicato in precedenza nella sezione Parameters. Il valore di *dwIndex* non è rilevante per questa chiamata. Quando la funzione restituisce, \* *pcbValueName* e \* *pcbData* conterranno dimensioni del buffer sufficientemente grandi da poter enumerare tutti i valori e i nomi dei valori dei dati di configurazione della stampante. Alla chiamata successiva, allocare il nome del valore e i buffer di dati, impostare *cbValueName* e *cbData* sulle dimensioni in byte dei buffer allocati e impostare *dwIndex* su zero. Successivamente, continuare a chiamare la funzione **EnumPrinterData** , incrementando di uno ogni volta *dwIndex* , fino a quando la funzione non restituisce un errore di \_ \_ altri \_ elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrinterDataW** (Unicode) e **EnumPrinterDataA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterData**](deleteprinterdata.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 


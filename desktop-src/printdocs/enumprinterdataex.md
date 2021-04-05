---
description: La funzione EnumPrinterDataEx enumera tutti i nomi e i dati dei valori per una stampante e una chiave specificate.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Funzione EnumPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757853"
---
# <a name="enumprinterdataex-function"></a>EnumPrinterDataEx (funzione)

La funzione **EnumPrinterDataEx** enumera tutti i nomi e i dati dei valori per una stampante e una chiave specificate.

I dati della stampante vengono archiviati nel registro di sistema. Durante l'enumerazione dei dati della stampante, non chiamare le funzioni del registro di sistema che potrebbero modificare i dati.

## <a name="syntax"></a>Sintassi


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante per il quale la funzione recupera i dati di configurazione. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pKeyName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica la chiave che contiene i valori da enumerare. Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi. **EnumPrinterDataEx** enumera tutti i valori della chiave, ma non enumera i valori delle sottochiavi della chiave specificata. Utilizzare la funzione [**EnumPrinterKey**](enumprinterkey.md) per enumerare le sottochiavi.

Se *pKeyName* è **null** o una stringa vuota, **EnumPrinterDataEx** restituisce l' \_ errore \_ parametro non valido.

</dd> <dt>

*pEnumValues* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture [**di \_ \_ valori enum della stampante**](printer-enum-values.md) . Ogni struttura contiene il nome del valore, il tipo, i dati e le dimensioni di un valore sotto la chiave.

</dd> <dt>

*cbEnumValues* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pcbEnumValues*. Se si imposta *cbEnumValues* su zero, il parametro *pcbEnumValues* restituisce le dimensioni del buffer richieste.

</dd> <dt>

*pcbEnumValues* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di configurazione recuperati. Se la dimensione del buffer specificata da *cbEnumValues* è troppo piccola, la funzione restituisce l'errore di \_ altri \_ dati e *pcbEnumValues* indica le dimensioni del buffer richieste.

</dd> <dt>

*pnEnumValues* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture [**di \_ \_ valori enum della stampante**](printer-enum-values.md) restituite in *pEnumValues*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

**EnumPrinterDataEx** recupera i dati di configurazione della stampante impostati dalle funzioni [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData**](setprinterdata.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrinterDataExW** (Unicode) e **EnumPrinterDataExA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_valori enum della stampante \_**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 





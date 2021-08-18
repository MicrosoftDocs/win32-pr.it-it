---
description: La funzione EnumPrinterDataEx enumera tutti i nomi di valore e i dati per una stampante e una chiave specificate.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Funzione EnumPrinterDataEx (Winspool.h)
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
ms.openlocfilehash: c1e78c17cccf416d186c4669e3576c5a0c9bf2365cb048a73b42d583b187156f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034269"
---
# <a name="enumprinterdataex-function"></a>Funzione EnumPrinterDataEx

La **funzione EnumPrinterDataEx** enumera tutti i nomi di valore e i dati per una stampante e una chiave specificate.

I dati della stampante vengono archiviati nel Registro di sistema. Durante l'enumerazione dei dati della stampante, non chiamare le funzioni del Registro di sistema che potrebbero modificare i dati.

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per cui la funzione recupera i dati di configurazione. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pKeyName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica la chiave contenente i valori da enumerare. Usare la barra rovesciata ( ) come delimitatore per specificare un \\ percorso con una o più sottochiavi. **EnumPrinterDataEx** enumera tutti i valori della chiave, ma non enumera i valori delle sottochiavi della chiave specificata. Usare la [**funzione EnumPrinterKey**](enumprinterkey.md) per enumerare le sottochiavi.

Se *pKeyName* è **NULL** o una stringa vuota, **EnumPrinterDataEx** restituisce ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*pEnumValues* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di [**strutture PRINTER \_ ENUM \_ VALUES.**](printer-enum-values.md) Ogni struttura contiene il nome del valore, il tipo, i dati e le dimensioni di un valore sotto la chiave.

</dd> <dt>

*cbEnumValues* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pcbEnumValues*. Se si imposta *cbEnumValues* su zero, il *parametro pcbEnumValues* restituisce le dimensioni del buffer richieste.

</dd> <dt>

*valori pcbEnumValues* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di configurazione recuperati. Se le dimensioni del buffer specificate da *cbEnumValues* sono troppo piccole, la funzione restituisce ERROR MORE DATA e \_ \_ *pcbEnumValues* indica le dimensioni del buffer richieste.

</dd> <dt>

*pnEnumValues* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di [**strutture PRINTER \_ ENUM \_ VALUES**](printer-enum-values.md) restituite in *pEnumValues.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

**EnumPrinterDataEx recupera** i dati di configurazione della stampante impostati dalle [**funzioni SetPrinterDataEx**](setprinterdataex.md) [**e SetPrinterData.**](setprinterdata.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrinterDataExW** (Unicode) ed **EnumPrinterDataExA** (ANSI)<br/>                             |



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

[**VALORI \_ DI ENUMERAZIONE \_ PRINTER**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 





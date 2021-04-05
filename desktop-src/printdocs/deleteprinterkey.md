---
description: La funzione DeletePrinterKey Elimina una chiave specificata e tutte le relative sottochiavi per una stampante specificata.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: Funzione DeletePrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757748"
---
# <a name="deleteprinterkey-function"></a>DeletePrinterKey (funzione)

La funzione **DeletePrinterKey** Elimina una chiave specificata e tutte le relative sottochiavi per una stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante per il quale la funzione Elimina una chiave. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pKeyName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica la chiave da eliminare. Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi.

Se *pKeyName* è una stringa vuota (""), **DeletePrinterKey** Elimina tutte le chiavi sotto la chiave di primo livello per la stampante. Se *pKeyName* è **null**, **DeletePrinterKey** restituisce l' \_ errore \_ parametro non valido.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **DeletePrinterKeyW** (Unicode) e **DeletePrinterKeyA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 





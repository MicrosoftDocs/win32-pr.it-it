---
description: La funzione EnumPrinterKey enumera le sottochiavi di una chiave specificata per una stampante specificata.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Funzione EnumPrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347496"
---
# <a name="enumprinterkey-function"></a>EnumPrinterKey (funzione)

La funzione **EnumPrinterKey** enumera le sottochiavi di una chiave specificata per una stampante specificata.

I dati della stampante vengono archiviati nel registro di sistema. Durante l'enumerazione dei dati della stampante, non chiamare le funzioni del registro di sistema che potrebbero modificare i dati.

## <a name="syntax"></a>Sintassi


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante per il quale la funzione enumera le sottochiavi. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pKeyName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica la chiave contenente le sottochiavi da enumerare. Usare il carattere barra rovesciata ' \\ ' come delimitatore per specificare un percorso con una o più sottochiavi. **EnumPrinterKey** enumera tutte le sottochiavi della chiave, ma non enumera le sottochiavi di tali sottochiavi.

Se *pKeyName* è una stringa vuota (""), **EnumPrinterKey** enumera la chiave di primo livello per la stampante. Se *pKeyName* è **null**, **EnumPrinterKey** restituisce l' \_ errore \_ parametro non valido.

</dd> <dt>

*pSubkey* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di nomi di sottochiavi con terminazione null. La matrice viene terminata da due caratteri null.

</dd> <dt>

*cbSubkey* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pSubkey*. Se si imposta *cbSubkey* su zero, il parametro *pcbSubkey* restituisce le dimensioni del buffer richieste.

</dd> <dt>

*pcbSubkey* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte recuperati nel buffer di *pSubkey* . Se la dimensione del buffer specificata da *cbSubkey* è troppo piccola, la funzione restituisce l'errore di \_ altri \_ dati e *pcbSubkey* indica le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema. Se *pKeyName* non esiste, il valore restituito è errore \_ file \_ non \_ trovato.

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
| Nomi Unicode e ANSI<br/>   | **EnumPrinterKeyW** (Unicode) e **EnumPrinterKeyA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 





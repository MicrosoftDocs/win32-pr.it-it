---
description: La funzione EnumPrinterKey enumera le sottochiavi di una chiave specificata per una stampante specificata.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Funzione EnumPrinterKey (Winspool.h)
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
ms.openlocfilehash: c3666cce36884a331085d074df44e05b5bcfd0422433ce24bdbf3dbc385d7f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471785"
---
# <a name="enumprinterkey-function"></a>Funzione EnumPrinterKey

La **funzione EnumPrinterKey** enumera le sottochiavi di una chiave specificata per una stampante specificata.

I dati della stampante vengono archiviati nel Registro di sistema. Durante l'enumerazione dei dati della stampante, non chiamare le funzioni del Registro di sistema che potrebbero modificare i dati.

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per cui la funzione enumera le sottochiavi. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pKeyName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica la chiave contenente le sottochiavi da enumerare. Usare il carattere barra rovesciata ' ' come delimitatore per specificare un \\ percorso con una o più sottochiavi. **EnumPrinterKey** enumera tutte le sottochiavi della chiave, ma non le sottochiavi di tali sottochiavi.

Se *pKeyName* è una stringa vuota (""), **EnumPrinterKey** enumera la chiave di primo livello per la stampante. Se *pKeyName* è **NULL,** **EnumPrinterKey** restituisce ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*pSubkey* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di nomi di sottochiavi con terminazione Null. La matrice termina con due caratteri Null.

</dd> <dt>

*cbSubkey* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pSubkey*. Se si imposta *cbSubkey* su zero, il *parametro pcbSubkey* restituisce le dimensioni del buffer richieste.

</dd> <dt>

*pcbSubkey* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte recuperati nel buffer *pSubkey.* Se le dimensioni del buffer specificate da *cbSubkey* sono troppo piccole, la funzione restituisce ERROR MORE DATA e \_ \_ *pcbSubkey* indica le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema. Se *pKeyName* non esiste, il valore restituito è ERROR \_ FILE NOT \_ \_ FOUND.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrinterKeyW** (Unicode) ed **EnumPrinterKeyA** (ANSI)<br/>                                   |



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

 

 





---
description: La funzione DeletePrinterDataEx elimina un valore specificato dai dati di configurazione per una stampante.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: Funzione DeletePrinterDataEx (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7a47b3a7a62ac9dd48a86a7ddf4d6634304a402b69d5dc191ce17e3f149ffb27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950071"
---
# <a name="deleteprinterdataex-function"></a>Funzione DeletePrinterDataEx

La **funzione DeletePrinterDataEx** elimina un valore specificato dai dati di configurazione per una stampante. I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipidati archiviati in una gerarchia di chiavi del Registro di sistema. La funzione elimina un valore specificato in una chiave specificata.

Analogamente alla [**funzione DeletePrinterData,**](deleteprinterdata.md) **DeletePrinterDataEx** può eliminare i valori archiviati dalla [**funzione SetPrinterData.**](setprinterdata.md) Inoltre, **DeletePrinterDataEx** può eliminare i valori archiviati in una chiave specificata dalla [**funzione SetPrinterDataEx.**](setprinterdataex.md)

## <a name="syntax"></a>Sintassi


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per cui la funzione elimina un valore. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pKeyName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica la chiave contenente il valore da eliminare. Usare la barra rovesciata ( ) come delimitatore per specificare un percorso con \\ una o più sottochiavi.

Se *pKeyName* è **NULL** o una stringa vuota, **DeletePrinterDataEx restituisce** ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*pValueName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del valore da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **DeletePrinterDataExW** (Unicode) e **DeletePrinterDataExA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterKey**](deleteprinterkey.md)
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

 

 





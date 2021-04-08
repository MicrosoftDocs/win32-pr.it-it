---
description: La funzione GetSpoolFileHandle recupera un handle per il file di spooling associato al processo attualmente inviato dall'applicazione.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Funzione GetSpoolFileHandle (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058244"
---
# <a name="getspoolfilehandle-function"></a>GetSpoolFileHandle (funzione)

La funzione **GetSpoolFileHandle** recupera un handle per il file di spooling associato al processo attualmente inviato dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante a cui è stato inviato il processo. Deve corrispondere allo stesso handle utilizzato per inviare il processo. Usare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un handle per il file di spooling.

Se la funzione ha esito negativo, restituisce un **\_ \_ valore di handle non valido**.

## <a name="remarks"></a>Commenti

Con l'handle per il file di spooling, l'applicazione può scrivere nel file spool con le chiamate a [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguito da [**CommitSpoolData**](commitspooldata.md).

L'applicazione non deve chiamare [**ClosePrinter**](closeprinter.md) su *hPrinter* fino a quando non ha eseguito l'accesso al file di spooling per l'ultima volta. Deve quindi chiamare [**CloseSpoolFileHandle**](closespoolfilehandle.md) seguito da **ClosePrinter**. I tentativi di accesso all'handle di file di spooling dopo la chiusura del *hPrinter* originale avranno esito negativo anche se l'handle di file non è stato chiuso. Se **ClosePrinter** viene chiamato per primo, **CloseSpoolFileHandle** avrà esito negativo.

Questa funzione avrà esito negativo se viene chiamata prima del completamento dello spooling del processo di stampa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetSpoolFileHandleW** (Unicode) e **GetSpoolFileHandleA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> <dt>

[**CommitSpoolData**](commitspooldata.md)
</dt> </dl>

 


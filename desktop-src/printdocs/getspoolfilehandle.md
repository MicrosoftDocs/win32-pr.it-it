---
description: La funzione GetSpoolFileHandle recupera un handle per il file di spooling associato al processo attualmente inviato dall'applicazione.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Funzione GetSpoolFileHandle (Winspool.h)
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
ms.openlocfilehash: 10b0b36333e51dfb5c831f6c74e00c6930ccbb9d1ce31646fed0d689abc7f639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686694"
---
# <a name="getspoolfilehandle-function"></a>Funzione GetSpoolFileHandle

La **funzione GetSpoolFileHandle** recupera un handle per il file di spooling associato al processo attualmente inviato dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante a cui è stato inviato il processo. Deve essere lo stesso handle usato per inviare il processo. Usare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un handle al file di spooling.

Se la funzione ha esito negativo, restituisce **INVALID \_ HANDLE \_ VALUE**.

## <a name="remarks"></a>Commenti

Con l'handle per il file di spooling, l'applicazione può scrivere nel file di spooling con chiamate a [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguite [**da CommitSpoolData**](commitspooldata.md).

L'applicazione non deve chiamare [**ClosePrinter**](closeprinter.md) su *hPrinter* fino a quando non ha eseguito l'accesso al file di spooling per l'ultima volta. Dovrebbe quindi chiamare [**CloseSpoolFileHandle**](closespoolfilehandle.md) seguito da **ClosePrinter.** I tentativi di accesso all'handle di file di spooling dopo la chiusura *dell'hPrinter* originale avranno esito negativo anche se l'handle di file stesso non è stato chiuso. **CloseSpoolFileHandle avrà** a sua volta esito negativo **se ClosePrinter** viene chiamato per primo.

Questa funzione avrà esito negativo se viene chiamata prima del termine dello spooling del processo di stampa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetSpoolFileHandleW** (Unicode) e **GetSpoolFileHandleA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> <dt>

[**CommitSpoolData**](commitspooldata.md)
</dt> </dl>

 


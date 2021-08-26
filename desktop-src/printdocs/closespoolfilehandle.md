---
description: La funzione CloseSpoolFileHandle chiude un handle a un file di spooling associato al processo di stampa attualmente inviato dall'applicazione.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Funzione CloseSpoolFileHandle (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: f62173747472820f1642578778b67f3cdc3403523d6ae28453888dae3d6d1a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950531"
---
# <a name="closespoolfilehandle-function"></a>Funzione CloseSpoolFileHandle

La **funzione CloseSpoolFileHandle** chiude un handle a un file di spooling associato al processo di stampa attualmente inviato dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante a cui è stato inviato il processo. Deve essere lo stesso handle usato per ottenere *hSpoolFile* con [**GetSpoolFileHandle.**](getspoolfilehandle.md)

</dd> <dt>

*hSpoolFile* \[ Pollici\]
</dt> <dd>

Handle per il file di spooling da chiudere. Se [**CommitSpoolData**](commitspooldata.md) non è stato chiamato dopo la chiamata a [**GetSpoolFileHandle,**](getspoolfilehandle.md) questo deve essere lo stesso handle restituito da **GetSpoolFileHandle.** In caso contrario, deve essere l'handle restituito dalla chiamata più recente a **CommitSpoolData.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TRUE,** se ha esito positivo, **FALSE in caso** contrario.

## <a name="remarks"></a>Commenti

L'applicazione non deve chiamare [**ClosePrinter**](closeprinter.md) su *hPrinter* fino a quando non ha eseguito l'accesso al file di spooling per l'ultima volta. Dovrebbe quindi chiamare **CloseSpoolFileHandle** seguito da **ClosePrinter.** I tentativi di accesso all'handle di file di spooling dopo la chiusura *dell'hPrinter* originale avranno esito negativo anche se l'handle di file stesso non è stato chiuso. **CloseSpoolFileHandle avrà** esito negativo se **ClosePrinter viene** chiamato per primo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> </dl>

 

 





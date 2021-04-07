---
description: La funzione CommitSpoolData notifica allo spooler di stampa che una quantità specificata di dati è stata scritta in un file di spool specificato ed è pronta per essere sottoposta a rendering.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Funzione CommitSpoolData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881405"
---
# <a name="commitspooldata-function"></a>CommitSpoolData (funzione)

La funzione **CommitSpoolData** notifica allo spooler di stampa che una quantità specificata di dati è stata scritta in un file di spool specificato ed è pronta per essere sottoposta a rendering.

## <a name="syntax"></a>Sintassi


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante a cui è stato inviato il processo. Deve corrispondere allo stesso handle usato per ottenere *hSpoolFile* con [**GetSpoolFileHandle**](getspoolfilehandle.md).

</dd> <dt>

*hSpoolFile* \[ in\]
</dt> <dd>

Handle per il file di spooling modificato. Alla prima chiamata di **CommitSpoolData**, deve essere lo stesso handle restituito da [**GetSpoolFileHandle**](getspoolfilehandle.md). Le chiamate successive a **CommitSpoolData** devono passare l'handle restituito dalla chiamata precedente. Vedere la sezione Osservazioni.

</dd> <dt>

*cbCommit* 
</dt> <dd>

Numero di byte di cui è stato eseguito il commit nello spooler di stampa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un handle per il file di spooling.

Se la funzione ha esito negativo, restituisce un valore di handle non valido \_ \_ .

## <a name="remarks"></a>Commenti

Le applicazioni che inviano un processo di stampa spooler possono chiamare [**GetSpoolFileHandle**](getspoolfilehandle.md) e quindi scrivere direttamente i dati nell'handle di file spool chiamando [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Per notificare allo spooler di stampa che il file contiene dati di cui è possibile eseguire il rendering, l'applicazione deve chiamare **CommitSpoolData** e specificare il numero di byte disponibili.

Se **CommitSpoolData** viene chiamato più volte, ogni chiamata deve usare l'handle di file di spool restituito dalla chiamata precedente. Quando non vengono scritti più dati nel file di spooling, è necessario chiamare [**CloseSpoolFileHandle**](closespoolfilehandle.md) per l'handle di file restituito dall'ultima chiamata a **CommitSpoolData**.

Prima di chiamare **CommitSpoolData**, le applicazioni devono impostare il puntatore del file sulla posizione in cui si trovava prima di scrivere i dati nel file. Nel processo di rendering dei dati nel file dello spooler, lo spooler di stampa sposterà il puntatore del file di spool *cbCommit* byte dal valore corrente del puntatore del file.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> </dl>

 


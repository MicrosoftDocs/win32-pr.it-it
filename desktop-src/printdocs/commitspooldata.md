---
description: La funzione CommitSpoolData notifica al spooler di stampa che una quantità specificata di dati è stata scritta in un file di spooling specificato ed è pronta per il rendering.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Funzione CommitSpoolData (Winspool.h)
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
ms.openlocfilehash: 90c5907f86f7586710e8a65e60874587491674f2dc4d73d0632279f8b1b3c119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950501"
---
# <a name="commitspooldata-function"></a>Funzione CommitSpoolData

La **funzione CommitSpoolData** notifica al spooler di stampa che una quantità specificata di dati è stata scritta in un file di spooling specificato ed è pronta per il rendering.

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante a cui è stato inviato il processo. Deve essere lo stesso handle usato per ottenere *hSpoolFile* con [**GetSpoolFileHandle.**](getspoolfilehandle.md)

</dd> <dt>

*hSpoolFile* \[ Pollici\]
</dt> <dd>

Handle per il file di spooling da modificare. Alla prima chiamata di **CommitSpoolData** deve essere lo stesso handle restituito da [**GetSpoolFileHandle.**](getspoolfilehandle.md) Le chiamate successive **a CommitSpoolData** devono passare l'handle restituito dalla chiamata precedente. Vedere la sezione Osservazioni.

</dd> <dt>

*cbCommit* 
</dt> <dd>

Numero di byte di cui è stato eseguito il commit per lo spooler di stampa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un handle al file di spooling.

Se la funzione ha esito negativo, restituisce INVALID \_ HANDLE \_ VALUE.

## <a name="remarks"></a>Commenti

Le applicazioni che inviano un processo di stampa dello spooler possono chiamare [**GetSpoolFileHandle**](getspoolfilehandle.md) e quindi scrivere direttamente i dati nell'handle del file di spooling chiamando [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Per notificare al spooler di stampa che il file contiene dati pronti per il rendering, l'applicazione deve chiamare **CommitSpoolData** e specificare il numero di byte disponibili.

Se **CommitSpoolData viene** chiamato più volte, ogni chiamata deve usare l'handle del file di spooling restituito dalla chiamata precedente. Quando non verranno scritti altri dati nel file di spooling, è necessario chiamare [**CloseSpoolFileHandle**](closespoolfilehandle.md) per l'handle di file restituito dall'ultima chiamata a **CommitSpoolData.**

Prima di **chiamare CommitSpoolData,** le applicazioni devono impostare il puntatore del file sulla posizione in cui si trova prima di scrivere i dati nel file. Durante il rendering dei dati nel file spooler, lo spooler di stampa sposterà il puntatore del file di spooling *cbCommit* bytes dal valore corrente del puntatore del file.

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

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> </dl>

 


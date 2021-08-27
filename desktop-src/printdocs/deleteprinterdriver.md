---
description: La funzione DeletePrinterDriver rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Funzione DeletePrinterDriver (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d878bb848eebed7eaccd904d4cdfd035d5056ee32eaa67eac5064dd5cf4e1e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060031"
---
# <a name="deleteprinterdriver-function"></a>Funzione DeletePrinterDriver

La **funzione DeletePrinterDriver** rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server.

Per eliminare i file associati al driver oltre a rimuovere il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati per un server, usare la [**funzione DeletePrinterDriverEx.**](deleteprinterdriverex.md)

**DeletePrinterDriver** elimina un driver solo se non è in uso alcuna versione del driver per l'ambiente specificato. [**DeletePrinterDriverEx**](deleteprinterdriverex.md) può eliminare versioni specifiche del driver.

## <a name="syntax"></a>Sintassi


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server da cui deve essere eliminato il driver. Se questo parametro è **NULL,** il nome del driver della stampante verrà rimosso in locale.

</dd> <dt>

*pEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente da cui deve essere eliminato il driver, ad esempio Windows x86, Windows IA64 o Windows x64). Se questo parametro è **NULL,** il nome del driver viene eliminato dall'ambiente corrente dell'applicazione chiamante e del computer client (non dell'applicazione di destinazione e del server di stampa).

</dd> <dt>

*pDriverName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del driver da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

La **funzione DeletePrinterDriver** non elimina i file associati, ma semplicemente rimuove il nome del driver dall'elenco restituito dalla [**funzione EnumPrinterDrivers.**](enumprinterdrivers.md)

Prima di **chiamare DeletePrinterDriver**, è necessario eliminare tutti gli oggetti stampante che usano il driver della stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **DeletePrinterDriverW** (Unicode) e **DeletePrinterDriverA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 


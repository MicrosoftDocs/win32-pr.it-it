---
description: La funzione DeletePrinterDriver rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Funzione DeletePrinterDriver (winspool. h)
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
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311549"
---
# <a name="deleteprinterdriver-function"></a>DeletePrinterDriver (funzione)

La funzione **DeletePrinterDriver** rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server.

Per eliminare i file associati al driver, oltre a rimuovere il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati per un server, utilizzare la funzione [**DeletePrinterDriverEx**](deleteprinterdriverex.md) .

**DeletePrinterDriver** Elimina un driver solo se non è in uso alcuna versione del driver per l'ambiente specificato. [**DeletePrinterDriverEx**](deleteprinterdriverex.md) può eliminare versioni specifiche del driver.

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

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server da cui deve essere eliminato il driver. Se questo parametro è **null**, il nome del driver della stampante verrà rimosso localmente.

</dd> <dt>

*pEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente da cui deve essere eliminato il driver (ad esempio, Windows x86, Windows IA64 o Windows x64). Se questo parametro è **null**, il nome del driver viene eliminato dall'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.

</dd> <dt>

*pDriverName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del driver da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

La funzione **DeletePrinterDriver** non elimina i file associati, ma rimuove semplicemente il nome del driver dall'elenco restituito dalla funzione [**EnumPrinterDrivers**](enumprinterdrivers.md) .

Prima di chiamare **DeletePrinterDriver**, è necessario eliminare tutti gli oggetti stampante che usano il driver della stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

 


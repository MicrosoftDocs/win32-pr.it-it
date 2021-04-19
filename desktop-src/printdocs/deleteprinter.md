---
description: La funzione DeletePrinter Elimina l'oggetto stampante specificato.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Funzione DeletePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311552"
---
# <a name="deleteprinter-function"></a>DeletePrinter (funzione)

La funzione **DeletePrinter** Elimina l'oggetto stampante specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in uscita\]
</dt> <dd>

Handle per un oggetto Printer che verrà eliminato. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Se sono presenti processi di stampa rimanenti da elaborare per la stampante specificata, **DeletePrinter** contrassegna la stampante per l'eliminazione in sospeso e quindi la Elimina al termine della stampa di tutti i processi di stampa. Non è possibile aggiungere processi di stampa a una stampante contrassegnata per l'eliminazione in sospeso.

Una stampante contrassegnata per l'eliminazione in sospeso non può essere mantenuta, ma i processi di stampa possono essere conservati, ripresi e riavviati. Se la stampante viene mantenuta e sono presenti processi per la stampante, **DeletePrinter** ha esito negativo e viene \_ negato l'accesso agli errori \_ .

Si noti che **DeletePrinter** non chiude l'handle che lo viene passato. Pertanto, l'applicazione deve comunque chiamare [**ClosePrinter**](closeprinter.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 





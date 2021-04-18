---
description: La funzione ResetPrinter specifica il tipo di dati e i valori della modalità dispositivo da usare per la stampa dei documenti inviati dalla funzione StartDocPrinter. È possibile eseguire l'override di questi valori utilizzando la funzione SetJob dopo l'avvio della stampa del documento.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Funzione ResetPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312569"
---
# <a name="resetprinter-function"></a>ResetPrinter (funzione)

La funzione **ResetPrinter** specifica il tipo di dati e i valori della modalità dispositivo da usare per la stampa dei documenti inviati dalla funzione [**StartDocPrinter**](startdocprinter.md) . È possibile eseguire l'override di questi valori utilizzando la funzione [**SetJob**](setjob.md) dopo l'avvio della stampa del documento.

## <a name="syntax"></a>Sintassi


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pDefault* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ impostazioni predefinite della stampante**](printer-defaults.md) .

La funzione **ResetPrinter** ignora il membro **desiredAccess** della struttura [**Printer \_ defaults**](printer-defaults.md) . Impostare il membro su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **ResetPrinterW** (Unicode) e **ResetPrinterA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_impostazioni predefinite stampanti**](printer-defaults.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 





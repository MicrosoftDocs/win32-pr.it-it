---
description: La funzione PrinterProperties Visualizza una finestra delle proprietà Printer-Properties per la stampante specificata.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: Funzione PrinterProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "106334303"
---
# <a name="printerproperties-function"></a>PrinterProperties (funzione)

La funzione **PrinterProperties** Visualizza una finestra delle proprietà Printer-Properties per la stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra padre della finestra delle proprietà.

</dd> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per un oggetto Printer. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

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
| DLL<br/>                      | <dl> <dt>winspool. drv</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DocumentProperties**](documentproperties.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 





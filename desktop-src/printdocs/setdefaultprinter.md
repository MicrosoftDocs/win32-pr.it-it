---
description: La funzione SetDefaultPrinter imposta il nome della stampante predefinita per l'utente corrente nel computer locale.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Funzione SetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314980"
---
# <a name="setdefaultprinter-function"></a>SetDefaultPrinter (funzione)

La funzione **SetDefaultPrinter** imposta il nome della stampante predefinita per l'utente corrente nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszPrinter* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome predefinito della stampante. Per una connessione a una stampante remota, il formato del nome è **\\\\** _Server_ *_\\_* _PrinterName_. Per una stampante locale, il formato del nome è *PrinterName*.

Se questo parametro è **null** o una stringa vuota, ovvero "", **SetDefaultPrinter** selezionerà una stampante predefinita da una delle stampanti installate. Se è già presente una stampante predefinita, la chiamata a **SetDefaultPrinter** con una stringa **null** o vuota in questo parametro potrebbe modificare la stampante predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Quando si utilizza questo metodo, è necessario specificare una stampante, un driver e una porta validi. Se non sono validi, le API non hanno esito negativo, ma il risultato non è definito. Questo potrebbe causare la reimpostazione della stampante da parte di altri programmi sulla stampante valida precedente. È possibile utilizzare [**EnumPrinters**](enumprinters.md) per recuperare il nome della stampante, il nome del driver e il nome della porta di tutte le stampanti disponibili.

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
| Nomi Unicode e ANSI<br/>   | **SetDefaultPrinterW** (Unicode) e **SetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetDefaultPrinter**](getdefaultprinter.md)
</dt> </dl>

 

 





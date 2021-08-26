---
description: La funzione SetDefaultPrinter imposta il nome della stampante predefinita per l'utente corrente nel computer locale.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Funzione SetDefaultPrinter (Winspool.h)
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
ms.openlocfilehash: 570e0d57c4a04cd4845883e825acfbbef0282186cc7289751737798ed52b9592
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112121"
---
# <a name="setdefaultprinter-function"></a>Funzione SetDefaultPrinter

La **funzione SetDefaultPrinter** imposta il nome della stampante predefinita per l'utente corrente nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszPrinter* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il nome predefinito della stampante. Per una connessione remota alla stampante, il formato del nome è **\\\\** _server_ *_\\_* _printername_. Per una stampante locale, il formato del nome è *printername*.

Se questo parametro è **NULL** o una stringa vuota, ad esempio "", **SetDefaultPrinter** selezionerà una stampante predefinita da una delle stampanti installate. Se esiste già una stampante predefinita, la chiamata di **SetDefaultPrinter** con **un valore NULL** o una stringa vuota in questo parametro potrebbe modificare la stampante predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Quando si utilizza questo metodo, è necessario specificare una stampante, un driver e una porta validi. Se non sono valide, le API non hanno esito negativo, ma il risultato non è definito. In questo modo altri programmi potrebbero impostare nuovamente la stampante sulla stampante valida precedente. È possibile usare [**EnumPrinters per**](enumprinters.md) recuperare il nome della stampante, il nome del driver e il nome della porta di tutte le stampanti disponibili.

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **SetDefaultPrinterW** (Unicode) e **SetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Enumprinters**](enumprinters.md)
</dt> <dt>

[**GetDefaultPrinter**](getdefaultprinter.md)
</dt> </dl>

 

 





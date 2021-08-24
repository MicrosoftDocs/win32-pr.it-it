---
description: La funzione GetDefaultPrinter recupera il nome della stampante predefinita per l'utente corrente nel computer locale.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Funzione GetDefaultPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 59d6ba435b592076455690916f5c627c73f65370df381861c25a6fafa21bf0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949101"
---
# <a name="getdefaultprinter-function"></a>Funzione GetDefaultPrinter

La **funzione GetDefaultPrinter** recupera il nome della stampante predefinita per l'utente corrente nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszBuffer* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che riceve una stringa di caratteri con terminazione Null contenente il nome predefinito della stampante. Se questo parametro è **NULL,** la funzione ha esito negativo e la variabile a cui *punta pcchBuffer* restituisce le dimensioni del buffer richieste, in caratteri.

</dd> <dt>

*pcchBuffer* \[ in, out\]
</dt> <dd>

Nell'input specifica le dimensioni, in caratteri, del buffer *pszBuffer.* Nell'output riceve le dimensioni, in caratteri, della stringa del nome della stampante, incluso il carattere Null di terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero e la variabile a cui punta *pcchBuffer* contiene il numero di caratteri copiati nel buffer *pszBuffer,* incluso il carattere Null di terminazione.

Se la funzione ha esito negativo, il valore restituito è zero.



| Valore                       | Significato                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ BUFFER \_ INSUFFICIENTE | Il buffer *pszBuffer* è troppo piccolo. La variabile a cui punta *pcchBuffer* contiene le dimensioni del buffer richieste, in caratteri. |
| FILE \_ DEGLI ERRORI NON \_ \_ TROVATO     | Non esiste alcuna stampante predefinita.                                                                                                   |



 

## <a name="remarks"></a>Commenti

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
| Nomi Unicode e ANSI<br/>   | **GetDefaultPrinterW** (Unicode) e **GetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**SetDefaultPrinter**](setdefaultprinter.md)
</dt> </dl>

 

 





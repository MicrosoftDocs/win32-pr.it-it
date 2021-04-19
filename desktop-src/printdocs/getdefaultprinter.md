---
description: La funzione GetDefaultPrinter Recupera il nome della stampante predefinita per l'utente corrente nel computer locale.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Funzione GetDefaultPrinter (winspool. h)
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
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311823"
---
# <a name="getdefaultprinter-function"></a>GetDefaultPrinter (funzione)

La funzione **GetDefaultPrinter** Recupera il nome della stampante predefinita per l'utente corrente nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszBuffer* \[ in\]
</dt> <dd>

Puntatore a un buffer che riceve una stringa di caratteri con terminazione null contenente il nome predefinito della stampante. Se questo parametro è **null**, la funzione ha esito negativo e la variabile a cui punta *pcchBuffer* restituisce le dimensioni del buffer richieste in caratteri.

</dd> <dt>

*pcchBuffer* \[ in uscita\]
</dt> <dd>

In input, specifica la dimensione, in caratteri, del buffer *pszBuffer* . Nell'output, riceve la dimensione, in caratteri, della stringa del nome della stampante, incluso il carattere null di terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero e la variabile a cui punta *pcchBuffer* contiene il numero di caratteri copiati nel buffer *pszBuffer* , incluso il carattere null di terminazione.

Se la funzione ha esito negativo, il valore restituito è zero.



| Valore                       | Significato                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ buffer insufficiente \_ | Il buffer *pszBuffer* è troppo piccolo. La variabile a cui punta *pcchBuffer* contiene le dimensioni del buffer richieste, in caratteri. |
| FILE di errore \_ \_ non \_ trovato     | Non è presente alcuna stampante predefinita.                                                                                                   |



 

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
| Nomi Unicode e ANSI<br/>   | **GetDefaultPrinterW** (Unicode) e **GetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**SetDefaultPrinter**](setdefaultprinter.md)
</dt> </dl>

 

 





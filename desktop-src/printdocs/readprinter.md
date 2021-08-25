---
description: La funzione ReadPrinter recupera i dati dalla stampante specificata.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: Funzione ReadPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 63683e421441fb15ec299f3077088bd8f9cffb65644550be912ee39b5c530371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824021"
---
# <a name="readprinter-function"></a>Funzione ReadPrinter

La **funzione ReadPrinter** recupera i dati dalla stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto stampante per il quale recuperare i dati. Usare la [**funzione OpenPrinter**](openprinter.md) per recuperare l'handle di un oggetto stampante. Usare il formato: Printername, Job xxxx.

</dd> <dt>

*pBuf* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve i dati della stampante.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui *punta pBuf.*

</dd> <dt>

*pNoBytesRead* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte di dati copiati nella matrice a cui *punta pBuf.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

**ReadPrinter** restituisce un errore se il dispositivo o la stampante non è bidirezionale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 





---
description: La funzione FlushPrinter invia un buffer alla stampante per cancellarlo da uno stato temporaneo.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Funzione FlushPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 78bd5b6ccc86651a717c29db8b938508c857f83dbd3bdf5364fb1596b8a2c956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949301"
---
# <a name="flushprinter-function"></a>Funzione FlushPrinter

La **funzione FlushPrinter** invia un buffer alla stampante per cancellarlo da uno stato temporaneo.

## <a name="syntax"></a>Sintassi


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto stampante. Deve essere lo stesso handle usato, in una chiamata [**WritePrinter**](writeprinter.md) precedente, dal driver della stampante.

</dd> <dt>

*pBuf* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di byte contenente i dati da scrivere nella stampante.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, della matrice a cui punta *pBuf*.

</dd> <dt>

*pcWritten* \[ Cambio\]
</dt> <dd>

Puntatore a un valore che riceve il numero di byte di dati scritti nella stampante.

</dd> <dt>

*cSleep* \[ Pollici\]
</dt> <dd>

Tempo, in millisecondi, durante il quale la riga di I/O sulla porta della stampante deve essere mantenuta inattiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

**FlushPrinter** deve essere chiamato solo in caso [**di errore di WritePrinter,**](writeprinter.md) lasciando la stampante in uno stato temporaneo. Ad esempio, la stampante potrebbe entrare in uno stato temporaneo quando il processo viene interrotto e il driver della stampante ha inviato parzialmente alcuni dati non elaborati alla stampante.

**FlushPrinter può** inoltre specificare un periodo di inattività durante il quale lo spooler di stampa non pianifica alcun processo sulla porta della stampante corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 





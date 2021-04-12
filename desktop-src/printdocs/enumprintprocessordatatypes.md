---
description: La funzione EnumPrintProcessorDatatypes enumera i tipi di dati supportati da un processore di stampa specificato.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Funzione EnumPrintProcessorDatatypes (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528999"
---
# <a name="enumprintprocessordatatypes-function"></a>EnumPrintProcessorDatatypes (funzione)

La funzione **EnumPrintProcessorDatatypes** enumera i tipi di dati supportati da un processore di stampa specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui risiede il processore di stampa. Se questo parametro è **null**, vengono enumerati i tipi di dati per il processore di stampa locale.

</dd> <dt>

*pPrintProcessorName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del processore di stampa i cui tipi di dati sono enumerati.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Tipo di informazioni restituite nel buffer di *pDatatypes* . Questo parametro deve essere 1.

</dd> <dt>

*pDatatypes* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture di [**tipo \_ info \_ 1**](datatypes-info-1.md) . Ogni struttura descrive un tipo di dati disponibile. Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa o altri dati a cui fanno riferimento i membri della struttura.

Per determinare le dimensioni del buffer richieste, chiamare **EnumPrintProcessorDatatypes** con *cbBuf* impostato su zero. **EnumPrintProcessorDatatypes** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pDatatypes*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte copiati nel buffer *pDatatypes* se la funzione ha esito positivo. Se il buffer è troppo piccolo, la funzione ha esito negativo e la variabile riceve il numero di byte necessari.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture restituite nel buffer di *pDatatypes* . Il numero dei tipi di dati supportati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

v

A partire da Windows Vista, le informazioni sul tipo di dati dei server di stampa remoti vengono recuperate da una cache locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrintProcessorDatatypesW** (Unicode) e **EnumPrintProcessorDatatypesA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**TIPI di \_ dati \_ 1**](datatypes-info-1.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 


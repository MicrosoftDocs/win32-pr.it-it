---
description: La funzione EnumPrintProcessors enumera i processori di stampa installati nel server specificato.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Funzione EnumPrintProcessors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967841"
---
# <a name="enumprintprocessors-function"></a>EnumPrintProcessors (funzione)

La funzione **EnumPrintProcessors** enumera i processori di stampa installati nel server specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui risiedono i processori di stampa. Se questo parametro è **null**, vengono enumerati i processori di stampa locali.

</dd> <dt>

*pEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64). Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Tipo di informazioni restituite nel buffer di *pPrintProcessorInfo* . Questo parametro deve essere 1.

</dd> <dt>

*pPrintProcessorInfo* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture [**PRINTPROCESSOR \_ info \_ 1**](printprocessor-info-1.md) . Ogni struttura descrive un processore di stampa disponibile. Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa a cui puntano i membri della struttura.

Per determinare le dimensioni del buffer richieste, chiamare **EnumPrintProcessors** con *cbBuf* impostato su zero. **EnumPrintProcessors** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pPrintProcessorInfo*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte copiati nel buffer *pPrintProcessorInfo* se la funzione ha esito positivo. Se il buffer è troppo piccolo, la funzione ha esito negativo e la variabile riceve il numero di byte necessari.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture restituite nel buffer di *pPrintProcessorInfo* .

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
| Nomi Unicode e ANSI<br/>   | **EnumPrintProcessorsW** (Unicode) e **EnumPrintProcessorsA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**PRINTPROCESSOR \_ info \_ 1**](printprocessor-info-1.md)
</dt> </dl>

 


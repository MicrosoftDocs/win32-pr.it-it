---
description: La funzione GetPrintProcessorDirectory Recupera il percorso della directory del processore di stampa nel server specificato.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Funzione GetPrintProcessorDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885181"
---
# <a name="getprintprocessordirectory-function"></a>GetPrintProcessorDirectory (funzione)

La funzione **GetPrintProcessorDirectory** Recupera il percorso della directory del processore di stampa nel server specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server. Se questo parametro è **null**, viene restituito un percorso locale.

</dd> <dt>

*pEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64). Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Livello della struttura. Questo valore deve essere 1.

</dd> <dt>

*pPrintProcessorInfo* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve il percorso. Si noti che, per i sistemi operativi precedenti a Windows Server 2003 SP 1, il percorso è nel formato locale per il server, non nel formato remoto vero e proprio. Ad esempio, il percorso viene specificato come "% windir% \\ system32 \\ spool \\ prtprocs \\ % Environment%" invece di " \\ \\ servername \\ Print $ \\ prtprocs \\ % Environment%", anche quando viene chiamato per un server remoto. Per i sistemi operativi Windows Server 2003 SP 1 e versioni successive, viene restituito il vero percorso remoto.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensioni del buffer a cui punta *pPrintProcessorInfo*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a un valore che specifica il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

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
| Nomi Unicode e ANSI<br/>   | **GetPrintProcessorDirectoryW** (Unicode) e **GetPrintProcessorDirectoryA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

 





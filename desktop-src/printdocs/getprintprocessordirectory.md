---
description: La funzione GetPrintProcessorDirectory recupera il percorso della directory del processore di stampa nel server specificato.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Funzione GetPrintProcessorDirectory (Winspool.h)
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
ms.openlocfilehash: 27e79305295d078912169a2a12a99aa516372486f9b5dcd1997161a030103dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719251"
---
# <a name="getprintprocessordirectory-function"></a>Funzione GetPrintProcessorDirectory

La **funzione GetPrintProcessorDirectory** recupera il percorso della directory del processore di stampa nel server specificato.

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

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server. Se questo parametro è **NULL,** viene restituito un percorso locale.

</dd> <dt>

*pEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente, ad esempio Windows x86, Windows IA64 o Windows x64). Se questo parametro è **NULL,** viene usato l'ambiente corrente dell'applicazione chiamante e del computer client (non dell'applicazione di destinazione e del server di stampa).

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Livello della struttura. Questo valore deve essere 1.

</dd> <dt>

*pPrintProcessorInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve il percorso. Si noti che, per i sistemi operativi precedenti Windows Server 2003 SP 1, il percorso è nel formato locale per il server, non nel formato remoto vero. Ad esempio, il percorso viene specificato come "%Windir% \\ System32 \\ Spool \\ Prtprocs \\ %Environment%" anziché \\ \\ "ServerName \\ Print$ \\ Prtprocs \\ %Environment%", anche quando viene chiamato per un server remoto. Per i sistemi operativi Windows Server 2003 SP 1 e versioni successive, viene restituito il percorso remoto vero.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione del buffer a cui punta *pPrintProcessorInfo.*

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a un valore che specifica il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetPrintProcessorDirectoryW** (Unicode) e **GetPrintProcessorDirectoryA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

 





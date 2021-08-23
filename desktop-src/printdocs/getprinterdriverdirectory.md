---
description: La funzione GetPrinterDriverDirectory recupera il percorso della directory printer-driver.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Funzione GetPrinterDriverDirectory (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 4822f2478313dc902062ff907df5af3f0f7a515f19e414d2bc1534cc991b1ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971360"
---
# <a name="getprinterdriverdirectory-function"></a>Funzione GetPrinterDriverDirectory

La **funzione GetPrinterDriverDirectory** recupera il percorso della directory printer-driver.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server in cui risiede il driver della stampante. Se questo parametro è **NULL,** viene recuperato il percorso della directory del driver locale.

</dd> <dt>

*pEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente,ad esempio Windows x86, Windows IA64 o Windows x64). Se questo parametro è **NULL,** viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client (non dell'applicazione di destinazione e del server di stampa).

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Livello della struttura. Questo valore deve essere 1.

</dd> <dt>

*pDriverDirectory* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve il percorso.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione del buffer a cui *punta pDriverDirectory.*

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
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetPrinterDriverDirectoryW** (Unicode) e **GetPrinterDriverDirectoryA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> </dl>

 

 





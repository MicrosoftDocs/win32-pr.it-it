---
description: La funzione GetPrinterDriverDirectory Recupera il percorso della directory del driver della stampante.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Funzione GetPrinterDriverDirectory (winspool. h)
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
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318381"
---
# <a name="getprinterdriverdirectory-function"></a>GetPrinterDriverDirectory (funzione)

La funzione **GetPrinterDriverDirectory** Recupera il percorso della directory del driver della stampante.

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

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui si trova il driver della stampante. Se questo parametro è **null**, viene recuperato il percorso della directory del driver locale.

</dd> <dt>

*pEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64). Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Livello della struttura. Questo valore deve essere 1.

</dd> <dt>

*pDriverDirectory* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve il percorso.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione del buffer a cui punta *pDriverDirectory* .

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
| Nomi Unicode e ANSI<br/>   | **GetPrinterDriverDirectoryW** (Unicode) e **GetPrinterDriverDirectoryA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> </dl>

 

 





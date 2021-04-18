---
description: La funzione GetPrinterDriver recupera i dati del driver per la stampante specificata. Se il driver non è installato nel computer locale, GetPrinterDriver lo installa.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Funzione GetPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318384"
---
# <a name="getprinterdriver-function"></a>GetPrinterDriver (funzione)

La funzione **GetPrinterDriver** recupera i dati del driver per la stampante specificata. Se il driver non è installato nel computer locale, **GetPrinterDriver** lo installa.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante per il quale devono essere recuperati i dati del driver. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64). Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Struttura del driver della stampante restituita nel buffer di *pDriverInfo* . Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                | Significato                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**\_Informazioni driver \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**\_Informazioni driver \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**\_Informazioni driver \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**\_Informazioni driver \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**\_Informazioni driver \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**\_Informazioni driver \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**\_Informazioni driver \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una struttura contenente informazioni sul driver, come specificato dal livello. Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui puntano i membri della struttura.

Per determinare le dimensioni del buffer richieste, chiamare **GetPrinterDriver** con *cbBuf* impostato su zero. **GetPrinterDriver** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, della matrice in corrispondenza della quale punta *pDriverInfo* .

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a un valore che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

Per un driver inesistente, la funzione restituisce l' \_ errore \_ driver della stampante sconosciuto \_ .

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Il driver info [**\_ \_ 2**](driver-info-2.md), [**driver \_ info \_ 3**](driver-info-3.md), [**driver \_ info \_ 4**](driver-info-4.md), [**driver \_ info \_ 5**](driver-info-5.md)e [**driver \_ info \_ 6**](driver-info-6.md) strutture contengono il nome file o il percorso completo e il nome file del driver della stampante nel membro **pDriverPath** . Un'applicazione può utilizzare il percorso e il nome file per caricare un driver della stampante chiamando la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e specificando il percorso e il nome del file come argomento singolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetPrinterDriverW** (Unicode) e **GetPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**\_Informazioni driver \_ 1**](driver-info-1.md)
</dt> <dt>

[**\_Informazioni driver \_ 2**](driver-info-2.md)
</dt> <dt>

[**\_Informazioni driver \_ 3**](driver-info-3.md)
</dt> <dt>

[**\_Informazioni driver \_ 4**](driver-info-4.md)
</dt> <dt>

[**\_Informazioni driver \_ 5**](driver-info-5.md)
</dt> <dt>

[**\_Informazioni driver \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 


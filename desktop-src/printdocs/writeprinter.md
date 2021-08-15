---
description: La funzione WritePrinter notifica lo spooler di stampa che i dati devono essere scritti nella stampante specificata.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Funzione WritePrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 4b8b413854f8634477f7fec9010f4306587a093bd5c791b1b7d0117b6c3ef91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971160"
---
# <a name="writeprinter-function"></a>Funzione WritePrinter

La **funzione WritePrinter** notifica lo spooler di stampa che i dati devono essere scritti nella stampante specificata.

> [!Note]  
> **WritePrinter** supporta solo la stampa GDI e non deve essere usato per la stampa XPS. Se il processo di stampa usa il percorso di stampa XPS o OpenXPS, usare [l'API di stampa XPS](/windows/desktop/printdocs/xps-printing). L'invio di processi di stampa XPS o OpenXPS nello spooler tramite **WritePrinter** non è supportato e può comportare risultati indeterminati.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pBuf* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di byte che contiene i dati che devono essere scritti nella stampante.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, della matrice.

</dd> <dt>

*pcWritten* \[ Cambio\]
</dt> <dd>

Puntatore a un valore che riceve il numero di byte di dati scritti nella stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

La sequenza per un processo di stampa è la seguente:

1.  Per iniziare un processo di stampa, [**chiamare StartDocPrinter**](startdocprinter.md).
2.  Per iniziare ogni pagina, chiamare [**StartPagePrinter**](startpageprinter.md).
3.  Per scrivere dati in una pagina, chiamare **WritePrinter**.
4.  Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).
5.  Ripetere 2, 3 e 4 per il numero di pagine necessario.
6.  Per terminare il processo di stampa, [**chiamare EndDocPrinter**](enddocprinter.md).

Quando un documento di alto livello (ad esempio un file Adobe PDF o Microsoft Word) o altri dati della stampante (ad esempio PCL, PS o HPGL) viene inviato direttamente a una stampante, le impostazioni di stampa definite nel documento hanno precedenti rispetto alle impostazioni di stampa Windows. L'output dei documenti quando il valore del membro *pDatatype* della struttura [**DOC INFO \_ \_ 1**](doc-info-1.md) passato nel *parametro pDocInfo* della chiamata [**StartDocPrinter**](startdocprinter.md) è "RAW" deve descrivere completamente le impostazioni del processo di stampa in stile [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)nella lingua compresa dall'hardware.

Nelle versioni di Windows precedenti Windows XP, quando una pagina in un file di spooling supera circa 350 MB, potrebbe non essere possibile stampare e non inviare un messaggio di errore. Ad esempio, ciò può verificarsi quando si stampano file EMF di grandi dimensioni. Il limite delle dimensioni della pagina nelle versioni di Windows precedenti Windows XP dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamanti e la quantità di frammentazione nell'heap del processo. In Windows XP e versioni successive di Windows, i file EMF devono avere dimensioni di 2 GB o inferiori. Se **WritePrinter** viene usato per scrivere dati non EMF, ad esempio PDL pronto per la stampante, le dimensioni del file sono limitate solo dallo spazio su disco disponibile.

## <a name="examples"></a>Esempio

Per un programma di esempio che usa questa funzione, vedere [Procedura: Stampare usando l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 


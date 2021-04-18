---
description: La funzione WritePrinter notifica allo spooler di stampa che i dati devono essere scritti nella stampante specificata.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Funzione WritePrinter (winspool. h)
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
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312568"
---
# <a name="writeprinter-function"></a>WritePrinter (funzione)

La funzione **WritePrinter** notifica allo spooler di stampa che i dati devono essere scritti nella stampante specificata.

> [!Note]  
> **WritePrinter** supporta solo la stampa GDI e non deve essere utilizzato per la stampa XPS. Se il processo di stampa usa il percorso di stampa XPS o OpenXPS, usare l' [API di stampa XPS](/windows/desktop/printdocs/xps-printing). L'invio di processi di stampa XPS o OpenXPS allo spooler mediante **WritePrinter** non è supportato e può causare risultati indeterminati.

 

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

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pbuf* \[ in\]
</dt> <dd>

Puntatore a una matrice di byte che contiene i dati che devono essere scritti sulla stampante.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, della matrice.

</dd> <dt>

*pcWritten* \[ out\]
</dt> <dd>

Puntatore a un valore che riceve il numero di byte di dati scritti nella stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

La sequenza per un processo di stampa è la seguente:

1.  Per iniziare un processo di stampa, chiamare [**StartDocPrinter**](startdocprinter.md).
2.  Per iniziare ogni pagina, chiamare [**StartPagePrinter**](startpageprinter.md).
3.  Per scrivere i dati in una pagina, chiamare **WritePrinter**.
4.  Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).
5.  Ripetere 2, 3 e 4 per il numero di pagine necessario.
6.  Per terminare il processo di stampa, chiamare [**EndDocPrinter**](enddocprinter.md).

Quando un documento di alto livello (ad esempio un file Adobe PDF o Microsoft Word) o altri dati della stampante (ad esempio, PCL, PS o HPGL) vengono inviati direttamente a una stampante, le impostazioni di stampa definite nel documento prendono le precedenti rispetto alle impostazioni di stampa di Windows. Documents output quando il valore del membro *pDatatype* della struttura [**doc \_ info \_ 1**](doc-info-1.md) passato nel parametro *pDocInfo* della chiamata [**StartDocPrinter**](startdocprinter.md) è "Raw" deve descrivere completamente le impostazioni del processo di stampa di tipo [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)nella lingua compresa nell'hardware.

Nelle versioni di Windows precedenti a Windows XP, quando una pagina in un file con spooling supera circa 350 MB, potrebbe non essere possibile stampare e inviare un messaggio di errore. Questo può verificarsi, ad esempio, durante la stampa di file EMF di grandi dimensioni. Il limite delle dimensioni della pagina nelle versioni di Windows precedenti a Windows XP dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamante e la quantità di frammentazione nell'heap dei processi. In Windows XP e versioni successive di Windows, i file EMF devono avere una dimensione di 2 GB o minore. Se **WritePrinter** viene usato per scrivere dati non EMF, ad esempio il PDL pronto per la stampa, le dimensioni del file sono limitate solo dallo spazio disponibile su disco.

## <a name="examples"></a>Esempio

Per un programma di esempio che usa questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
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

 


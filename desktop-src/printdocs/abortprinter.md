---
description: La funzione AbortPrinter elimina un file di spooling delle stampanti se la stampante è configurata per lo spooling.
ms.assetid: b361fba5-e4e7-4c9e-ab32-b8ab88dcb1dc
title: Funzione AbortPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbortPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c4d3bd7af58c0c927d01fad734ad58f59941815b1680e730f2569efcc6c00b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951031"
---
# <a name="abortprinter-function"></a>Funzione AbortPrinter

La **funzione AbortPrinter** elimina il file di spooling di una stampante se la stampante è configurata per lo spooling.

## <a name="syntax"></a>Sintassi


```C++
BOOL AbortPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante da cui viene eliminato il file di spooling. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Se la stampante non è configurata per lo spooling, la **funzione AbortPrinter** non ha alcun effetto.

La sequenza per un processo di stampa è la seguente:

1.  Per avviare un processo di stampa, [**chiamare StartDocPrinter**](startdocprinter.md).
2.  Per iniziare ogni pagina, chiamare [**StartPagePrinter**](startpageprinter.md).
3.  Per scrivere dati in una pagina, chiamare [**WritePrinter**](writeprinter.md).
4.  Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).
5.  Ripetere 2, 3 e 4 per tutte le pagine necessarie.
6.  Per terminare il processo di stampa, [**chiamare EndDocPrinter**](enddocprinter.md).

Quando una pagina in un file di spooling supera circa 350 MB, può non riuscire a stampare e non inviare un messaggio di errore. Ad esempio, ciò può verificarsi quando si stampano file EMF di grandi dimensioni. Il limite delle dimensioni della pagina dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamanti e la quantità di frammentazione nell'heap del processo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
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

 

 





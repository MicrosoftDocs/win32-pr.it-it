---
description: La funzione EndPagePrinter notifica allo spooler di stampa che l'applicazione si trova alla fine di una pagina in un processo di stampa.
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: Funzione EndPagePrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 9a152716a295650575fce0fefe5299ca4a214c322afa6570760c988182f9ba65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711861"
---
# <a name="endpageprinter-function"></a>Funzione EndPagePrinter

La **funzione EndPagePrinter** notifica allo spooler di stampa che l'applicazione si trova alla fine di una pagina in un processo di stampa.

## <a name="syntax"></a>Sintassi


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per cui verrà conclusa la pagina. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

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
3.  Per scrivere dati in una pagina, chiamare [**WritePrinter**](writeprinter.md).
4.  Per terminare ogni pagina, chiamare **EndPagePrinter**.
5.  Ripetere 2, 3 e 4 per il numero di pagine necessario.
6.  Per terminare il processo di stampa, [**chiamare EndDocPrinter**](enddocprinter.md).

Quando una pagina in un file di spooling supera circa 350 MB, può non riuscire a stampare e non inviare un messaggio di errore. Ad esempio, ciò può verificarsi quando si stampano file EMF di grandi dimensioni. Il limite delle dimensioni della pagina dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamanti e la quantità di frammentazione nell'heap del processo.

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

 

 





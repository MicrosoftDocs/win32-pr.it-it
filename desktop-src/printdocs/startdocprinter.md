---
description: La funzione StartDocPrinter notifica allo spooler di stampa che è necessario eseguire lo spooling di un documento per la stampa.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: Funzione StartDocPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884669"
---
# <a name="startdocprinter-function"></a>StartDocPrinter (funzione)

La funzione **StartDocPrinter** notifica allo spooler di stampa che è necessario eseguire lo spooling di un documento per la stampa.

## <a name="syntax"></a>Sintassi


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura a cui punta *pDocInfo* . Questo valore deve essere 1.

</dd> <dt>

*pDocInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**doc \_ info \_ 1**](doc-info-1.md) che descrive il documento da stampare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito identifica il processo di stampa.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

La sequenza tipica per un processo di stampa è la seguente:

1.  Per iniziare un processo di stampa, chiamare **StartDocPrinter**.
2.  Per iniziare ogni pagina, chiamare [**StartPagePrinter**](startpageprinter.md).
3.  Per scrivere i dati in una pagina, chiamare [**WritePrinter**](writeprinter.md).
4.  Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).
5.  Ripetere 2, 3 e 4 per il numero di pagine necessario.
6.  Per terminare il processo di stampa, chiamare [**EndDocPrinter**](enddocprinter.md).

Si noti che la chiamata a [**StartPagePrinter**](startpageprinter.md) e [**EndPagePrinter**](endpageprinter.md) potrebbe non essere necessaria, ad esempio se il tipo di dati di stampa include le informazioni sulla pagina.

Quando una pagina in un file con spooling supera circa 350 MB, potrebbe non essere possibile stampare e inviare un messaggio di errore. Questo può verificarsi, ad esempio, durante la stampa di file EMF di grandi dimensioni. Il limite delle dimensioni della pagina dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamante e la quantità di frammentazione nell'heap dei processi.

## <a name="examples"></a>Esempio

Per un programma di esempio che usa questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **StartDocPrinterW** (Unicode) e **StartDocPrinterA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**\_Informazioni doc \_ 1**](doc-info-1.md)
</dt> <dt>

[**Informazioni del documento \_ \_ 2**](doc-info-2.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 





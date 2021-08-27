---
description: La funzione StartDocPrinter notifica lo spooler di stampa che è necessario eseguire lo spooling di un documento per la stampa.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: Funzione StartDocPrinter (Winspool.h)
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
ms.openlocfilehash: 047784a7debd0c12fa7a5ad144dbc1e81c4715d990be794c180e86555c8e9f37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060011"
---
# <a name="startdocprinter-function"></a>Funzione StartDocPrinter

La **funzione StartDocPrinter** notifica lo spooler di stampa che è necessario eseguire lo spooling di un documento per la stampa.

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Versione della struttura a cui *punta pDocInfo.* Questo valore deve essere 1.

</dd> <dt>

*pDocInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura DOC \_ INFO \_ 1**](doc-info-1.md) che descrive il documento da stampare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito identifica il processo di stampa.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

La sequenza tipica per un processo di stampa è la seguente:

1.  Per iniziare un processo di stampa, **chiamare StartDocPrinter**.
2.  Per iniziare ogni pagina, chiamare [**StartPagePrinter**](startpageprinter.md).
3.  Per scrivere dati in una pagina, chiamare [**WritePrinter**](writeprinter.md).
4.  Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).
5.  Ripetere 2, 3 e 4 per il numero di pagine necessario.
6.  Per terminare il processo di stampa, [**chiamare EndDocPrinter**](enddocprinter.md).

Si noti che la [**chiamata di StartPagePrinter**](startpageprinter.md) ed [**EndPagePrinter**](endpageprinter.md) potrebbe non essere necessaria, ad esempio se il tipo di dati print include le informazioni sulla pagina.

Quando una pagina in un file di spooling supera circa 350 MB, può non riuscire a stampare e non inviare un messaggio di errore. Ad esempio, ciò può verificarsi quando si stampano file EMF di grandi dimensioni. Il limite delle dimensioni della pagina dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamanti e la quantità di frammentazione nell'heap del processo.

## <a name="examples"></a>Esempio

Per un programma di esempio che usa questa funzione, vedere [Procedura: Stampare usando l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **StartDocPrinterW** (Unicode) e **StartDocPrinterA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**DOC \_ INFO \_ 1**](doc-info-1.md)
</dt> <dt>

[**DOC \_ INFO \_ 2**](doc-info-2.md)
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

 

 





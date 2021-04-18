---
description: Nell'esempio di codice riportato più avanti in questo argomento viene illustrato come inviare i dati di controllo della stampante direttamente alle stampanti che utilizzano i driver della stampante basati su GDI.
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: 'Procedura: inviare dati direttamente a una stampante GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1968b435068a62ce7a7d379a66c1500d04d8936a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314982"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a>Procedura: inviare dati direttamente a una stampante GDI

Nell'esempio di codice riportato più avanti in questo argomento viene illustrato come inviare i dati di controllo della stampante direttamente alle stampanti che utilizzano i driver della stampante basati su GDI.

Nei passaggi seguenti viene descritto come inviare dati direttamente a una stampante. Questi passaggi sono illustrati anche nell'esempio di codice seguente.

1.  Chiamare [**OpenPrinter**](openprinter.md) per ottenere un handle per la stampante.
2.  Inizializzare una struttura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) con i dati della stampante.
3.  Chiamare [**StartDocPrinter**](startdocprinter.md) per indicare che l'applicazione invierà i dati del documento alla stampante.
4.  Chiamare [**StartPagePrinter**](startpageprinter.md) per indicare che l'applicazione invierà una nuova pagina alla stampante.
5.  Chiamare [**WritePrinter**](writeprinter.md) per inviare i dati.
6.  Chiamare [**EndPagePrinter**](endpageprinter.md) per indicare che tutti i dati per la pagina corrente sono stati inviati.
7.  Chiamare [**EndDocPrinter**](enddocprinter.md) per indicare che tutti i dati per questo documento sono stati inviati.
8.  Chiamare [**ClosePrinter**](closeprinter.md) per rilasciare le risorse.

Inviare i dati di controllo della stampante direttamente alle stampanti che utilizzano i driver della stampante basati su GDI.


```C++
// 
// RawDataToPrinter - sends binary data directly to a printer 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToPrinter(LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1 DocInfo;
    DWORD      dwJob = 0L;
    DWORD      dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter( szPrinterName, &hPrinter, NULL );
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;
        DocInfo.pDatatype = (LPTSTR)_T("RAW");

        // Inform the spooler the document is beginning. 
        dwJob = StartDocPrinter( hPrinter, 1, (LPBYTE)&DocInfo );
        if (dwJob > 0) {
            // Start a page. 
            bStatus = StartPagePrinter( hPrinter );
            if (bStatus) {
                // Send the data to the printer. 
                bStatus = WritePrinter( hPrinter, lpData, dwCount, &dwBytesWritten);
                EndPagePrinter (hPrinter);
            }
            // Inform the spooler that the document is ending. 
            EndDocPrinter( hPrinter );
        }
        // Close the printer handle. 
        ClosePrinter( hPrinter );
    }
    // Check to see if correct number of bytes were written. 
    if (!bStatus || (dwBytesWritten != dwCount)) {
        bStatus = FALSE;
    } else {
        bStatus = TRUE;
    }
    return bStatus;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ClosePrinter**](closeprinter.md)
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

 

 

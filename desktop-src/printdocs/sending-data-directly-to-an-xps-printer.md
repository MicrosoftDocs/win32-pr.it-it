---
description: In questo argomento viene descritto come inviare i dati di controllo della stampante direttamente alle stampanti che usano i driver della stampante XPSDrv.
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: 'Procedura: Inviare dati direttamente a una stampante XPS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fba87578f9257290123b737f2d1d8c3e48f57e6a628110a20a232ddb290ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470153"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a>Procedura: Inviare dati direttamente a una stampante XPS

In questo argomento viene descritto come inviare i dati di controllo della stampante direttamente alle stampanti che usano i driver della stampante XPSDrv.

I passaggi seguenti descrivono come inviare i dati direttamente a una stampante. Questi passaggi sono illustrati anche nell'esempio di codice seguente.

1.  Chiamare [**OpenPrinter**](openprinter.md) per ottenere un handle per la stampante.
2.  Inizializzare [**una struttura DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) con i dati della stampante.
3.  Chiamare [**StartDocPrinter per**](startdocprinter.md) indicare che l'applicazione invierà i dati del documento alla stampante.
4.  Chiamare [**WritePrinter**](writeprinter.md) per inviare i dati.
5.  Chiamare [**EndDocPrinter**](enddocprinter.md) per indicare che tutti i dati per questo documento sono stati inviati.
6.  Chiamare [**ClosePrinter**](closeprinter.md) per rilasciare le risorse.

Inviare i dati di controllo della stampante direttamente alle stampanti che usano i driver della stampante XPSDrv.


```C++
// 
//  RawDataToXpsPrinter - sends binary data directly to a printer 
//          with an XPSDrv Printer Driver 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToXpsPrinter (LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1       DocInfo;
    DWORD    dwPrtJob = 0L;
    DWORD    dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter (szPrinterName, &hPrinter, NULL);
    
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;

        // Enter the datatype of this buffer.
        //  Use "XPS_PASS" when the data buffer should bypass the 
        //    print filter pipeline of the XPSDrv printer driver. 
        //    This datatype would be used to send the buffer directly 
        //    to the printer, such as when sending print head alignment 
        //    commands. Normally, a data buffer would be sent as the
        //    "RAW" datatype.
        //
        DocInfo.pDatatype = (LPTSTR)_T("XPS_PASS");

        dwPrtJob = StartDocPrinter (
                        hPrinter,
                        1,
                        (LPBYTE)&DocInfo);

        if (dwPrtJob > 0) {
                // Send the data to the printer. 
                bStatus = WritePrinter (
                hPrinter,
                lpData,
                dwCount,
                &dwBytesWritten);
        }
        
        EndDocPrinter (hPrinter);

        // Close the printer handle. 
        bStatus = ClosePrinter(hPrinter);
    }
    
    if (!bStatus || (dwCount != dwBytesWritten)) {
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

 

 

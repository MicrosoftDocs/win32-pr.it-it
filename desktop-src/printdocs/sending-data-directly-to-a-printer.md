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
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a><span data-ttu-id="55dc7-103">Procedura: inviare dati direttamente a una stampante GDI</span><span class="sxs-lookup"><span data-stu-id="55dc7-103">How To: Send Data Directly to a GDI Printer</span></span>

<span data-ttu-id="55dc7-104">Nell'esempio di codice riportato più avanti in questo argomento viene illustrato come inviare i dati di controllo della stampante direttamente alle stampanti che utilizzano i driver della stampante basati su GDI.</span><span class="sxs-lookup"><span data-stu-id="55dc7-104">The code sample later in this topic shows how to send printer control data directly to printers that use GDI-based printer drivers.</span></span>

<span data-ttu-id="55dc7-105">Nei passaggi seguenti viene descritto come inviare dati direttamente a una stampante.</span><span class="sxs-lookup"><span data-stu-id="55dc7-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="55dc7-106">Questi passaggi sono illustrati anche nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="55dc7-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="55dc7-107">Chiamare [**OpenPrinter**](openprinter.md) per ottenere un handle per la stampante.</span><span class="sxs-lookup"><span data-stu-id="55dc7-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="55dc7-108">Inizializzare una struttura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) con i dati della stampante.</span><span class="sxs-lookup"><span data-stu-id="55dc7-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="55dc7-109">Chiamare [**StartDocPrinter**](startdocprinter.md) per indicare che l'applicazione invierà i dati del documento alla stampante.</span><span class="sxs-lookup"><span data-stu-id="55dc7-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="55dc7-110">Chiamare [**StartPagePrinter**](startpageprinter.md) per indicare che l'applicazione invierà una nuova pagina alla stampante.</span><span class="sxs-lookup"><span data-stu-id="55dc7-110">Call [**StartPagePrinter**](startpageprinter.md) to indicate that the application will be sending a new page to the printer.</span></span>
5.  <span data-ttu-id="55dc7-111">Chiamare [**WritePrinter**](writeprinter.md) per inviare i dati.</span><span class="sxs-lookup"><span data-stu-id="55dc7-111">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
6.  <span data-ttu-id="55dc7-112">Chiamare [**EndPagePrinter**](endpageprinter.md) per indicare che tutti i dati per la pagina corrente sono stati inviati.</span><span class="sxs-lookup"><span data-stu-id="55dc7-112">Call [**EndPagePrinter**](endpageprinter.md) to indicate that all data for the current page has been sent.</span></span>
7.  <span data-ttu-id="55dc7-113">Chiamare [**EndDocPrinter**](enddocprinter.md) per indicare che tutti i dati per questo documento sono stati inviati.</span><span class="sxs-lookup"><span data-stu-id="55dc7-113">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
8.  <span data-ttu-id="55dc7-114">Chiamare [**ClosePrinter**](closeprinter.md) per rilasciare le risorse.</span><span class="sxs-lookup"><span data-stu-id="55dc7-114">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="55dc7-115">Inviare i dati di controllo della stampante direttamente alle stampanti che utilizzano i driver della stampante basati su GDI.</span><span class="sxs-lookup"><span data-stu-id="55dc7-115">Send printer control data directly to printers that use GDI-based printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="55dc7-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55dc7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55dc7-117">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="55dc7-117">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="55dc7-118">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="55dc7-118">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="55dc7-119">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="55dc7-119">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="55dc7-120">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="55dc7-120">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="55dc7-121">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="55dc7-121">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="55dc7-122">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="55dc7-122">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="55dc7-123">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="55dc7-123">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 

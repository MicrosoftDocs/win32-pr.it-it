---
title: Uso delle funzioni di modifica e inserimento di un file negli Appunti
description: Uso delle funzioni di modifica e inserimento di un file negli Appunti
ms.assetid: 2c69e44a-5f45-45e7-bbad-c593359943a0
keywords:
- EditStreamClone (funzione)
- EditStreamCopy (funzione)
- EditStreamCut (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533f2165afdb3173ea0f8c603764f25d0fa625fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955269"
---
# <a name="using-the-editing-functions-and-putting-a-file-on-the-clipboard"></a><span data-ttu-id="73e94-106">Uso delle funzioni di modifica e inserimento di un file negli Appunti</span><span class="sxs-lookup"><span data-stu-id="73e94-106">Using the Editing Functions and Putting a File on the Clipboard</span></span>

<span data-ttu-id="73e94-107">Nell'esempio seguente vengono tagliati, copiati o eliminati segmenti da una matrice di flussi.</span><span class="sxs-lookup"><span data-stu-id="73e94-107">The following example cuts, copies, or deletes segments from an array of streams.</span></span> <span data-ttu-id="73e94-108">I flussi tagliati e copiati vengono uniti in un nuovo file e inseriti negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="73e94-108">The cut and copied streams are merged into a new file and placed on the clipboard.</span></span> <span data-ttu-id="73e94-109">Le funzioni usate includono [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone), [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)e [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut).</span><span class="sxs-lookup"><span data-stu-id="73e94-109">The functions used include [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone), [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy), and [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut).</span></span>


```C++
// Global variables 
// gcpavi - count of streams in an AVI file 
// gapavi[] - array of stream-interface pointers, used as data source 
// gapaviSel[] - stream-interface pointers of edited streams 
// galSelStart[] - edit starting point in each stream 
// galSelLen[] - length of edit to make in each stream 
// gapaviTemp[] - array of stream-interface pointers put on clipboard 
// 
// Comment: 
//     The editable streams in gapaviSel have been 
//     initialized with CreateEditableStream. 
 
case MENU_CUT: 
case MENU_COPY: 
case MENU_DELETE: 
{ 
    PAVIFILE pf; 
    int      i; 
 
    // Walk list of selections and make streams out of each section. 
    gcpaviSel = 0;  // index counter for destination streams 
    for (i = 0; i < gcpavi; i++) { 
        if (galSelStart[i] != -1) { 
            if (wParam == MENU_COPY) 
                EditStreamCopy(gapavi[i], &galSelStart[i], 
                &galSelLen[i], &gapaviSel[gcpaviSel++]); 
            else { 
                EditStreamCut(gapavi[i], &galSelStart[i], 
                &galSelLen[i], &gapaviSel[gcpaviSel++]); 
            } 
        } 
    } 
 
. 
. 
. 
    // Put on the clipboard if segment is not deleted. 
    if (gcpaviSel && wParam != MENU_DELETE) { 
        PAVISTREAM   gapaviTemp[MAXNUMSTREAMS]; 
        int i; 
 
        // Clone the edited streams, so that if the user does 
        // more editing, the clipboard won't change. 
        for (i = 0; i < gcpaviSel; i++) { 
            gapaviTemp[i] = NULL; 
            EditStreamClone(gapaviSel[i], &gapaviTemp[i]); 
            // 
            // Place error check here. 
            // 
        } 
 
        // Create a file from the streams and put on clipboard. 
        AVIMakeFileFromStreams(&pf, gcpaviSel, gapaviTemp); 
        AVIPutFileOnClipboard(pf); 
 
        // Release clone streams. 
        for (i = 0; i < gcpaviSel; i++) { 
            AVIStreamRelease(gapaviTemp[i]); 
        } 
 
        // Release file put on clipboard. 
        AVIFileRelease(pf); 
    } 
 
    // Release streams created. 
    for (i = 0; i < gcpaviSel; i++) 
        AVIStreamRelease(gapaviSel[i]); 
} 
 
```



 

 





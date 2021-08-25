---
title: Uso delle funzioni di modifica e inserimento di un file negli Appunti
description: Uso delle funzioni di modifica e inserimento di un file negli Appunti
ms.assetid: 2c69e44a-5f45-45e7-bbad-c593359943a0
keywords:
- Funzione EditStreamClone
- Funzione EditStreamCopy
- Funzione EditStreamCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2f3ad09b882d9df6d9b7603e6f5596789ba32157f6050916ae9212f52395a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804531"
---
# <a name="using-the-editing-functions-and-putting-a-file-on-the-clipboard"></a>Uso delle funzioni di modifica e inserimento di un file negli Appunti

Nell'esempio seguente vengono tagliati, copiati o eliminati segmenti da una matrice di flussi. I flussi tagliati e copiati vengono uniti in un nuovo file e inseriti negli Appunti. Le funzioni usate includono [**EditStreamClone,**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)e [**EditStreamCut.**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)


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



 

 





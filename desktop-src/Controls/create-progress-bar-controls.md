---
title: Come usare i controlli indicatore di stato
description: Questo argomento illustra come usare un indicatore di stato per indicare lo stato di avanzamento di una lunga operazione di analisi dei file.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65d47d6b41422853d401a1fb2686e03e3d3f5bc378b78b7ba762b86fc7ffe30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826421"
---
# <a name="how-to-use-progress-bar-controls"></a>Come usare i controlli indicatore di stato

Questo argomento illustra come usare un indicatore di stato per indicare lo stato di avanzamento di una lunga operazione di analisi dei file.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-progress-bar-control"></a>Creare un controllo indicatore di stato

Il codice di esempio seguente crea un indicatore di stato e lo posiziona nella parte inferiore dell'area client della finestra padre. L'altezza dell'indicatore di stato è basata sull'altezza della bitmap della freccia usata in una barra di scorrimento. L'intervallo è basato sulle dimensioni del file diviso per 2.048, ovvero le dimensioni di ogni "blocco" di dati letti dal file. L'esempio imposta anche un incremento e fa avanzare la posizione corrente dell'indicatore di stato dell'incremento dopo l'analisi di ogni blocco.


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a>Commenti

È necessario assicurarsi di usare correttamente la [**funzione ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) per garantire la sicurezza dell'applicazione. Nel codice di esempio, ad esempio, è necessario verificare che legge `ReadFile` effettivamente tutti i dati richiesti.

Si noti anche che il quarto parametro [**di CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)( (LPSECURITY \_ ATTRIBUTES)**NULL**- imposta i valori di sicurezza predefiniti. Se sono necessarie impostazioni di sicurezza specifiche, è necessario impostare i valori appropriati nei membri della struttura. Chiamare **sizeof** per impostare le dimensioni corrette della struttura **LPSECURITY \_ ATTRIBUTES.**

Per altre informazioni, vedere [Considerazioni sulla sicurezza: Microsoft Windows Controls](sec-comctls.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli indicatore di stato](using-progress-bar-controls.md)
</dt> <dt>

[Considerazioni sulla sicurezza: Controlli Windows Microsoft](sec-comctls.md)
</dt> </dl>

 

 
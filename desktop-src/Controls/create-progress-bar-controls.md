---
title: Come usare i controlli indicatore di stato
description: In questo argomento viene illustrato come utilizzare un indicatore di stato per indicare lo stato di un'operazione di analisi dei file di lunga durata.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963509"
---
# <a name="how-to-use-progress-bar-controls"></a>Come usare i controlli indicatore di stato

In questo argomento viene illustrato come utilizzare un indicatore di stato per indicare lo stato di un'operazione di analisi dei file di lunga durata.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="create-a-progress-bar-control"></a>Creare un controllo indicatore di stato

Il codice di esempio seguente crea un indicatore di stato e lo posiziona lungo la parte inferiore dell'area client della finestra padre. L'altezza dell'indicatore di stato è basata sull'altezza della bitmap della freccia utilizzata in una barra di scorrimento. L'intervallo è basato sulle dimensioni del file diviso per 2.048, ovvero le dimensioni di ogni "blocco" di dati letti dal file. Nell'esempio viene inoltre impostato un incremento e viene spostata in avanti la posizione corrente dell'indicatore di stato in base all'incremento dopo l'analisi di ogni blocco.


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

Per garantire la sicurezza dell'applicazione, è necessario assicurarsi di usare correttamente la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . Nel codice di esempio, ad esempio, è necessario assicurarsi che `ReadFile` legga effettivamente tutti i dati richiesti.

Si noti anche che il quarto parametro di [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)-( \_ attributi LPSECURITY)**null**-imposta i valori di sicurezza predefiniti. Se sono necessarie impostazioni di sicurezza specifiche, è necessario impostare i valori appropriati nei membri della struttura. Chiamare **sizeof** per impostare la dimensione corretta della struttura **degli \_ attributi LPSECURITY** .

Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di controlli indicatore di stato](using-progress-bar-controls.md)
</dt> <dt>

[Considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md)
</dt> </dl>

 

 
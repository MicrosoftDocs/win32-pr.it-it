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
# <a name="how-to-use-progress-bar-controls"></a><span data-ttu-id="70f6e-103">Come usare i controlli indicatore di stato</span><span class="sxs-lookup"><span data-stu-id="70f6e-103">How to Use Progress Bar Controls</span></span>

<span data-ttu-id="70f6e-104">In questo argomento viene illustrato come utilizzare un indicatore di stato per indicare lo stato di un'operazione di analisi dei file di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="70f6e-104">This topic explains how to use a progress bar to indicate the progress of a lengthy file-parsing operation.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="70f6e-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="70f6e-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="70f6e-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="70f6e-106">Technologies</span></span>

-   [<span data-ttu-id="70f6e-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="70f6e-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="70f6e-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="70f6e-108">Prerequisites</span></span>

-   <span data-ttu-id="70f6e-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="70f6e-109">C/C++</span></span>
-   <span data-ttu-id="70f6e-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="70f6e-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="70f6e-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="70f6e-111">Instructions</span></span>

### <a name="create-a-progress-bar-control"></a><span data-ttu-id="70f6e-112">Creare un controllo indicatore di stato</span><span class="sxs-lookup"><span data-stu-id="70f6e-112">Create a Progress Bar Control</span></span>

<span data-ttu-id="70f6e-113">Il codice di esempio seguente crea un indicatore di stato e lo posiziona lungo la parte inferiore dell'area client della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="70f6e-113">The following example code creates a progress bar and positions it along the bottom of the parent window's client area.</span></span> <span data-ttu-id="70f6e-114">L'altezza dell'indicatore di stato è basata sull'altezza della bitmap della freccia utilizzata in una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="70f6e-114">The height of the progress bar is based on the height of the arrow bitmap used in a scroll bar.</span></span> <span data-ttu-id="70f6e-115">L'intervallo è basato sulle dimensioni del file diviso per 2.048, ovvero le dimensioni di ogni "blocco" di dati letti dal file.</span><span class="sxs-lookup"><span data-stu-id="70f6e-115">The range is based on the size of the file divided by 2,048, which is the size of each "chunk" of data that is read from the file.</span></span> <span data-ttu-id="70f6e-116">Nell'esempio viene inoltre impostato un incremento e viene spostata in avanti la posizione corrente dell'indicatore di stato in base all'incremento dopo l'analisi di ogni blocco.</span><span class="sxs-lookup"><span data-stu-id="70f6e-116">The example also sets an increment and advances the current position of the progress bar by the increment after parsing each chunk.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="70f6e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="70f6e-117">Remarks</span></span>

<span data-ttu-id="70f6e-118">Per garantire la sicurezza dell'applicazione, è necessario assicurarsi di usare correttamente la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) .</span><span class="sxs-lookup"><span data-stu-id="70f6e-118">You must make sure to use the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function correctly, to ensure the security of your application.</span></span> <span data-ttu-id="70f6e-119">Nel codice di esempio, ad esempio, è necessario assicurarsi che `ReadFile` legga effettivamente tutti i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="70f6e-119">For instance, in the example code, you should check to make sure that `ReadFile` actually reads all of the requested data.</span></span>

<span data-ttu-id="70f6e-120">Si noti anche che il quarto parametro di [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)-( \_ attributi LPSECURITY)**null**-imposta i valori di sicurezza predefiniti.</span><span class="sxs-lookup"><span data-stu-id="70f6e-120">Also notice that the fourth parameter of [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)—(LPSECURITY\_ATTRIBUTES)**NULL**—sets default security values.</span></span> <span data-ttu-id="70f6e-121">Se sono necessarie impostazioni di sicurezza specifiche, è necessario impostare i valori appropriati nei membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="70f6e-121">If you need specific security settings, you must set the appropriate values in the structure's members.</span></span> <span data-ttu-id="70f6e-122">Chiamare **sizeof** per impostare la dimensione corretta della struttura **degli \_ attributi LPSECURITY** .</span><span class="sxs-lookup"><span data-stu-id="70f6e-122">Call **sizeof** to set the correct size of the **LPSECURITY\_ATTRIBUTES** structure.</span></span>

<span data-ttu-id="70f6e-123">Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md).</span><span class="sxs-lookup"><span data-stu-id="70f6e-123">For more information, see [Security Considerations: Microsoft Windows Controls](sec-comctls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="70f6e-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70f6e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70f6e-125">Utilizzo di controlli indicatore di stato</span><span class="sxs-lookup"><span data-stu-id="70f6e-125">Using Progress Bar Controls</span></span>](using-progress-bar-controls.md)
</dt> <dt>

[<span data-ttu-id="70f6e-126">Considerazioni sulla sicurezza: controlli di Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="70f6e-126">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)
</dt> </dl>

 

 
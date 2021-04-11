---
title: Come usare i flussi
description: È possibile utilizzare i flussi per trasferire i dati all'interno o all'esterno di un controllo Rich Edit. Un flusso è definito da una struttura EDITSTREAM, che specifica un buffer e una funzione di callback definita dall'applicazione.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104117494"
---
# <a name="how-to-use-streams"></a><span data-ttu-id="b1769-104">Come usare i flussi</span><span class="sxs-lookup"><span data-stu-id="b1769-104">How to Use Streams</span></span>

<span data-ttu-id="b1769-105">È possibile utilizzare i flussi per trasferire i dati all'interno o all'esterno di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b1769-105">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="b1769-106">Un flusso è definito da una struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) , che specifica un buffer e una funzione di callback definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1769-106">A stream is defined by an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure, which specifies a buffer and an application-defined callback function.</span></span>

<span data-ttu-id="b1769-107">Per leggere i dati in un controllo Rich Edit (ovvero il flusso nei dati), usare il messaggio [**\_ Stream em**](em-streamin.md) .</span><span class="sxs-lookup"><span data-stu-id="b1769-107">To read data into a rich edit control (that is, stream in the data), use the [**EM\_STREAMIN**](em-streamin.md) message.</span></span> <span data-ttu-id="b1769-108">Il controllo chiama ripetutamente la funzione di callback dell'applicazione, che trasferisce ogni volta una parte dei dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-108">The control repeatedly calls the application's callback function, which transfers a portion of the data into the buffer each time.</span></span>

<span data-ttu-id="b1769-109">Per salvare il contenuto di un controllo Rich Edit (ovvero trasmettere in streaming i dati), è possibile usare il messaggio [**di \_ flusso em**](em-streamout.md) .</span><span class="sxs-lookup"><span data-stu-id="b1769-109">To save the contents of a rich edit control (that is, stream out the data), you can use the [**EM\_STREAMOUT**](em-streamout.md) message.</span></span> <span data-ttu-id="b1769-110">Il controllo scrive ripetutamente nel buffer e quindi chiama la funzione di callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1769-110">The control repeatedly writes to the buffer and then calls the application's callback function.</span></span> <span data-ttu-id="b1769-111">Per ogni chiamata, la funzione di callback salva il contenuto del buffer.</span><span class="sxs-lookup"><span data-stu-id="b1769-111">For each call, the callback function saves the contents of the buffer.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b1769-112">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="b1769-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b1769-113">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="b1769-113">Technologies</span></span>

-   [<span data-ttu-id="b1769-114">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="b1769-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b1769-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="b1769-115">Prerequisites</span></span>

-   <span data-ttu-id="b1769-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="b1769-116">C/C++</span></span>
-   <span data-ttu-id="b1769-117">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="b1769-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b1769-118">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="b1769-118">Instructions</span></span>

### <a name="use-a-stream"></a><span data-ttu-id="b1769-119">Usare un flusso</span><span class="sxs-lookup"><span data-stu-id="b1769-119">Use a Stream</span></span>

<span data-ttu-id="b1769-120">Nell'esempio di codice seguente viene illustrato come leggere un file RTF in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b1769-120">The following code example shows how to read an .rtf file into a rich edit control.</span></span> <span data-ttu-id="b1769-121">L'handle di file viene passato alla funzione di callback tramite il membro **dwCookie** della struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="b1769-121">The file handle is passed to the callback function through the **dwCookie** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span>


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="b1769-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1769-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1769-123">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="b1769-123">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="b1769-124">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="b1769-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





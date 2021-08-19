---
title: Come usare Flussi
description: È possibile usare i flussi per trasferire i dati all'interno o all'uscita da un controllo Rich Edit. Un flusso è definito da una struttura EDITSTREAM, che specifica un buffer e una funzione di callback definita dall'applicazione.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae620d123ad983cd150bf78d27d99de137ec61eea8c5a32c9fcc9698cb262a63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828623"
---
# <a name="how-to-use-streams"></a>Come usare Flussi

È possibile usare i flussi per trasferire i dati all'interno o all'uscita da un controllo Rich Edit. Un flusso è definito da una [**struttura EDITSTREAM,**](/windows/desktop/api/Richedit/ns-richedit-editstream) che specifica un buffer e una funzione di callback definita dall'applicazione.

Per leggere i dati in un controllo Rich Edit(ovvero, trasmettere i dati), usare il [**messaggio \_ EM STREAMIN.**](em-streamin.md) Il controllo chiama ripetutamente la funzione di callback dell'applicazione, che trasferisce ogni volta una parte dei dati nel buffer.

Per salvare il contenuto di un controllo Rich Edit, ovvero trasmettere i dati in streaming, è possibile usare il [**messaggio \_ STREAMOUT EM.**](em-streamout.md) Il controllo scrive ripetutamente nel buffer e quindi chiama la funzione di callback dell'applicazione. Per ogni chiamata, la funzione di callback salva il contenuto del buffer.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-a-stream"></a>Usare un flusso

Nell'esempio di codice seguente viene illustrato come leggere un file RTF in un controllo Rich Edit. L'handle di file viene passato alla funzione di callback tramite **il membro dwCookie** della [**struttura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream)


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





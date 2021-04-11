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
# <a name="how-to-use-streams"></a>Come usare i flussi

È possibile utilizzare i flussi per trasferire i dati all'interno o all'esterno di un controllo Rich Edit. Un flusso è definito da una struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) , che specifica un buffer e una funzione di callback definita dall'applicazione.

Per leggere i dati in un controllo Rich Edit (ovvero il flusso nei dati), usare il messaggio [**\_ Stream em**](em-streamin.md) . Il controllo chiama ripetutamente la funzione di callback dell'applicazione, che trasferisce ogni volta una parte dei dati nel buffer.

Per salvare il contenuto di un controllo Rich Edit (ovvero trasmettere in streaming i dati), è possibile usare il messaggio [**di \_ flusso em**](em-streamout.md) . Il controllo scrive ripetutamente nel buffer e quindi chiama la funzione di callback dell'applicazione. Per ogni chiamata, la funzione di callback salva il contenuto del buffer.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-a-stream"></a>Usare un flusso

Nell'esempio di codice seguente viene illustrato come leggere un file RTF in un controllo Rich Edit. L'handle di file viene passato alla funzione di callback tramite il membro **dwCookie** della struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .


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

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





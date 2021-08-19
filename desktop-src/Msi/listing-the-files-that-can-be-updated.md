---
description: La funzione MsiGetPatchFileList e la proprietà PatchFiles dell'oggetto Installer accettano un elenco di patch del programma di installazione di Windows (file con estensione msp) e restituiscono un elenco di file che possono essere aggiornati dalle patch.
ms.assetid: cc2eb506-c1fc-4125-b98c-12221b918e23
title: Elenco dei file che possono essere aggiornati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad76355c97d62d9c3f1282b5ebd66f54c5fef0f6f7359a41a35f2ebaee9a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945906"
---
# <a name="listing-the-files-that-can-be-updated"></a>Elenco dei file che possono essere aggiornati

La funzione [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) e la [](installer-object.md) proprietà [**PatchFiles**](installer-patchfiles.md) dell'oggetto Installer accettano un elenco di patch del programma di installazione di Windows (file con estensione msp) e restituiscono un elenco di file che possono essere aggiornati dalle patch. La [**funzione MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) e la [**proprietà PatchFiles**](installer-patchfiles.md) sono disponibili a partire da Windows Installer 4.0.

## <a name="listing-files-that-can-be-updated"></a>Elenco dei file che possono essere aggiornati

L'esempio seguente illustra come estrarre le informazioni sull'applicabilità per un elenco di patch Windows Installer (file con estensione msp) usando [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista). Alla **funzione MsiGetPatchFileList** viene fornito il codice prodotto per la destinazione delle patch e un elenco di file msp delimitati da punti e virgola. Per questo esempio è Windows programma di installazione 4.0 in esecuzione Windows Vista.


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")
#pragma comment(lib, "shell32.lib")

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles);

int __cdecl main()
{
    UINT uiRet = ERROR_SUCCESS;
    int argc;
    WCHAR** argv = CommandLineToArgvW(GetCommandLine(), &argc);
    
    MSIHANDLE *phFileListRec = NULL;
    DWORD dwcFiles = 0;
    WCHAR* szProductCode = argv[1];
    WCHAR* szPatchFileList = argv[2];
    if(ERROR_SUCCESS != (uiRet = MsiGetPatchFileList(szProductCode, szPatchFileList, &dwcFiles, &phFileListRec)))
    {
        printf("MsiGetPatchFileListW(%S, ...) Failed with:%d", szProductCode, uiRet);
        return uiRet;
    }
    
    DWORD cchBuf = 1;
    DWORD cchBufSize = 1;
    WCHAR* szBuf = new WCHAR[cchBufSize];
    if (!szBuf)
    {
        printf("Failed to allocate memory");
        CloseMsiHandles(phFileListRec, dwcFiles);
        return ERROR_OUTOFMEMORY;
    }
    memset(szBuf, 0, sizeof(WCHAR)*cchBufSize);
    
    for(unsigned int i = 0; i < dwcFiles; i++)
    {
        cchBuf = cchBufSize;
        while(ERROR_MORE_DATA == (uiRet = MsiRecordGetString(phFileListRec[i], 0, szBuf, &cchBuf)))
        {
            if (szBuf)
                delete[] szBuf;
            cchBufSize = ++cchBuf;
            szBuf = new WCHAR[cchBufSize];
            if (!szBuf)
            {
                printf("Failed to allocate memory");
                CloseMsiHandles(phFileListRec, dwcFiles);
                return ERROR_OUTOFMEMORY;
            }
        }
        
        if(uiRet != ERROR_SUCCESS)
        {
            printf("MsiRecordGetString(phFileListRec[%d] with %d", i, uiRet);
            CloseMsiHandles(phFileListRec, dwcFiles);
            if (szBuf)
                delete[] szBuf;
            return uiRet;
        }
        else
        {
            printf("File %d:%S\n", i, szBuf);
        }            
    }

    CloseMsiHandles(phFileListRec, dwcFiles);
    if (szBuf)
        delete[] szBuf;
    return 0;
}

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles)
{
    if (!phFileListRec)
        return;
    
    for (unsigned int i = 0; i < dwcFiles; i++)
    {
        if (phFileListRec[i])
            MsiCloseHandle(phFileListRec[i]);
    }    
}
//
```



L'esempio seguente illustra come estrarre le informazioni sull'applicabilità per un elenco di patch del programma di installazione di Windows (file con estensione msp) usando la proprietà [**PatchFiles**](installer-patchfiles.md) dell'oggetto [**Installer**](installer-object.md). Alla **proprietà PatchFiles** viene fornito il codice prodotto per la destinazione delle patch e un elenco di file msp delimitati da punti e virgola. Per questo esempio è Windows programma di installazione 4.0 in esecuzione Windows Vista.


```VB
Dim FileList
Dim installer : Set installer = Nothing
Dim argCount:argCount = Wscript.Arguments.Count

Set installer = Wscript.CreateObject("WindowsInstaller.Installer")

If (argCount > 0) Then
    sProdCode = Wscript.Arguments(0)
    sPatchPckgPath = Wscript.Arguments(1)
    Set FileList = installer.PatchFiles (sProdCode, sPatchPckgPath)
    For each File in FileList
           Wscript.Echo "Affected file: " & File
    Next
Else
    Usage
End If

Sub Usage
    Wscript.Echo "Windows Installer utility to list files updated by a patch for an installed product" &_
    vbNewLine & " 1st argument is the product code (GUID) of an installed product" &_
    vbNewLine & " 2nd argument is the list of patches" &_
    vbNewLine &_
    vbNewLine & "Copyright (C) Microsoft. All rights reserved."
    Wscript.Quit 1
End Sub
```



 

 




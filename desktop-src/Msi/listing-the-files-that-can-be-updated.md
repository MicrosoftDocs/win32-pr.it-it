---
description: La funzione MsiGetPatchFileList e la proprietà PatchFiles dell'oggetto Installer accettano un elenco di patch Windows Installer (file con estensione msp) e restituiscono un elenco di file che possono essere aggiornati dalle patch.
ms.assetid: cc2eb506-c1fc-4125-b98c-12221b918e23
title: Elenco dei file che possono essere aggiornati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c15872cce902f5a9059d4256e9e5c30ecff213f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314206"
---
# <a name="listing-the-files-that-can-be-updated"></a><span data-ttu-id="b226f-103">Elenco dei file che possono essere aggiornati</span><span class="sxs-lookup"><span data-stu-id="b226f-103">Listing the Files that can be Updated</span></span>

<span data-ttu-id="b226f-104">La funzione [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) e la proprietà [**PatchFiles**](installer-patchfiles.md) dell' [**oggetto Installer**](installer-object.md) accettano un elenco di patch Windows Installer (file con estensione msp) e restituiscono un elenco di file che possono essere aggiornati dalle patch.</span><span class="sxs-lookup"><span data-stu-id="b226f-104">The [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) function and [**PatchFiles**](installer-patchfiles.md) property of the [**Installer Object**](installer-object.md) take a list of Windows Installer patches (.msp files) and return a list of files that can be updated by the patches.</span></span> <span data-ttu-id="b226f-105">La funzione [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) e la proprietà [**PatchFiles**](installer-patchfiles.md) sono disponibili a partire da Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="b226f-105">The [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) function and [**PatchFiles**](installer-patchfiles.md) property are available beginning with Windows Installer 4.0.</span></span>

## <a name="listing-files-that-can-be-updated"></a><span data-ttu-id="b226f-106">Elenco di file che possono essere aggiornati</span><span class="sxs-lookup"><span data-stu-id="b226f-106">Listing Files that can be Updated</span></span>

<span data-ttu-id="b226f-107">Nell'esempio seguente viene illustrato come estrarre le informazioni sull'applicabilità per un elenco di patch di Windows Installer (file con estensione msp) utilizzando [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span><span class="sxs-lookup"><span data-stu-id="b226f-107">The following example shows you how to extract the applicability information for a list of Windows Installer patches (.msp files) using [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="b226f-108">Alla funzione **MsiGetPatchFileList** viene fornito il codice prodotto per la destinazione delle patch e un elenco di file con estensione msp delimitati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="b226f-108">The **MsiGetPatchFileList** function is provided the product code for the target of the patches and a list of .msp files delimited by semicolons.</span></span> <span data-ttu-id="b226f-109">Questo esempio richiede Windows Installer 4,0 in esecuzione in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b226f-109">This example requires Windows Installer 4.0 running on Windows Vista.</span></span>


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



<span data-ttu-id="b226f-110">Nell'esempio seguente viene illustrato come estrarre le informazioni sull'applicabilità per un elenco di patch Windows Installer (file con estensione msp) utilizzando la proprietà [**PatchFiles**](installer-patchfiles.md) dell' [**oggetto del programma di installazione**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="b226f-110">The following example shows you how to extract the applicability information for a list of Windows Installer patches (.msp files) using [**PatchFiles**](installer-patchfiles.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="b226f-111">Alla proprietà **PatchFiles** viene fornito il codice prodotto per la destinazione delle patch e un elenco di file con estensione msp delimitati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="b226f-111">The **PatchFiles** property is provided the product code for the target of the patches and a list of .msp files delimited by semicolons.</span></span> <span data-ttu-id="b226f-112">Questo esempio richiede Windows Installer 4,0 in esecuzione in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b226f-112">This example requires Windows Installer 4.0 running on Windows Vista.</span></span>


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



 

 




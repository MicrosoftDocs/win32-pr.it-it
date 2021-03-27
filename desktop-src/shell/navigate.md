---
description: Sono ora disponibili tutti gli elementi essenziali necessari per spostarsi in un punto qualsiasi dello spazio dei nomi.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Spostamento nello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049602"
---
# <a name="navigating-the-namespace"></a><span data-ttu-id="78d32-103">Spostamento nello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78d32-103">Navigating the Namespace</span></span>

<span data-ttu-id="78d32-104">Sono ora disponibili tutti gli elementi essenziali necessari per spostarsi in un punto qualsiasi dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="78d32-104">You now have all the essential elements needed to navigate anywhere in the namespace.</span></span> <span data-ttu-id="78d32-105">Il modo più semplice per iniziare è fare in modo che l'applicazione chiami [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) per recuperare l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del desktop.</span><span class="sxs-lookup"><span data-stu-id="78d32-105">The simplest way to start is to have your application call [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) to retrieve the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="78d32-106">Quindi, per spostarsi verso il basso nello spazio dei nomi, l'applicazione può seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="78d32-106">Then, to navigate downward through the namespace, your application can follow these steps:</span></span>

1.  <span data-ttu-id="78d32-107">Enumerare il contenuto della cartella.</span><span class="sxs-lookup"><span data-stu-id="78d32-107">Enumerate the folder's contents.</span></span>
2.  <span data-ttu-id="78d32-108">Determinare quali oggetti sono sottocartelle e selezionarne uno.</span><span class="sxs-lookup"><span data-stu-id="78d32-108">Determine which objects are subfolders, and select one.</span></span>
3.  <span data-ttu-id="78d32-109">Eseguire l'associazione alla sottocartella per recuperare l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="78d32-109">Bind to the subfolder to retrieve its [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span>

<span data-ttu-id="78d32-110">Ripetere questi passaggi con la frequenza necessaria per raggiungere la destinazione.</span><span class="sxs-lookup"><span data-stu-id="78d32-110">Repeat these steps as often as necessary to reach the target.</span></span>

## <a name="a-simple-example-of-namespace-navigation"></a><span data-ttu-id="78d32-111">Esempio semplice di esplorazione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78d32-111">A Simple Example of Namespace Navigation</span></span>

<span data-ttu-id="78d32-112">Il seguente frammento di codice di esempio è una semplice applicazione console che illustra una serie di procedure illustrate nelle sezioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="78d32-112">The following piece of sample code is a simple console application that illustrates a number of the procedures discussed in the preceding sections.</span></span> <span data-ttu-id="78d32-113">Il controllo degli errori è stato omesso per maggiore chiarezza.</span><span class="sxs-lookup"><span data-stu-id="78d32-113">Error checking has been omitted for clarity.</span></span> <span data-ttu-id="78d32-114">L'applicazione esegue queste attività:</span><span class="sxs-lookup"><span data-stu-id="78d32-114">The application performs the following tasks:</span></span>

1.  <span data-ttu-id="78d32-115">Recupera l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) della cartella programmi ([usando l'interfaccia IShellFolder](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="78d32-115">Retrieves the Program Files folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface ([Using the IShellFolder Interface](folder-info.md)).</span></span>
2.  <span data-ttu-id="78d32-116">Enumera il contenuto della cartella ([enumerando il contenuto di una cartella](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="78d32-116">Enumerates the contents of the folder ([Enumerating the Contents of a Folder](folder-info.md)).</span></span>
3.  <span data-ttu-id="78d32-117">Determina tutti i nomi visualizzati e li stampa ([determinando i nomi visualizzati e altre proprietà](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="78d32-117">Determines all the display names and prints them ([Determining Display Names and Other Properties](folder-info.md)).</span></span>
4.  <span data-ttu-id="78d32-118">Cerca una sottocartella ([ottenendo un puntatore all'interfaccia IShellFolder di una sottocartella](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="78d32-118">Looks for a subfolder ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
5.  <span data-ttu-id="78d32-119">Esegue l'associazione alla prima sottocartella individuata ([ottenendo un puntatore all'interfaccia IShellFolder di una sottocartella](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="78d32-119">Binds to the first subfolder it finds ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
6.  <span data-ttu-id="78d32-120">Stampa i nomi visualizzati degli oggetti nella sottocartella.</span><span class="sxs-lookup"><span data-stu-id="78d32-120">Prints the display names of the objects in the subfolder.</span></span>


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>

main()
{
    LPITEMIDLIST pidlProgFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfFirstFolder = NULL;
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfProgFiles = NULL;
    LPENUMIDLIST ppenum = NULL;
    ULONG celtFetched;
    HRESULT hr;
    STRRET strDispName;
    TCHAR pszDisplayName[MAX_PATH];
    ULONG uAttr;
   
    CoInitialize( NULL );
    
    hr = SHGetFolderLocation(NULL, CSIDL_PROGRAM_FILES, NULL, 0, &pidlProgFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlProgFiles, NULL, IID_IShellFolder, (LPVOID *) &psfProgFiles);
    psfDeskTop->Release();

    hr = psfProgFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfProgFiles->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
        cout << pszDisplayName << '\n';
        if(!psfFirstFolder)
        {
            uAttr = SFGAO_FOLDER;
            psfProgFiles->GetAttributesOf(1, (LPCITEMIDLIST *) &pidlItems, &uAttr);
            if(uAttr & SFGAO_FOLDER)
            {
                hr = psfProgFiles->BindToObject(pidlItems, NULL, IID_IShellFolder, (LPVOID *) &psfFirstFolder);
            }
        }
        CoTaskMemFree(pidlItems);
    }

    cout << "\n\n";

    ppenum->Release();

    if(psfFirstFolder)
    {
        hr = psfFirstFolder->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

        while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
        {
            psfFirstFolder->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
            StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
            cout << pszDisplayName << '\n';
            CoTaskMemFree(pidlItems);
        }
    }

    ppenum->Release();
    CoTaskMemFree(pidlProgFiles);
    psfProgFiles->Release();
    psfFirstFolder->Release();

    CoUninitialize();
    return 0;
}
```



 

 

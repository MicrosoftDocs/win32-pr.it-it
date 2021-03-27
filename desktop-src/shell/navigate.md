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
# <a name="navigating-the-namespace"></a>Spostamento nello spazio dei nomi

Sono ora disponibili tutti gli elementi essenziali necessari per spostarsi in un punto qualsiasi dello spazio dei nomi. Il modo più semplice per iniziare è fare in modo che l'applicazione chiami [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) per recuperare l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del desktop. Quindi, per spostarsi verso il basso nello spazio dei nomi, l'applicazione può seguire questa procedura:

1.  Enumerare il contenuto della cartella.
2.  Determinare quali oggetti sono sottocartelle e selezionarne uno.
3.  Eseguire l'associazione alla sottocartella per recuperare l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Ripetere questi passaggi con la frequenza necessaria per raggiungere la destinazione.

## <a name="a-simple-example-of-namespace-navigation"></a>Esempio semplice di esplorazione dello spazio dei nomi

Il seguente frammento di codice di esempio è una semplice applicazione console che illustra una serie di procedure illustrate nelle sezioni precedenti. Il controllo degli errori è stato omesso per maggiore chiarezza. L'applicazione esegue queste attività:

1.  Recupera l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) della cartella programmi ([usando l'interfaccia IShellFolder](folder-info.md)).
2.  Enumera il contenuto della cartella ([enumerando il contenuto di una cartella](folder-info.md)).
3.  Determina tutti i nomi visualizzati e li stampa ([determinando i nomi visualizzati e altre proprietà](folder-info.md)).
4.  Cerca una sottocartella ([ottenendo un puntatore all'interfaccia IShellFolder di una sottocartella](folder-info.md)).
5.  Esegue l'associazione alla prima sottocartella individuata ([ottenendo un puntatore all'interfaccia IShellFolder di una sottocartella](folder-info.md)).
6.  Stampa i nomi visualizzati degli oggetti nella sottocartella.


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



 

 

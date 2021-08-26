---
description: Sono ora presenti tutti gli elementi essenziali necessari per spostarsi in qualsiasi punto dello spazio dei nomi.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Esplorazione dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2778fc21df12e9228f9335a52c04556e97563cba5f8a4cb6b82eb779944c451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111481"
---
# <a name="navigating-the-namespace"></a>Esplorazione dello spazio dei nomi

Sono ora presenti tutti gli elementi essenziali necessari per spostarsi in qualsiasi punto dello spazio dei nomi. Il modo più semplice per iniziare è fare in modo che l'applicazione chiami [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) per recuperare [**l'interfaccia IShellFolder del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) desktop. Quindi, per spostarsi verso il basso nello spazio dei nomi, l'applicazione può seguire questa procedura:

1.  Enumerare il contenuto della cartella.
2.  Determinare quali oggetti sono sottocartelle e selezionarne uno.
3.  Eseguire il binding alla sottocartella per recuperare [**l'interfaccia IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)

Ripetere questi passaggi con la frequenza necessaria per raggiungere la destinazione.

## <a name="a-simple-example-of-namespace-navigation"></a>Esempio semplice di navigazione nello spazio dei nomi

La parte di codice di esempio seguente è una semplice applicazione console che illustra una serie di procedure illustrate nelle sezioni precedenti. Il controllo degli errori è stato omesso per maggiore chiarezza. L'applicazione esegue queste attività:

1.  Recupera l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) della cartella Programmi ([tramite l'interfaccia IShellFolder](folder-info.md)).
2.  Enumera il contenuto della cartella ([Enumerazione del contenuto di una cartella](folder-info.md)).
3.  Determina tutti i nomi visualizzati e li stampa ([Determinazione dei nomi visualizzati e altre proprietà](folder-info.md)).
4.  Cerca una sottocartella ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).
5.  Esegue l'associazione alla prima sottocartella trovata ( Recupero di un puntatore[all'interfaccia IShellFolder di una sottocartella).](folder-info.md)
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



 

 

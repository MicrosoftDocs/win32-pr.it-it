---
title: Salvataggio di profili
description: Salvataggio di profili
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows Media Format SDK, salvataggio di profili
- Windows Media Format SDK, salvataggio del profilo
- profili, salvataggio
- profili,interfaccia IWMProfileManager
- IWMProfileManager, salvataggio di profili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6befb09d7e0d628462bdd22e1e905c351be58dc077959089883ce3707dc493d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547041"
---
# <a name="saving-profiles"></a>Salvataggio di profili

È possibile usare il [**metodo IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) per salvare il contenuto di un oggetto profilo in una stringa formattata con XML. Non vengono forniti metodi per archiviare la stringa del profilo in un file. è possibile usare le routine di I/O di file di propria scelta.

> [!Note]  
> Non modificare mai la stringa del profilo scritta in un file. Le modifiche da apportare a un profilo devono essere apportate a livello di codice. La modifica dei valori in un file con estensione prx può causare risultati imprevedibili.

 

L'esempio seguente è una funzione per salvare un profilo in un file usando I/O standard di file di tipo C. Per compilare un'applicazione che usa questo esempio, è necessario includere stdio.h nel progetto.


```C++
HRESULT ProfileToFile(IWMProfileManager* pProfileMgr, 
                      IWMProfile* pProfile)
{
    HRESULT hr = S_OK;

    FILE*   pFile;
    
    WCHAR*  pwszProfileString = NULL;
    DWORD   cchProfileString = 0;

    // Save the profile to a string.
    // First, retrieve the size of the string required.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  NULL, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not get the profile string size.");
        return hr;
    }

    // Allocate memory to hold the string.
    pwszProfileString = new WCHAR[cchProfileString];

    if(pwszProfileString == NULL)
    {
        printf("Could not allocate memory for the profile string.");
        return E_OUTOFMEMORY;
    }

    // Retrieve the string.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  pwszProfileString, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not save the profile string.");
        return hr;
    }

    // Create the output file.
    pFile = fopen("MyProfile.prx", "w");

    // Write the profile string to the file.
    fprintf(pFile, "%S\n", pwszProfileString);

    // Close the file.
    fclose(pFile);

    delete[] pwszProfileString;

    return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> </dl>

 

 





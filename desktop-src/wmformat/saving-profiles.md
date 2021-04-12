---
title: Salvataggio di profili
description: Salvataggio di profili
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows Media Format SDK, salvataggio di profili
- Windows Media Format SDK, salvataggio del profilo
- profili, salvataggio
- profili, interfaccia IWMProfileManager
- IWMProfileManager, salvataggio di profili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276b002f0b7f98de2e84f2c27a4f52bde25726bb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398551"
---
# <a name="saving-profiles"></a><span data-ttu-id="e5900-108">Salvataggio di profili</span><span class="sxs-lookup"><span data-stu-id="e5900-108">Saving Profiles</span></span>

<span data-ttu-id="e5900-109">È possibile usare il metodo [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) per salvare il contenuto di un oggetto profilo in una stringa formattata con XML.</span><span class="sxs-lookup"><span data-stu-id="e5900-109">You can use the [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) method to save the contents of a profile object to a string formatted with XML.</span></span> <span data-ttu-id="e5900-110">Nessun metodo fornito per archiviare la stringa del profilo in un file; è possibile usare le routine di I/O dei file di propria scelta.</span><span class="sxs-lookup"><span data-stu-id="e5900-110">No methods are provided to store the profile string to a file; you can use the file I/O routines of your choice.</span></span>

> [!Note]  
> <span data-ttu-id="e5900-111">Non modificare mai la stringa del profilo scritta in un file.</span><span class="sxs-lookup"><span data-stu-id="e5900-111">You should never alter the profile string written to a file.</span></span> <span data-ttu-id="e5900-112">Tutte le modifiche da apportare a un profilo devono essere apportate a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="e5900-112">Any changes you want to make to a profile should be made programmatically.</span></span> <span data-ttu-id="e5900-113">La modifica dei valori in un file con estensione prx può causare risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="e5900-113">Changing values in a .prx file can cause unpredictable results.</span></span>

 

<span data-ttu-id="e5900-114">L'esempio seguente è una funzione per salvare un profilo in un file usando l'I/O di file di tipo C standard.</span><span class="sxs-lookup"><span data-stu-id="e5900-114">The following example is a function to save a profile to a file using standard C-style file I/O.</span></span> <span data-ttu-id="e5900-115">Per compilare un'applicazione che usa questo esempio, è necessario includere STDIO. h nel progetto.</span><span class="sxs-lookup"><span data-stu-id="e5900-115">To compile an application that uses this example, you must include stdio.h in your project.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e5900-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5900-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5900-117">**Utilizzo dei profili**</span><span class="sxs-lookup"><span data-stu-id="e5900-117">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 





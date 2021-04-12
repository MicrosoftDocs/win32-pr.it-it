---
title: Per modificare le versioni del profilo di sistema
description: Per modificare le versioni del profilo di sistema
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- profili, sistema
- profili di sistema, versioni
- profili di sistema, modifica delle versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824e2b1cf4a43cef0e87daa461c6510a6672472d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336369"
---
# <a name="to-change-system-profile-versions"></a><span data-ttu-id="ca20f-106">Per modificare le versioni del profilo di sistema</span><span class="sxs-lookup"><span data-stu-id="ca20f-106">To Change System Profile Versions</span></span>

<span data-ttu-id="ca20f-107">Ogni volta che si crea un oggetto di gestione profili, analizza i profili di sistema.</span><span class="sxs-lookup"><span data-stu-id="ca20f-107">Whenever you create a profile manager object, it parses the system profiles.</span></span> <span data-ttu-id="ca20f-108">È possibile scorrere i profili di sistema usando i metodi [**IWMProfileManager:: GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**IWMProfileManager:: LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) , ma gestione profili consentirà di contare ed elencare solo i profili di una sola versione alla volta.</span><span class="sxs-lookup"><span data-stu-id="ca20f-108">You can iterate through the system profiles using the [**IWMProfileManager::GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods, but the profile manager will count and list only the profiles of a single version at a time.</span></span> <span data-ttu-id="ca20f-109">Se si vuole usare questo metodo per trovare i profili di sistema, è necessario assicurarsi che il gestore del profilo occupi la versione desiderata.</span><span class="sxs-lookup"><span data-stu-id="ca20f-109">If you want to use this method of finding system profiles, you need to ensure that the profile manger deals with the version you want.</span></span> <span data-ttu-id="ca20f-110">Utilizzare i metodi dell'interfaccia [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) per impostare e recuperare la versione del profilo di sistema utilizzata da Gestione profili.</span><span class="sxs-lookup"><span data-stu-id="ca20f-110">Use the methods of the [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) interface to set and retrieve the system profile version used by the profile manager.</span></span>

<span data-ttu-id="ca20f-111">Le versioni vengono specificate usando i membri del tipo di enumerazione della [**\_ versione WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) .</span><span class="sxs-lookup"><span data-stu-id="ca20f-111">Versions are specified using the members of the [**WMT\_VERSION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) enumeration type.</span></span> <span data-ttu-id="ca20f-112">Se si imposta la versione del profilo di sistema su WMT \_ ver \_ 9 \_ 0, la chiamata avrà esito positivo, ma il conteggio del profilo di sistema sarà zero.</span><span class="sxs-lookup"><span data-stu-id="ca20f-112">If you set the system profile version to WMT\_VER\_9\_0, the call will succeed, but the system profile count will be zero.</span></span> <span data-ttu-id="ca20f-113">Questo perché nessun profilo di sistema predefinito usa i codec della serie Windows Media Audio e video 9.</span><span class="sxs-lookup"><span data-stu-id="ca20f-113">This is because no predefined system profiles use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="ca20f-114">Per ulteriori informazioni sull'aggiornamento dei profili per l'utilizzo dei codec più recenti, vedere [riutilizzo delle configurazioni di flusso](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="ca20f-114">For more information about updating profiles to use the newest codecs, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

<span data-ttu-id="ca20f-115">Se si carica un profilo di sistema in base al relativo identificatore GUID, la versione del profilo di sistema utilizzata da Profile Manager non è rilevante.</span><span class="sxs-lookup"><span data-stu-id="ca20f-115">If you load a system profile by its GUID identifier, it does not matter which system profile version the profile manager is using.</span></span> <span data-ttu-id="ca20f-116">Per ulteriori informazioni sul caricamento dei profili di sistema, vedere [per caricare un profilo di sistema](to-load-a-system-profile.md).</span><span class="sxs-lookup"><span data-stu-id="ca20f-116">For more information about loading system profiles, see [To Load a System Profile](to-load-a-system-profile.md).</span></span>

<span data-ttu-id="ca20f-117">Nell'esempio di codice seguente viene illustrato come impostare e recuperare la versione del profilo di sistema.</span><span class="sxs-lookup"><span data-stu-id="ca20f-117">The following example code shows how to set and retrieve the system profile version.</span></span> <span data-ttu-id="ca20f-118">Questo esempio USA printf per l'output della console e richiede l'inclusione di stdio. h.</span><span class="sxs-lookup"><span data-stu-id="ca20f-118">This example uses printf for console output and requires stdio.h to be included.</span></span> <span data-ttu-id="ca20f-119">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ca20f-119">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
int main(void)
{
    HRESULT hr = S_OK;

    IWMProfileManager*  pProfileMgr  = NULL;
    IWMProfileManager2* pProfileMgr2 = NULL;

    WMT_VERSION         profileVersion;

    // Initialize COM.
    hr = CoInitialize(NULL);
    if(FAILED(hr))
    {
        printf("Could not initialize COM.");
        return 0;
    }

    // Create a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    if(FAILED(hr))
    {
        printf("Could not create a profile manager object.");
        return 0;
    }

    // Get the IWMProfileManager2 interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManager2, 
                                     (void**) &pProfileMgr2);
    if(FAILED(hr))
    {
        printf("Could not get the IWMProfileManager2 interface.");
        SAFE_RELEASE(pProfileMgr);
        return 0;
    }

    // Release the old interface.
    SAFE_RELEASE(pProfileMgr);

    // Get the current system profile version.
    hr = pProfileMgr2->GetSystemProfileVersion(&profileVersion);
    if(FAILED(hr))
    {
        printf("Could not retrieve profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }
    
    // Display the current version.
    printf("Current version: ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Set the system profile version to 8.
    profileVersion = WMT_VER_8_0;

    hr = pProfileMgr2->SetSystemProfileVersion(profileVersion);
    if(FAILED(hr))
    {
        printf("Could not change profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }

    // Print verification.
    printf("Successfully set version to ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Clean up.
    SAFE_RELEASE(pProfileMgr2);
}
```



## <a name="related-topics"></a><span data-ttu-id="ca20f-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca20f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca20f-121">**Uso dei profili di sistema**</span><span class="sxs-lookup"><span data-stu-id="ca20f-121">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 





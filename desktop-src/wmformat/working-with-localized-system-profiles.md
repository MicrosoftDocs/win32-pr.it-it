---
title: Utilizzo dei profili di sistema localizzati
description: Utilizzo dei profili di sistema localizzati
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- profili, sistema
- profili di sistema, localizzati
- profili di sistema, interfaccia IWMProfileManagerLanguage
- profili di sistema localizzati, informazioni
- IWMProfileManagerLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8c040d9804cd822b17e7caad8a8cfb5e5854c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299395"
---
# <a name="working-with-localized-system-profiles"></a><span data-ttu-id="7ce10-108">Utilizzo dei profili di sistema localizzati</span><span class="sxs-lookup"><span data-stu-id="7ce10-108">Working with Localized System Profiles</span></span>

<span data-ttu-id="7ce10-109">Windows Media Format SDK include i profili di sistema con nomi e descrizioni in diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="7ce10-109">The Windows Media Format SDK includes system profiles with names and descriptions in several languages.</span></span> <span data-ttu-id="7ce10-110">I file con estensione prx del profilo di sistema localizzati vengono installati nella \[ \] \\ cartella sdkroot WMSDK \\ WMFSDK9 \\ LocalizedProfiles</span><span class="sxs-lookup"><span data-stu-id="7ce10-110">The localized system profile .prx files are installed into the \[SDKRoot\]\\WMSDK\\WMFSDK9\\LocalizedProfiles folder.</span></span> <span data-ttu-id="7ce10-111">Per accedere a un file specifico con i metodi **IWMProfileManagerLanguage** , è necessario spostarlo nella directory radice del sistema insieme agli altri file del profilo di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ce10-111">To access a particular file with the **IWMProfileManagerLanguage** methods, you must move it into the system root directory along with the other system profile files.</span></span> <span data-ttu-id="7ce10-112">Per un elenco dei file del profilo di sistema localizzati, vedere [profili di sistema localizzati](localized-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="7ce10-112">For a list of the localized system profile files, see [Localized System Profiles](localized-system-profiles.md).</span></span>

<span data-ttu-id="7ce10-113">È possibile impostare o recuperare il linguaggio del profilo di sistema utilizzando i metodi dell'interfaccia [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) .</span><span class="sxs-lookup"><span data-stu-id="7ce10-113">You can set or retrieve the system profile language using the methods of the [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) interface.</span></span> <span data-ttu-id="7ce10-114">Il linguaggio viene specificato come valore LANGID, che è costituito da un identificatore di lingua principale e un identificatore della lingua secondaria.</span><span class="sxs-lookup"><span data-stu-id="7ce10-114">The language is specified as a LANGID value, which consists of a primary language identifier and a secondary language identifier.</span></span> <span data-ttu-id="7ce10-115">Nel codice seguente viene illustrato come recuperare il linguaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="7ce10-115">The following code demonstrates how to retrieve the current language.</span></span> <span data-ttu-id="7ce10-116">La lingua predefinita è U.S. English (0x409).</span><span class="sxs-lookup"><span data-stu-id="7ce10-116">The default language is U.S. English (0x409).</span></span> <span data-ttu-id="7ce10-117">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="7ce10-117">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetCurrentSystemProfileLanguage(IMWProfilManager* pProfileMgr)
{
    HRESULT hr = S_OK;

    IWMProfileManagerLanguage* pProfileMgrLang = NULL;

    // Get the profile manager language interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManagerLanguage,
                                     (void **) &pProfileMgrLang);
    if(FAILED(hr))
    {
        printf("Couldn't get IWMProfileManagerLanguage.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    // Retrieve the current language (as a LANGID value)
    WORD wLangID = 0;
    hr = pProfileMgrLang->GetUserLanguageID(&wLangID);
    if(FAILED(hr))
    {
        printf("Could not get the current language.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    printf("The current language ID is 0x%X\n", wLangID);

    SAFE_RELEASE(pProfileMgrLang);
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="7ce10-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ce10-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ce10-119">**Uso dei profili di sistema**</span><span class="sxs-lookup"><span data-stu-id="7ce10-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 





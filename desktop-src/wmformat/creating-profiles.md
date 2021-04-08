---
title: Creazione di profili
description: Creazione di profili
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media Format SDK, profili
- profili, creazione
- profili, interfaccia IWMProfileManager
- IWMProfileManager, creazione di profili
- profili, funzione WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046279"
---
# <a name="creating-profiles"></a><span data-ttu-id="6b89f-109">Creazione di profili</span><span class="sxs-lookup"><span data-stu-id="6b89f-109">Creating Profiles</span></span>

<span data-ttu-id="6b89f-110">In molti casi, è possibile creare un profilo vuoto da configurare in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6b89f-110">In many cases, you will want to create an empty profile to configure for your needs.</span></span> <span data-ttu-id="6b89f-111">In altri casi è più semplice modificare un profilo esistente, ad esempio un profilo di sistema.</span><span class="sxs-lookup"><span data-stu-id="6b89f-111">In other cases it is easier to edit an existing profile, like a system profile.</span></span> <span data-ttu-id="6b89f-112">Per ulteriori informazioni sull'utilizzo dei profili di sistema, vedere [using System Profiles](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6b89f-112">For more information about using system profiles, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="6b89f-113">La creazione di un profilo vuoto, pronto per la configurazione, richiede un oggetto gestore profili.</span><span class="sxs-lookup"><span data-stu-id="6b89f-113">Creating an empty profile, ready for you to configure, requires a profile manager object.</span></span> <span data-ttu-id="6b89f-114">Per ottenere l'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) di un oggetto di gestione profilo, chiamare la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="6b89f-114">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>

<span data-ttu-id="6b89f-115">Per creare un profilo vuoto, chiamare [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="6b89f-115">To create an empty profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span> <span data-ttu-id="6b89f-116">Quando si crea un profilo vuoto, l'unica cosa specificata è la versione di Windows Media Format SDK con cui è conforme il profilo.</span><span class="sxs-lookup"><span data-stu-id="6b89f-116">When you create an empty profile, the only thing you specify is the version of the Windows Media Format SDK with which the profile complies.</span></span> <span data-ttu-id="6b89f-117">A meno che non sia necessario usare una versione precedente, è sempre necessario usare la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="6b89f-117">Unless you have a specific need to use a previous version, you should always use the latest version.</span></span> <span data-ttu-id="6b89f-118">La versione impone la struttura del profilo; le versioni precedenti non supportavano alcune proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b89f-118">The version dictates the structure of the profile; previous versions did not support some properties.</span></span>

<span data-ttu-id="6b89f-119">Nell'esempio di codice seguente viene illustrato come creare un nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="6b89f-119">The following example code shows how to create a new profile.</span></span> <span data-ttu-id="6b89f-120">Per compilare il codice nell'applicazione, includere STDIO. h.</span><span class="sxs-lookup"><span data-stu-id="6b89f-120">To compile this code in your application, include stdio.h.</span></span> <span data-ttu-id="6b89f-121">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="6b89f-121">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="6b89f-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b89f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b89f-123">**Interfaccia IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="6b89f-123">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="6b89f-124">**Interfaccia IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="6b89f-124">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="6b89f-125">**Utilizzo dei profili**</span><span class="sxs-lookup"><span data-stu-id="6b89f-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 





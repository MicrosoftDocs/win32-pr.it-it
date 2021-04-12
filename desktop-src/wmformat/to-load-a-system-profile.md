---
title: Per caricare un profilo di sistema
description: Per caricare un profilo di sistema
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- profili, sistema
- profili di sistema, caricamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398581"
---
# <a name="to-load-a-system-profile"></a><span data-ttu-id="be960-105">Per caricare un profilo di sistema</span><span class="sxs-lookup"><span data-stu-id="be960-105">To Load a System Profile</span></span>

<span data-ttu-id="be960-106">Per apportare modifiche a un profilo di sistema, è necessario caricarlo in un oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="be960-106">To make changes to a system profile, you must load it into a profile object.</span></span> <span data-ttu-id="be960-107">Gestione profili fornisce due opzioni per il caricamento dei profili di sistema: per identificatore e per indice.</span><span class="sxs-lookup"><span data-stu-id="be960-107">The profile manager provides two options for loading system profiles: by identifier, and by index.</span></span>

<span data-ttu-id="be960-108">Un identificatore del profilo di sistema è un valore GUID assegnato al profilo di sistema al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="be960-108">A system profile identifier is a GUID value assigned to the system profile when it was created.</span></span> <span data-ttu-id="be960-109">Per un elenco delle costanti GUID associate ai profili di sistema versione 8, vedere profili di [sistema](system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="be960-109">For a list of the GUID constants associated with the version 8 system profiles, see [System Profiles](system-profiles.md).</span></span> <span data-ttu-id="be960-110">È possibile trovare le costanti GUID per le versioni precedenti nel file di intestazione WMSysPrf. h.</span><span class="sxs-lookup"><span data-stu-id="be960-110">You can find the GUID constants for previous versions in the header file WMSysPrf.h.</span></span> <span data-ttu-id="be960-111">Per ulteriori informazioni su questo e altri file di intestazione inclusi con Windows Media Format SDK, vedere [file di libreria e impostazioni del compilatore](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="be960-111">For more information about this and other header files included with the Windows Media Format SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

<span data-ttu-id="be960-112">Nell'esempio di codice seguente viene illustrato come caricare un profilo di sistema utilizzando l'identificatore del profilo di sistema.</span><span class="sxs-lookup"><span data-stu-id="be960-112">The following example code demonstrates how to load a system profile using the system profile identifier.</span></span> <span data-ttu-id="be960-113">Per il corretto funzionamento di questo codice, è necessario includere WMSysPrf. h e stdio. h.</span><span class="sxs-lookup"><span data-stu-id="be960-113">For this code to work, you must include WMSysPrf.h and stdio.h.</span></span> <span data-ttu-id="be960-114">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="be960-114">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



<span data-ttu-id="be960-115">Se non si conosce il profilo che si vuole usare, è possibile scorrere tutti i profili di sistema di una determinata versione usando i metodi [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) dell'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="be960-115">If you do not know which profile you want to use, you can iterate through all of the system profiles of a particular version using the [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="be960-116">Questi metodi gestiscono solo una versione dei profili di sistema alla volta.</span><span class="sxs-lookup"><span data-stu-id="be960-116">These methods only deal with one version of the system profiles at a time.</span></span> <span data-ttu-id="be960-117">Per ulteriori informazioni sulla modifica della versione del profilo di sistema, vedere [per modificare le versioni del profilo di sistema](to-change-system-profile-versions.md).</span><span class="sxs-lookup"><span data-stu-id="be960-117">For more information about changing the system profile version, see [To Change System Profile Versions](to-change-system-profile-versions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="be960-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be960-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be960-119">**Uso dei profili di sistema**</span><span class="sxs-lookup"><span data-stu-id="be960-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 





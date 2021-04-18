---
description: Registrazione di un DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registrazione di un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303899"
---
# <a name="registering-a-dmo"></a><span data-ttu-id="4ec6b-103">Registrazione di un DMO</span><span class="sxs-lookup"><span data-stu-id="4ec6b-103">Registering a DMO</span></span>

<span data-ttu-id="4ec6b-104">Per consentire ai client di usare DMO, il CLSID deve essere registrato nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-104">In order for clients to use your DMO, the CLSID must be registered on the user's system.</span></span> <span data-ttu-id="4ec6b-105">Questa operazione viene eseguita tramite la funzione **DllRegisterServer** della dll.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-105">This is done through the DLL's **DllRegisterServer** function.</span></span> <span data-ttu-id="4ec6b-106">Se si utilizza il Active Template Library (ATL), questa funzione viene generata automaticamente dalla procedura guidata ATL.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-106">If you are using the Active Template Library (ATL), the ATL wizard automatically generates this function.</span></span>

<span data-ttu-id="4ec6b-107">È anche possibile registrare il DMO in una o più categorie DMO standard.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-107">You can also register your DMO under one or more standard DMO categories.</span></span> <span data-ttu-id="4ec6b-108">Questo consente ai client di individuare il DMO usando la funzione [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="4ec6b-108">This enables clients to discover your DMO using the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span> <span data-ttu-id="4ec6b-109">Le categorie sono definite dal GUID e sono elencate nella sezione [GUID DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="4ec6b-109">The categories are defined by GUID, and are listed in the section [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="4ec6b-110">La registrazione di un DMO in una categoria è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-110">Registering a DMO under a category is optional.</span></span> <span data-ttu-id="4ec6b-111">A tale scopo, chiamare la funzione [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) e specificare il nome descrittivo di DMO, il CLSID e la categoria.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-111">To do so, call the [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) function and specify the friendly name of the DMO, the CLSID, and the category.</span></span> <span data-ttu-id="4ec6b-112">Facoltativamente, è anche possibile registrare un set di tipi di supporto supportati dal DMOs.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-112">Optionally, you can also register a set of media types that your DMOs supports.</span></span> <span data-ttu-id="4ec6b-113">Per ulteriori informazioni, vedere [DMO media types](dmo-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="4ec6b-113">For more information, see [DMO Media Types](dmo-media-types.md).</span></span>

<span data-ttu-id="4ec6b-114">Nell'esempio seguente viene illustrato come registrare un valore DMO (audio Effect) che supporta l'input e l'output audio PCM.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-114">The following example shows how to register an audio effect DMO that supports PCM audio input and output.</span></span> <span data-ttu-id="4ec6b-115">In questo caso i tipi di input e di output sono uguali.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-115">In this case the input types and output types are the same.</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



<span data-ttu-id="4ec6b-116">In questo esempio si presuppone che ATL sia stato utilizzato per creare il progetto. L'ultima riga della funzione chiama il metodo standard ATL per registrare il server COM.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-116">This example assumes that ATL was used to create the project; the last line of the function calls the standard ATL method to register the COM server.</span></span> <span data-ttu-id="4ec6b-117">Se non si usa ATL, l'aspetto della funzione sarà diverso.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-117">If you are not using ATL, your function will look different.</span></span>

<span data-ttu-id="4ec6b-118">**Annullamento della registrazione di un DMO**</span><span class="sxs-lookup"><span data-stu-id="4ec6b-118">**Unregistering a DMO**</span></span>

<span data-ttu-id="4ec6b-119">La funzione **DllUnregisterServer** deve rimuovere qualsiasi voce del registro di sistema creata dalla funzione **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="4ec6b-119">Your **DllUnregisterServer** function must remove any registry entries that the **DllRegisterServer** function creates.</span></span> <span data-ttu-id="4ec6b-120">Se si chiama **DMORegister** quando si registra DMO, è necessario [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) con la stessa categoria quando si annulla la registrazione di DMO.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-120">If you call **DMORegister** when you register the DMO, you must [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) with the same category when you unregister the DMO.</span></span>

<span data-ttu-id="4ec6b-121">Nell'esempio seguente vengono rimosse le voci del registro di sistema create nell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="4ec6b-121">The following example removes the registry entries created in the previous example:</span></span>


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



<span data-ttu-id="4ec6b-122">**Valori Merit di DirectShow**</span><span class="sxs-lookup"><span data-stu-id="4ec6b-122">**DirectShow Merit Values**</span></span>

<span data-ttu-id="4ec6b-123">Ai fini della creazione di grafici di filtro, DirectShow assegna un valore Merit predefinito a DMOs.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-123">For purposes of building filter graphs, DirectShow assigns a default merit value to DMOs.</span></span> <span data-ttu-id="4ec6b-124">È possibile eseguire l'override di questo valore aggiungendo una voce del registro di sistema alla chiave del registro di sistema DMO nel \_ CLSID radice delle classi HKEY \_ \\ .</span><span class="sxs-lookup"><span data-stu-id="4ec6b-124">You can override this value by adding a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="4ec6b-125">Includere un valore **DWORD** denominato `Merit` il cui valore specifichi il merito.</span><span class="sxs-lookup"><span data-stu-id="4ec6b-125">Include a **DWORD** value named `Merit` whose value specifies the merit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ec6b-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ec6b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ec6b-127">Scrittura di un DMO</span><span class="sxs-lookup"><span data-stu-id="4ec6b-127">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 




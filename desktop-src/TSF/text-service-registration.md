---
title: Registrazione del servizio di testo
description: Oltre alle voci del registro di sistema COM standard del server in-process, un servizio di testo deve registrarsi con il Framework di servizi di testo (TSF), in modo che possa essere usato con un'applicazione.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Framework servizi di testo (TSF), registrazione
- TSF (Framework di servizi di testo), registrazione
- Servizi di testo, registrazione
- Framework servizi di testo (TSF), profili linguaggio
- TSF (Framework dei servizi di testo), profili di linguaggio
- Servizi di testo, profili di linguaggio
- Framework servizi di testo (TSF), categorie
- TSF (Framework di servizi di testo), categorie
- Servizi di testo, categorie
- registrazione di servizi di testo
- registrazione dei profili di linguaggio
- registrazione di categorie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473627"
---
# <a name="text-service-registration"></a><span data-ttu-id="e0b69-115">Registrazione del servizio di testo</span><span class="sxs-lookup"><span data-stu-id="e0b69-115">Text Service Registration</span></span>

<span data-ttu-id="e0b69-116">Oltre alle voci del registro di sistema COM standard del server in-process, un servizio di testo deve registrarsi con il Framework di servizi di testo (TSF), in modo che possa essere usato con un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e0b69-116">In addition to the standard COM in-proc server registry entries, a text service must register itself with the Text Services Framework (TSF) so that it can be available for use with an application.</span></span> <span data-ttu-id="e0b69-117">TSF fornisce l'interfaccia [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) e [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) per semplificare il processo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e0b69-117">TSF supplies the [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) and [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) interface to simplify the registration process.</span></span>

<span data-ttu-id="e0b69-118">I provider di servizi di testo devono inoltre fornire firme digitali con i rispettivi file eseguibili binari.</span><span class="sxs-lookup"><span data-stu-id="e0b69-118">Text service providers should also provide digital signatures with their binary executables.</span></span> <span data-ttu-id="e0b69-119">Vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e0b69-119">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="registering-the-text-service"></a><span data-ttu-id="e0b69-120">Registrazione del servizio di testo</span><span class="sxs-lookup"><span data-stu-id="e0b69-120">Registering the Text Service</span></span>

<span data-ttu-id="e0b69-121">Un servizio di testo si registra con TSF chiamando [ITfInputProcessorProfiles:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) con l'identificatore di classe del servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="e0b69-121">A text service registers itself with TSF by calling [ITfInputProcessorProfiles::Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) with the class identifier of the text service.</span></span> <span data-ttu-id="e0b69-122">Un'istanza dell'interfaccia **ITfInputProcessorProfiles** viene ottenuta chiamando **CoCreateInstance** con CLSID \_ tf \_ InputProcessorProfiles.</span><span class="sxs-lookup"><span data-stu-id="e0b69-122">An instance of the **ITfInputProcessorProfiles** interface is obtained by calling **CoCreateInstance** with CLSID\_TF\_InputProcessorProfiles.</span></span>

<span data-ttu-id="e0b69-123">Nell'esempio seguente viene illustrato come creare un oggetto **ITfInputProcessorProfiles** e registrare il servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="e0b69-123">The following example demonstrates how to create an **ITfInputProcessorProfiles** object and register the text service.</span></span>


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[<span data-ttu-id="e0b69-124">ITfInputProcessorProfiles:: Annulla registrazione</span><span class="sxs-lookup"><span data-stu-id="e0b69-124">ITfInputProcessorProfiles::Unregister</span></span>](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a><span data-ttu-id="e0b69-125">Registrazione dei profili di linguaggio</span><span class="sxs-lookup"><span data-stu-id="e0b69-125">Registering Language Profiles</span></span>

<span data-ttu-id="e0b69-126">Un servizio di testo è disponibile solo quando un'applicazione ha lo stato attivo e la lingua corretta è selezionata nella barra della lingua.</span><span class="sxs-lookup"><span data-stu-id="e0b69-126">A text service is only available when an application has the focus and the proper language is selected in the language bar.</span></span> <span data-ttu-id="e0b69-127">Per semplificare questa operazione, TSF richiede che un servizio di testo si registri per tutte le lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="e0b69-127">To facilitate this, TSF requires that a text service register itself for all of the languages that it supports.</span></span> <span data-ttu-id="e0b69-128">Il servizio di testo registra i profili di linguaggio chiamando [ITfInputProcessorProfiles:: AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) con l'identificatore della classe del servizio di testo, l'identificatore di lingua del profilo e un **GUID** definito dal servizio di testo che identifica il profilo del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="e0b69-128">The text service registers its language profiles by calling [ITfInputProcessorProfiles::AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) with the text service class identifier, that language identifier of the profile, and a text service defined **GUID** that identifies the language profile.</span></span>

<span data-ttu-id="e0b69-129">È possibile rimuovere un profilo del linguaggio chiamando [ITfInputProcessorProfiles:: RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span><span class="sxs-lookup"><span data-stu-id="e0b69-129">A language profile can be removed by calling [ITfInputProcessorProfiles::RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span></span> <span data-ttu-id="e0b69-130">**ITfInputProcessorProfiles:: Unregister** rimuove tutti i profili di linguaggio per il servizio di testo; Quando viene disinstallato, un servizio di testo richiede la rimozione dei singoli profili di linguaggio.</span><span class="sxs-lookup"><span data-stu-id="e0b69-130">**ITfInputProcessorProfiles::Unregister** removes all language profiles for the text service; when a text service is uninstalled, it does require removal of the individual language profiles.</span></span>

## <a name="registering-categories"></a><span data-ttu-id="e0b69-131">Registrazione di categorie</span><span class="sxs-lookup"><span data-stu-id="e0b69-131">Registering Categories</span></span>

<span data-ttu-id="e0b69-132">Un servizio di testo deve inoltre registrare la categoria a cui si applica il servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="e0b69-132">A text service must also register the category that the text service applies to.</span></span> <span data-ttu-id="e0b69-133">Se, ad esempio, il servizio di testo fornisce informazioni sugli attributi di visualizzazione, è necessario registrarsi come provider di attributi di visualizzazione chiamando [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con l'identificatore di classe del servizio di testo per il primo parametro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER per il secondo parametro e l'identificatore di classe del servizio di testo per il terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="e0b69-133">For example, if the text service supplies display attribute information, it must register itself as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span> <span data-ttu-id="e0b69-134">Le categorie possibili sono elencate in [valori di categoria predefiniti](predefined-category-values.md).</span><span class="sxs-lookup"><span data-stu-id="e0b69-134">The possible categories are listed under [Predefined Category Values](predefined-category-values.md).</span></span>

<span data-ttu-id="e0b69-135">Rimuovere le categorie registrate in precedenza chiamando [ITfCategoryMgr:: UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span><span class="sxs-lookup"><span data-stu-id="e0b69-135">Remove previously registered categories by calling [ITfCategoryMgr::UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span></span> <span data-ttu-id="e0b69-136">ITfInputProcessorProfiles:: Unregister rimuove tutte le categorie per il servizio di testo; Quando viene disinstallato un servizio di testo, è necessario rimuovere le singole categorie.</span><span class="sxs-lookup"><span data-stu-id="e0b69-136">ITfInputProcessorProfiles::Unregister removes all categories for the text service; when a text service is uninstalled, it must remove the individual categories.</span></span>

 

 
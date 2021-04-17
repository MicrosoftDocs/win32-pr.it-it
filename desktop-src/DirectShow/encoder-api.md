---
description: API del codificatore
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API del codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401285"
---
# <a name="encoder-api"></a><span data-ttu-id="91643-103">API del codificatore</span><span class="sxs-lookup"><span data-stu-id="91643-103">Encoder API</span></span>

<span data-ttu-id="91643-104">L'API del codificatore fornisce un'interfaccia uniforme per la configurazione dei codificatori software e hardware.</span><span class="sxs-lookup"><span data-stu-id="91643-104">The Encoder API provides a uniform interface for configuring software and hardware encoders.</span></span> <span data-ttu-id="91643-105">Le applicazioni possono usare l'API del codificatore per configurare un codificatore e archiviare le impostazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="91643-105">Applications can use the Encoder API to configure an encoder and to store the configuration settings.</span></span> <span data-ttu-id="91643-106">I fornitori del codificatore possono utilizzare l'API del codificatore per esporre le funzionalità di un codificatore.</span><span class="sxs-lookup"><span data-stu-id="91643-106">Encoder vendors can use the Encoder API to expose the capabilities of an encoder.</span></span> <span data-ttu-id="91643-107">Anche se l'API del codificatore è progettata principalmente per i codificatori, è sufficiente che i decodificatori possano supportarla.</span><span class="sxs-lookup"><span data-stu-id="91643-107">Although the Encoder API is designed primarily for encoders, it is general enough that decoders can support it as well.</span></span>

<span data-ttu-id="91643-108">L'API del codificatore viene esposta alle applicazioni tramite l'interfaccia [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , esposta dal filtro del codificatore.</span><span class="sxs-lookup"><span data-stu-id="91643-108">The Encoder API is exposed to applications through the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface, which is exposed by the encoder filter.</span></span> <span data-ttu-id="91643-109">Il filtro del codificatore può essere un filtro DirectShow nativo, un codificatore hardware o un oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="91643-109">The encoder filter may be a native DirectShow filter, a hardware encoder, or a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="91643-110">Filtri software: un codificatore implementato come filtro DirectShow nativo deve esporre direttamente il [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="91643-110">Software filters: An encoder that is implemented as a native DirectShow filter should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directly.</span></span>
-   <span data-ttu-id="91643-111">Codificatori hardware: il dispositivo di codifica viene esposto tramite uno o più i Minidriver AVStream, che sono rappresentati in modalità utente da KSProxy.</span><span class="sxs-lookup"><span data-stu-id="91643-111">Hardware encoders: The encoding device is exposed through one or more AVStream minidrivers, which are represented in user mode by KSProxy.</span></span> <span data-ttu-id="91643-112">KSProxy converte le chiamate al metodo [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) in set di proprietà KS.</span><span class="sxs-lookup"><span data-stu-id="91643-112">KSProxy translates [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) method calls into KS property sets.</span></span> <span data-ttu-id="91643-113">Per ulteriori informazioni, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="91643-113">For more information, see the DDK documentation.</span></span>
-   <span data-ttu-id="91643-114">DMOs: DMO deve esporre l'interfaccia [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="91643-114">DMOs: The DMO should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="91643-115">Le applicazioni DirectShow possono eseguire query sul filtro del wrapper DMO, che espone l'interfaccia aggregando DMO.</span><span class="sxs-lookup"><span data-stu-id="91643-115">DirectShow applications can query the DMO Wrapper filter, which exposes the interface by aggregating the DMO.</span></span> <span data-ttu-id="91643-116">Le applicazioni non basate su DirectShow possono eseguire query direttamente su DMO.</span><span class="sxs-lookup"><span data-stu-id="91643-116">Applications not based on DirectShow can query the DMO directly.</span></span>

### <a name="encoder-capabilties"></a><span data-ttu-id="91643-117">Avanzata codificatore</span><span class="sxs-lookup"><span data-stu-id="91643-117">Encoder Capabilties</span></span>

<span data-ttu-id="91643-118">Un codificatore può registrare un elenco di funzionalità di alto livello archiviando tali funzionalità nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="91643-118">An encoder can register a list of high-level capabilities by storing them in the system registry.</span></span> <span data-ttu-id="91643-119">Ogni funzionalità è identificata da un GUID.</span><span class="sxs-lookup"><span data-stu-id="91643-119">Each capability is identified by a GUID.</span></span> <span data-ttu-id="91643-120">Per enumerare le funzionalità di un determinato codificatore, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="91643-120">To enumerate the capabilities of a particular encoder, do the following:</span></span>

1.  <span data-ttu-id="91643-121">Creare il moniker che rappresenta il filtro del codificatore.</span><span class="sxs-lookup"><span data-stu-id="91643-121">Create the moniker that represents the encoder filter.</span></span> <span data-ttu-id="91643-122">Vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="91643-122">(See [Using the System Device Enumerator](using-the-system-device-enumerator.md).)</span></span>
2.  <span data-ttu-id="91643-123">Eseguire una query sul moniker di filtro per l'interfaccia [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .</span><span class="sxs-lookup"><span data-stu-id="91643-123">Query the filter moniker for the [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) interface.</span></span>
3.  <span data-ttu-id="91643-124">Chiamare [**IGetCapabilitiesKey:: GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="91643-124">Call [**IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span></span> <span data-ttu-id="91643-125">Il metodo restituisce un handle per la chiave del registro di sistema che contiene l'elenco delle funzionalità del filtro.</span><span class="sxs-lookup"><span data-stu-id="91643-125">The method returns a handle to the registry key that contains the filter's capabilities list.</span></span>
4.  <span data-ttu-id="91643-126">Chiamare la funzione **RegEnumValue** per enumerare i valori per la chiave restituita.</span><span class="sxs-lookup"><span data-stu-id="91643-126">Call the **RegEnumValue** function to enumerate the values for the returned key.</span></span>

<span data-ttu-id="91643-127">Se si sviluppare un codificatore, creare le voci del registro di sistema per le funzionalità quando il filtro è registrato.</span><span class="sxs-lookup"><span data-stu-id="91643-127">If you are devloping an encoder, create the registry entries for the capabilities when the filter is registered.</span></span> <span data-ttu-id="91643-128">Per i filtri software, creare una chiave denominata **funzionalità** adiacente alle chiavi **FilterData** e **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="91643-128">For software filters, create a key named **Capabilities** that is adjacent to the **FilterData** and **FriendlyName** keys.</span></span> <span data-ttu-id="91643-129">In genere, è necessario aggiungere queste informazioni dopo aver chiamato [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) per registrare i dati del filtro standard.</span><span class="sxs-lookup"><span data-stu-id="91643-129">Typically, you would add this information after calling [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) to register the standard filter data.</span></span> <span data-ttu-id="91643-130">Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="91643-130">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="91643-131">In alternativa, è possibile creare una chiave **CapabilitiesLocation** contenente una stringa che fornisce il percorso della chiave delle **funzionalità** nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="91643-131">Alternatively, you can create a **CapabilitiesLocation** key that contains a string giving the location of the **Capabilities** key in the registry.</span></span> <span data-ttu-id="91643-132">La stringa deve iniziare con "HKLM \\ ", "HKCR \\ " o "HKCU \\ " per indicare il sottoalbero del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="91643-132">The string should start with "HKLM\\", "HKCR\\", or "HKCU\\" to indicate the registry subtree.</span></span> <span data-ttu-id="91643-133">Per i dispositivi Plug and Play, i file di installazione del driver devono creare una chiave delle **funzionalità** accanto alla chiave **FriendlyName** del filtro oppure usare una chiave **CapabilitiesLocation** come descritto per i filtri software.</span><span class="sxs-lookup"><span data-stu-id="91643-133">For Plug and Play devices, the driver's setup files should create a **Capabilities** key adjacent to the filter's **FriendlyName** key, or it can use a **CapabilitiesLocation** key as described for software filters.</span></span>

<span data-ttu-id="91643-134">Dopo aver creato la chiave delle **funzionalità** , creare un valore per ogni GUID della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="91643-134">Once you have created the **Capabilities** key, create a value for each capability GUID.</span></span> <span data-ttu-id="91643-135">Il nome del valore deve essere il formato stringa del GUID, nel formato `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="91643-135">The name of the value should be the string form of the GUID, in the form `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="91643-136">Ogni tipo di valore deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="91643-136">Each value type should be one of the following:</span></span>

-   <span data-ttu-id="91643-137">Singolo valore numerico.</span><span class="sxs-lookup"><span data-stu-id="91643-137">Single numerical value.</span></span> <span data-ttu-id="91643-138">Usare un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="91643-138">Use a **DWORD** value.</span></span>
-   <span data-ttu-id="91643-139">GUID.</span><span class="sxs-lookup"><span data-stu-id="91643-139">GUID.</span></span> <span data-ttu-id="91643-140">Usare il formato stringa del GUID.</span><span class="sxs-lookup"><span data-stu-id="91643-140">Use the string form of the GUID.</span></span>
-   <span data-ttu-id="91643-141">Coppie numeriche.</span><span class="sxs-lookup"><span data-stu-id="91643-141">Numeric pairs.</span></span> <span data-ttu-id="91643-142">Usare una stringa con il formato "a, b" per rappresentare coppie di valori, ad esempio larghezza e altezza, o numeratore e denominatore per le frazioni.</span><span class="sxs-lookup"><span data-stu-id="91643-142">Use a string with the form "a,b" to represent pairs of values, such as width and height, or numerator and denominator for fractions.</span></span>
-   <span data-ttu-id="91643-143">Matrici di valori.</span><span class="sxs-lookup"><span data-stu-id="91643-143">Arrays of values.</span></span> <span data-ttu-id="91643-144">Usare più stringhe (**reg \_ SZ \_ multifunzione**) per rappresentare più di un valore.</span><span class="sxs-lookup"><span data-stu-id="91643-144">Use multi-strings (**REG\_SZ\_MULTI**) to represent more than one value.</span></span>

<span data-ttu-id="91643-145">Nell'esempio seguente viene illustrato il layout del registro di sistema per un filtro software:</span><span class="sxs-lookup"><span data-stu-id="91643-145">The following example shows the registry layout for a software filter:</span></span>


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a><span data-ttu-id="91643-146">Profili codificatore</span><span class="sxs-lookup"><span data-stu-id="91643-146">Encoder Profiles</span></span>

<span data-ttu-id="91643-147">Un *profilo del codificatore* è un elenco fisso di impostazioni di configurazione che possono essere applicate a un codificatore in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="91643-147">An *encoder profile* is a fixed list of configuration settings that can be applied to an encoder at run time.</span></span> <span data-ttu-id="91643-148">I profili sono indipendenti dal codificatore; un'applicazione può selezionare un codificatore, quindi selezionare un profilo e applicare le impostazioni del profilo al codificatore.</span><span class="sxs-lookup"><span data-stu-id="91643-148">Profiles are independent of the encoder; an application can select an encoder, then select a profile and apply the profile settings to the encoder.</span></span> <span data-ttu-id="91643-149">I profili sono identificati dal GUID e devono essere archiviati nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="91643-149">Profiles are identified by GUID and should be stored in the following location in the registry:</span></span>


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



<span data-ttu-id="91643-150">*GUID profilo*</span><span class="sxs-lookup"><span data-stu-id="91643-150">where *Profile GUID*</span></span>

<span data-ttu-id="91643-151">formato stringa del GUID che identifica il profilo.</span><span class="sxs-lookup"><span data-stu-id="91643-151">is the string form of the GUID that identifies the profile.</span></span> <span data-ttu-id="91643-152">Creare valori per ogni impostazione.</span><span class="sxs-lookup"><span data-stu-id="91643-152">Create values for each setting.</span></span> <span data-ttu-id="91643-153">Creare anche un valore stringa denominato "FriendlyName" i cui dati identificano il profilo, ad esempio "LowBandwidthVideo".</span><span class="sxs-lookup"><span data-stu-id="91643-153">Also create a string value named "FriendlyName" whose data identifies the profile (such as "LowBandwidthVideo").</span></span>

## <a name="related-topics"></a><span data-ttu-id="91643-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91643-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91643-155">Sviluppo di codificatori e decodificatori</span><span class="sxs-lookup"><span data-stu-id="91643-155">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 




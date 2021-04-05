---
title: Registrazione di plug-in DSP
description: Registrazione di plug-in DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Plug-in di Windows Media Player, voci del registro di sistema
- plug-in, voci del registro di sistema
- plug-in di elaborazione dei segnali digitali, voci del registro di sistema
- Plug-in DSP, voci del registro di sistema
- Registro di sistema, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956195"
---
# <a name="registering-dsp-plug-ins"></a><span data-ttu-id="77137-108">Registrazione di plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="77137-108">Registering DSP Plug-ins</span></span>

<span data-ttu-id="77137-109">Per rendere disponibile il plug-in DSP in Windows Media Player è necessario creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77137-109">To make your DSP plug-in available in Windows Media Player you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



<span data-ttu-id="77137-110">Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per i nomi e identificatori univoci globali (GUID) specifici per il plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="77137-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="77137-111">Nella tabella seguente vengono descritti i segnaposto.</span><span class="sxs-lookup"><span data-stu-id="77137-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="77137-112">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="77137-112">Placeholder</span></span>               | <span data-ttu-id="77137-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77137-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77137-114">*PluginClsid*</span><span class="sxs-lookup"><span data-stu-id="77137-114">*PluginClsid*</span></span>             | <span data-ttu-id="77137-115">GUID che rappresenta l'identificatore di classe per la classe primaria del plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="77137-115">A GUID that is the class identifier for the DSP plug-in's primary class.</span></span> <span data-ttu-id="77137-116">Si tratta della classe che implementa **IMediaObject**, **IPluginEnable** e possibilmente **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="77137-116">This is the class that implements **IMediaObject**, **IPluginEnable**, and possibly **ISpecifyPropertyPages**.</span></span> <span data-ttu-id="77137-117">In un plug-in in modalità duale, questa classe implementa anche **IMFTransform** e **IMFGetService**. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="77137-117">In a dual-mode plug-in, this class also implements **IMFTransform** and **IMFGetService**.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="77137-118">Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="77137-118">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="77137-119">*PluginClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="77137-119">*PluginClassFriendlyName*</span></span> | <span data-ttu-id="77137-120">Nome descrittivo per la classe primaria del plug-in DSP. Esempio: "classe ProsewareDSP"</span><span class="sxs-lookup"><span data-stu-id="77137-120">A friendly name for the DSP plug-in's primary class.Example: "ProsewareDSP Class"</span></span><br/>                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="77137-121">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="77137-121">*PluginModuleName*</span></span>        | <span data-ttu-id="77137-122">Percorso completo della DLL che implementa il plug-in DSP. Esempio: "C: \\ Program Files \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="77137-122">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="77137-123">*Threading*</span><span class="sxs-lookup"><span data-stu-id="77137-123">*Threading*</span></span>               | <span data-ttu-id="77137-124">Stringa che specifica il modello di threading per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="77137-124">A string that specifies the threading model for the plug-in.</span></span> <span data-ttu-id="77137-125">Se il plug-in verrà eseguito con Windows Media Player 11 in Windows Vista, questa voce del registro di sistema deve essere uguale a "both".</span><span class="sxs-lookup"><span data-stu-id="77137-125">If the plug-in is going to run with Windows Media Player 11 on Windows Vista, this registry entry must be equal to "Both".</span></span> <span data-ttu-id="77137-126">Se il plug-in viene eseguito in Windows XP o in sistemi operativi precedenti, la voce del registro di sistema può essere uguale a "Apartment" o "both".</span><span class="sxs-lookup"><span data-stu-id="77137-126">If the plug-in is going to run on Windows XP or older operating systems, this registry entry can be equal to either "Apartment" or "Both".</span></span>                                                                                           |



 

<span data-ttu-id="77137-127">Se il plug-in DSP implementa un'interfaccia personalizzata e se il plug-in viene eseguito in Windows Media Player 11 in Windows Vista, è necessario creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77137-127">If your DSP plug-in implements a custom interface and if your plug-in is going to run in Windows Media Player 11 on Windows Vista, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



<span data-ttu-id="77137-128">Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per nomi, valori numerici e identificatori univoci globali (GUID) specifici per il plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="77137-128">In the preceding registry syntax, the symbols in italic are placeholders for names, numeric values, and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="77137-129">Nella tabella seguente vengono descritti i segnaposto.</span><span class="sxs-lookup"><span data-stu-id="77137-129">The following table describes those placeholders.</span></span>



| <span data-ttu-id="77137-130">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="77137-130">Placeholder</span></span>           | <span data-ttu-id="77137-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77137-131">Description</span></span>                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77137-132">*ProxyStubClsid*</span><span class="sxs-lookup"><span data-stu-id="77137-132">*ProxyStubClsid*</span></span>      | <span data-ttu-id="77137-133">GUID che rappresenta l'identificatore di classe per la classe che implementa i proxy e gli stub per le interfacce personalizzate del plug-in DSP. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="77137-133">A GUID that is the class identifier for the class that implements the proxies and stubs for the DSP plug-in's custom interfaces.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="77137-134">Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="77137-134">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="77137-135">*ProxyStubModuleName*</span><span class="sxs-lookup"><span data-stu-id="77137-135">*ProxyStubModuleName*</span></span> | <span data-ttu-id="77137-136">Percorso completo della DLL che implementa le interfacce del proxy e dello stub per il plug-in DSP. Esempio: "C: \\ Program Files \\ Proseware \\ProsewareDspPS.dll"</span><span class="sxs-lookup"><span data-stu-id="77137-136">The fully qualified path to the DLL that implements the proxy and stub interfaces for the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDspPS.dll"</span></span><br/>                                                                                               |
| <span data-ttu-id="77137-137">*CustomInterfaceId*</span><span class="sxs-lookup"><span data-stu-id="77137-137">*CustomInterfaceId*</span></span>   | <span data-ttu-id="77137-138">GUID che rappresenta l'identificatore di interfaccia per un'interfaccia personalizzata implementata dal plug-in DSP. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="77137-138">A GUID that is the interface identifier for a custom interface that is implemented by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="77137-139">Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="77137-139">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                           |
| <span data-ttu-id="77137-140">*CustomInterfaceName*</span><span class="sxs-lookup"><span data-stu-id="77137-140">*CustomInterfaceName*</span></span> | <span data-ttu-id="77137-141">Nome di un'interfaccia personalizzata implementata dal plug-in DSP. Esempio: "IProsewareDsp"</span><span class="sxs-lookup"><span data-stu-id="77137-141">The name of a custom interface that is implemented by the DSP plug-in.Example: "IProsewareDsp"</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="77137-142">*NumberOfMethods*</span><span class="sxs-lookup"><span data-stu-id="77137-142">*NumberOfMethods*</span></span>     | <span data-ttu-id="77137-143">Numero di metodi, inclusi i metodi ereditati, definiti da un'interfaccia personalizzata. Esempio: "5"</span><span class="sxs-lookup"><span data-stu-id="77137-143">The number of methods, including inherited methods, defined by a custom interface.Example: "5"</span></span><br/>                                                                                                                                                                  |



 

<span data-ttu-id="77137-144">Se il plug-in DSP fornisce una pagina delle proprietà, è necessario creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77137-144">If your DSP plug-in provides a property page, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="77137-145">Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per i nomi e identificatori univoci globali (GUID) specifici per il plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="77137-145">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="77137-146">Nella tabella seguente vengono descritti i segnaposto.</span><span class="sxs-lookup"><span data-stu-id="77137-146">The following table describes those placeholders.</span></span>



| <span data-ttu-id="77137-147">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="77137-147">Placeholder</span></span>                 | <span data-ttu-id="77137-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77137-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77137-149">*PropPageClsid*</span><span class="sxs-lookup"><span data-stu-id="77137-149">*PropPageClsid*</span></span>             | <span data-ttu-id="77137-150">GUID che rappresenta l'identificatore di classe per la classe di pagine delle proprietà fornita dal plug-in DSP. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="77137-150">A GUID that is the class identifier for the property page class provided by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="77137-151">Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="77137-151">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="77137-152">*PropPageClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="77137-152">*PropPageClassFriendlyName*</span></span> | <span data-ttu-id="77137-153">Nome descrittivo per la classe della pagina delle proprietà. Esempio: "classe della pagina delle proprietà di ProsewareDSP"</span><span class="sxs-lookup"><span data-stu-id="77137-153">A friendly name for the property page class.Example: "ProsewareDSP Property Page Class"</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="77137-154">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="77137-154">*PluginModuleName*</span></span>          | <span data-ttu-id="77137-155">Percorso completo della DLL che implementa il plug-in DSP. Esempio: "C: \\ Program Files \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="77137-155">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                               |



 

<span data-ttu-id="77137-156">**Chiamata di IWMPPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="77137-156">**Calling IWMPPluginRegistrar**</span></span>

<span data-ttu-id="77137-157">Oltre alle sottochiavi del registro di sistema e alle voci descritte nelle tabelle e negli elenchi precedenti, è necessario creare alcune voci e chiavi del registro di sistema chiamando [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span><span class="sxs-lookup"><span data-stu-id="77137-157">In addition to the registry subkeys and entries described in the preceding lists and tables, you must create some registry keys and entries by calling [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span></span> <span data-ttu-id="77137-158">Questo metodo esegue la registrazione necessaria per consentire a Windows Media Player di riconoscere il plug-in e presentarlo come opzione all'utente.</span><span class="sxs-lookup"><span data-stu-id="77137-158">This method performs the necessary registration to enable Windows Media Player to recognize your plug-in and present it as an option to the user.</span></span>

<span data-ttu-id="77137-159">Chiamare **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** nella funzione **DllRegisterServer** del plug-in e chiamare [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) nella funzione **DllUnregisterServer** del plug-in.</span><span class="sxs-lookup"><span data-stu-id="77137-159">Call **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** in your plug-in's **DllRegisterServer** function, and call [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) in your plug-in's **DllUnregisterServer** function.</span></span> <span data-ttu-id="77137-160">Per ottenere un puntatore a un'interfaccia **IWMPMediaPluginRegistrar** , chiamare **COCREATEINSTANCE**, passando CLSID \_ WMPMediaPluginRegistrar come ID classe.</span><span class="sxs-lookup"><span data-stu-id="77137-160">To get a pointer to an **IWMPMediaPluginRegistrar** interface, call **CoCreateInstance**, passing CLSID\_WMPMediaPluginRegistrar as the Class ID.</span></span> <span data-ttu-id="77137-161">La costante CLSID \_ WMPMediaPluginRegistrar è definita in wmpservices. h.</span><span class="sxs-lookup"><span data-stu-id="77137-161">The constant CLSID\_WMPMediaPluginRegistrar is defined in wmpservices.h.</span></span>

<span data-ttu-id="77137-162">**Registrazione nella procedura guidata del plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="77137-162">**Registration in the DSP Plug-in Wizard**</span></span>

<span data-ttu-id="77137-163">La procedura guidata plug-in DSP, inclusa nella Windows SDK, genera codice di esempio basato su Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="77137-163">The DSP plug-in wizard, which is included in the Windows SDK, generates sample code that is based on Active Template Library (ATL).</span></span> <span data-ttu-id="77137-164">La funzione **DllRegisterServer** del plug-in di esempio chiama la funzione **RegisterServer** di ATL, che crea le sottochiavi e le voci del registro di sistema in base a due file di script del registro di sistema nel progetto di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="77137-164">The sample plug-in's **DllRegisterServer** function calls ATL's **RegisterServer** function, which creates registry subkeys and entries according to two registry script files in the Visual Studio project.</span></span> <span data-ttu-id="77137-165">Il file *ProjectName*. RGS contiene lo script per la registrazione della classe principale del plug-in e il file *NomeProgetto* . RGS contiene lo script per la registrazione della classe della pagina delle proprietà del plug-in.</span><span class="sxs-lookup"><span data-stu-id="77137-165">The file *ProjectName*.rgs contains the script for registering the plug-in's main class, and the file *ProjectName* PropPage.rgs contains the script for registering the plug-in's property page class.</span></span> <span data-ttu-id="77137-166">La funzione **DllRegisterServer** del plug-in di esempio chiama anche **IWMPPluginRegistrar:: WMPRegisterPlayerPlugin**.</span><span class="sxs-lookup"><span data-stu-id="77137-166">The sample plug-in's **DllRegisterServer** function also calls **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.</span></span>

<span data-ttu-id="77137-167">La procedura guidata plug-in DSP genera anche il codice per un componente stub proxy che è un file con estensione dll autoregistrato.</span><span class="sxs-lookup"><span data-stu-id="77137-167">The DSP plug-in wizard also generates code for a proxy-stub component that is a self-registering .dll file.</span></span> <span data-ttu-id="77137-168">Il codice di registrazione per il file si trova in dlldata. cpp.</span><span class="sxs-lookup"><span data-stu-id="77137-168">The registration code for that file is in dlldata.cpp.</span></span> <span data-ttu-id="77137-169">Le **\_ routine dlldata** della macro si espandono in modo da includere un'implementazione di **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="77137-169">The macro **DLLDATA\_ROUTINES** expands to include an implementation of **DllRegisterServer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77137-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77137-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77137-171">**Panoramica per gli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="77137-171">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="77137-172">**IWMPMediaPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="77137-172">**IWMPMediaPluginRegistrar**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 






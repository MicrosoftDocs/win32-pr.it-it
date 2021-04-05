---
title: Flag di registrazione
description: Flag di registrazione
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Plug-in di Windows Media Player, flag di registrazione
- plug-in, flag di registrazione
- plug-in dell'interfaccia utente, flag di registrazione
- Plug-in dell'interfaccia utente, flag di registrazione
- flag, plug-in dell'interfaccia utente
- Registro di sistema, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046319"
---
# <a name="registration-flags"></a><span data-ttu-id="332d6-109">Flag di registrazione</span><span class="sxs-lookup"><span data-stu-id="332d6-109">Registration Flags</span></span>

<span data-ttu-id="332d6-110">Quando la procedura guidata per il plug-in di Windows Media Player crea un nuovo progetto di plug-in dell'interfaccia utente, crea una chiave nel registro di sistema che contiene informazioni sul plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-110">When the Windows Media Player Plug-in Wizard creates a new UI plug-in project, it creates a key in the registry that contains information about the plug-in.</span></span> <span data-ttu-id="332d6-111">Questa chiave viene creata nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="332d6-111">This key is created in the following location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



<span data-ttu-id="332d6-112">*ClassID* è l'ID della classe del plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-112">*ClassId* is the class id of the plug-in.</span></span>

<span data-ttu-id="332d6-113">Questa chiave include i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="332d6-113">This key includes the following values.</span></span>



| <span data-ttu-id="332d6-114">Nome</span><span class="sxs-lookup"><span data-stu-id="332d6-114">Name</span></span>                     | <span data-ttu-id="332d6-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="332d6-115">Type</span></span>       | <span data-ttu-id="332d6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="332d6-116">Description</span></span>                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332d6-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="332d6-117">Capabilities</span></span>             | <span data-ttu-id="332d6-118">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="332d6-118">REG\_DWORD</span></span> | <span data-ttu-id="332d6-119">Valore DWORD costituito da almeno un flag del tipo di plug-in che può essere combinato con uno o più flag di funzionalità plug-in tramite operazioni binarie o.</span><span class="sxs-lookup"><span data-stu-id="332d6-119">A DWORD value that consists of at least one plug-in type flag that may be combined with one or more plug-in capabilities flags by using binary OR operations.</span></span>                             |
| <span data-ttu-id="332d6-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="332d6-120">Description</span></span>              | <span data-ttu-id="332d6-121">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="332d6-121">REG\_SZ</span></span>    | <span data-ttu-id="332d6-122">Stringa che contiene la descrizione del plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-122">A string that contains the description of the plug-in.</span></span> <span data-ttu-id="332d6-123">La creazione guidata plug-in crea una risorsa di stringa e fornisce l'URL della risorsa (usando il protocollo RES) per questo valore.</span><span class="sxs-lookup"><span data-stu-id="332d6-123">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span>         |
| <span data-ttu-id="332d6-124">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="332d6-124">FriendlyName</span></span>             | <span data-ttu-id="332d6-125">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="332d6-125">REG\_SZ</span></span>    | <span data-ttu-id="332d6-126">Stringa che contiene il nome leggibile dall'utente per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-126">A string that contains the user-readable name for the plug-in.</span></span> <span data-ttu-id="332d6-127">La creazione guidata plug-in crea una risorsa di stringa e fornisce l'URL della risorsa (usando il protocollo RES) per questo valore.</span><span class="sxs-lookup"><span data-stu-id="332d6-127">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span> |
| <span data-ttu-id="332d6-128">UninstallPath (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="332d6-128">UninstallPath (optional)</span></span> | <span data-ttu-id="332d6-129">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="332d6-129">REG\_SZ</span></span>    | <span data-ttu-id="332d6-130">Stringa che contiene il percorso di un file eseguibile che disinstalla il plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-130">A string that contains the path to an executable file that uninstalls the plug-in.</span></span>                                                                                                        |



 

<span data-ttu-id="332d6-131">Per ulteriori informazioni sul protocollo RES, vedere Internet Development SDK.</span><span class="sxs-lookup"><span data-stu-id="332d6-131">For more information about the res protocol, see the Internet Development SDK.</span></span>

<span data-ttu-id="332d6-132">Nella tabella seguente vengono illustrati in dettaglio i flag dei tipi di plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-132">The following table details the plug-in type flags.</span></span>



| <span data-ttu-id="332d6-133">Flag tipo di plug-in</span><span class="sxs-lookup"><span data-stu-id="332d6-133">Plug-in Type Flag</span></span>                | <span data-ttu-id="332d6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="332d6-134">Value</span></span> | <span data-ttu-id="332d6-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="332d6-135">Description</span></span>                                       |
|----------------------------------|-------|---------------------------------------------------|
| <span data-ttu-id="332d6-136">**\_sfondo tipo di plug-in \_**</span><span class="sxs-lookup"><span data-stu-id="332d6-136">**PLUGIN\_TYPE\_BACKGROUND**</span></span>     | <span data-ttu-id="332d6-137">0x1</span><span class="sxs-lookup"><span data-stu-id="332d6-137">0x1</span></span>   | <span data-ttu-id="332d6-138">Il plug-in dell'interfaccia utente non visualizza un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="332d6-138">The UI plug-in does not display a user interface.</span></span> |
| <span data-ttu-id="332d6-139">**tipo di plug-in \_ \_ SEPARATEWINDOW**</span><span class="sxs-lookup"><span data-stu-id="332d6-139">**PLUGIN\_TYPE\_SEPARATEWINDOW**</span></span> | <span data-ttu-id="332d6-140">0x2</span><span class="sxs-lookup"><span data-stu-id="332d6-140">0x2</span></span>   | <span data-ttu-id="332d6-141">Il plug-in dell'interfaccia utente è un plug-in di finestra separato.</span><span class="sxs-lookup"><span data-stu-id="332d6-141">The UI plug-in is a separate window plug-in.</span></span>      |
| <span data-ttu-id="332d6-142">**tipo di plug-in \_ \_ DISPLAYAREA**</span><span class="sxs-lookup"><span data-stu-id="332d6-142">**PLUGIN\_TYPE\_DISPLAYAREA**</span></span>    | <span data-ttu-id="332d6-143">0x3</span><span class="sxs-lookup"><span data-stu-id="332d6-143">0x3</span></span>   | <span data-ttu-id="332d6-144">Il plug-in dell'interfaccia utente è un plug-in dell'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="332d6-144">The UI plug-in is a display area plug-in.</span></span>         |
| <span data-ttu-id="332d6-145">**tipo di plug-in \_ \_ SETTINGSAREA**</span><span class="sxs-lookup"><span data-stu-id="332d6-145">**PLUGIN\_TYPE\_SETTINGSAREA**</span></span>   | <span data-ttu-id="332d6-146">0x4</span><span class="sxs-lookup"><span data-stu-id="332d6-146">0x4</span></span>   | <span data-ttu-id="332d6-147">Il plug-in dell'interfaccia utente è un plug-in area impostazioni.</span><span class="sxs-lookup"><span data-stu-id="332d6-147">The UI plug-in is a settings area plug-in.</span></span>        |
| <span data-ttu-id="332d6-148">**tipo di plug-in \_ \_ METADATAAREA**</span><span class="sxs-lookup"><span data-stu-id="332d6-148">**PLUGIN\_TYPE\_METADATAAREA**</span></span>   | <span data-ttu-id="332d6-149">0x5</span><span class="sxs-lookup"><span data-stu-id="332d6-149">0x5</span></span>   | <span data-ttu-id="332d6-150">Il plug-in dell'interfaccia utente è un plug-in dell'area dei metadati.</span><span class="sxs-lookup"><span data-stu-id="332d6-150">The UI plug-in is a metadata area plug-in.</span></span>        |



 

<span data-ttu-id="332d6-151">Nella tabella seguente vengono illustrati in dettaglio i flag delle funzionalità plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-151">The following table details the plug-in capabilities flags.</span></span>



| <span data-ttu-id="332d6-152">Flag funzionalità plug-in</span><span class="sxs-lookup"><span data-stu-id="332d6-152">Plug-in Capabilities Flag</span></span>             | <span data-ttu-id="332d6-153">Valore</span><span class="sxs-lookup"><span data-stu-id="332d6-153">Value</span></span>      | <span data-ttu-id="332d6-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="332d6-154">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332d6-155">**flag plug-in \_ \_ ACCEPTSMEDIA**</span><span class="sxs-lookup"><span data-stu-id="332d6-155">**PLUGIN\_FLAGS\_ACCEPTSMEDIA**</span></span>       | <span data-ttu-id="332d6-156">0x10000000</span><span class="sxs-lookup"><span data-stu-id="332d6-156">0x10000000</span></span> | <span data-ttu-id="332d6-157">Il plug-in dell'interfaccia utente può accettare matrici di puntatore a oggetti **multimediali** quando Windows Media Player chiama [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="332d6-157">The UI plug-in can accept **Media** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="332d6-158">**flag plug-in \_ \_ ACCEPTSPLAYLISTS**</span><span class="sxs-lookup"><span data-stu-id="332d6-158">**PLUGIN\_FLAGS\_ACCEPTSPLAYLISTS**</span></span>   | <span data-ttu-id="332d6-159">0x8000000</span><span class="sxs-lookup"><span data-stu-id="332d6-159">0x8000000</span></span>  | <span data-ttu-id="332d6-160">Il plug-in dell'interfaccia utente può accettare le matrici di puntatori a oggetti della **playlist** quando Windows Media Player chiama [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="332d6-160">The UI plug-in can accept **Playlist** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="332d6-161">**flag plug-in \_ \_ HASPRESETS**</span><span class="sxs-lookup"><span data-stu-id="332d6-161">**PLUGIN\_FLAGS\_HASPRESETS**</span></span>         | <span data-ttu-id="332d6-162">0x4000000</span><span class="sxs-lookup"><span data-stu-id="332d6-162">0x4000000</span></span>  | <span data-ttu-id="332d6-163">Il plug-in dell'interfaccia utente usa i set di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="332d6-163">The UI plug-in uses presets.</span></span> <span data-ttu-id="332d6-164">Se il plug-in specifica questo flag, Windows Media Player eseguirà una query sul plug-in per ottenere informazioni sul set di impostazioni chiamando [**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="332d6-164">If the plug-in specifies this flag, Windows Media Player will query the plug-in for preset information by calling [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="332d6-165">**flag plug-in \_ \_ HASPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="332d6-165">**PLUGIN\_FLAGS\_HASPROPERTYPAGE**</span></span>    | <span data-ttu-id="332d6-166">0x80000000</span><span class="sxs-lookup"><span data-stu-id="332d6-166">0x80000000</span></span> | <span data-ttu-id="332d6-167">Il plug-in dell'interfaccia utente fornisce una finestra di dialogo della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="332d6-167">The UI plug-in provides a property page dialog.</span></span> <span data-ttu-id="332d6-168">Windows Media Player chiamerà [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) se questo flag viene impostato quando viene richiamata la pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="332d6-168">Windows Media Player will call [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) if this flag is set when the property page is invoked.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="332d6-169">**flag plug-in \_ \_ nascosti**</span><span class="sxs-lookup"><span data-stu-id="332d6-169">**PLUGIN\_FLAGS\_HIDDEN**</span></span>             | <span data-ttu-id="332d6-170">0x02000000</span><span class="sxs-lookup"><span data-stu-id="332d6-170">0x02000000</span></span> | <span data-ttu-id="332d6-171">Il plug-in in background dell'interfaccia utente non viene visualizzato nel menu **plug-** in a cui si accede dai menu **Visualizza** o **strumenti** oppure dal pulsante **Seleziona opzioni di riproduzione ora** in gioco.</span><span class="sxs-lookup"><span data-stu-id="332d6-171">The background UI plug-in does not appear on the **Plug-ins** menu that is accessed from the **View** or **Tools** menus or the **Select Now Playing options** button in Now Playing.</span></span> <span data-ttu-id="332d6-172">Viene visualizzato nella scheda **plug-** in della finestra di dialogo Opzioni.</span><span class="sxs-lookup"><span data-stu-id="332d6-172">It does appear on the **Plug-ins** tab of the Options dialog.</span></span> <span data-ttu-id="332d6-173">Il plug-in in background che esegue l'icona viene visualizzato nella barra di stato. Questo flag non ha alcun effetto sui plug-in diversi dai plug-in di interfaccia utente in background.</span><span class="sxs-lookup"><span data-stu-id="332d6-173">It does cause the Background Plug-in Running icon to appear in the status bar.This flag has no effect on plug-ins other than background UI plug-ins.</span></span><br/> |
| <span data-ttu-id="332d6-174">**flag plug-in \_ \_ INSTALLAUTORUN**</span><span class="sxs-lookup"><span data-stu-id="332d6-174">**PLUGIN\_FLAGS\_INSTALLAUTORUN**</span></span>     | <span data-ttu-id="332d6-175">0x40000000</span><span class="sxs-lookup"><span data-stu-id="332d6-175">0x40000000</span></span> | <span data-ttu-id="332d6-176">Windows Media Player esegue automaticamente il plug-in dell'interfaccia utente quando viene installato il plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-176">Windows Media Player runs the UI plug-in automatically when the plug-in is installed.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="332d6-177">**flag plug-in \_ \_ LAUNCHPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="332d6-177">**PLUGIN\_FLAGS\_LAUNCHPROPERTYPAGE**</span></span> | <span data-ttu-id="332d6-178">0x20000000</span><span class="sxs-lookup"><span data-stu-id="332d6-178">0x20000000</span></span> | <span data-ttu-id="332d6-179">Windows Media Player chiama [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) quando il plug-in dell'interfaccia utente viene eseguito per la prima volta. Se questo flag è specificato, è necessario specificare anche i flag di plug-in **\_ \_ HASPROPERTYPAGE** .</span><span class="sxs-lookup"><span data-stu-id="332d6-179">Windows Media Player calls [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) when the UI plug-in runs for the first time.If this flag is specified, **PLUGIN\_FLAGS\_HASPROPERTYPAGE** should be specified also.</span></span><br/>                                                                                                                                                             |



 

<span data-ttu-id="332d6-180">Le costanti seguenti sono definite in wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="332d6-180">The following constants are defined in wmpplug.h.</span></span> <span data-ttu-id="332d6-181">Non modificare i valori associati a queste costanti.</span><span class="sxs-lookup"><span data-stu-id="332d6-181">Do not change the values associated with these constants.</span></span>



| <span data-ttu-id="332d6-182">Nome</span><span class="sxs-lookup"><span data-stu-id="332d6-182">Name</span></span>                                    | <span data-ttu-id="332d6-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="332d6-183">Description</span></span>                               |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="332d6-184">**PLUG-in \_ INSTALLREGKEY**</span><span class="sxs-lookup"><span data-stu-id="332d6-184">**PLUGIN\_INSTALLREGKEY**</span></span>               | <span data-ttu-id="332d6-185">Percorso della chiave del registro di sistema del plug-in.</span><span class="sxs-lookup"><span data-stu-id="332d6-185">The location of the plug-in registry key.</span></span> |
| <span data-ttu-id="332d6-186">**PLUG-in \_ INSTALLREGKEY \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="332d6-186">**PLUGIN\_INSTALLREGKEY\_FRIENDLYNAME**</span></span> | <span data-ttu-id="332d6-187">Nome del valore del nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="332d6-187">The name of the friendly name value.</span></span>      |
| <span data-ttu-id="332d6-188">**Descrizione del plug-in \_ INSTALLREGKEY \_**</span><span class="sxs-lookup"><span data-stu-id="332d6-188">**PLUGIN\_INSTALLREGKEY\_DESCRIPTION**</span></span>  | <span data-ttu-id="332d6-189">Nome del valore di descrizione.</span><span class="sxs-lookup"><span data-stu-id="332d6-189">The name of the description value.</span></span>        |
| <span data-ttu-id="332d6-190">**funzionalità del plug-in \_ INSTALLREGKEY \_**</span><span class="sxs-lookup"><span data-stu-id="332d6-190">**PLUGIN\_INSTALLREGKEY\_CAPABILITIES**</span></span> | <span data-ttu-id="332d6-191">Nome del valore delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="332d6-191">The name of the capabilities value.</span></span>       |
| <span data-ttu-id="332d6-192">**disinstallazione del plug-in \_ INSTALLREGKEY \_**</span><span class="sxs-lookup"><span data-stu-id="332d6-192">**PLUGIN\_INSTALLREGKEY\_UNINSTALL**</span></span>    | <span data-ttu-id="332d6-193">Nome del valore del percorso di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="332d6-193">The name of the uninstall path value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="332d6-194">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="332d6-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="332d6-195">**IWMPPluginUI::D isplayPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="332d6-195">**IWMPPluginUI::DisplayPropertyPage**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[<span data-ttu-id="332d6-196">**IWMPPluginUI:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="332d6-196">**IWMPPluginUI::GetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[<span data-ttu-id="332d6-197">**IWMPPluginUI:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="332d6-197">**IWMPPluginUI::SetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[<span data-ttu-id="332d6-198">**Guida di riferimento alla programmazione di plug-in dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="332d6-198">**User Interface Plug-ins Programming Reference**</span></span>](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 






---
description: Utilizzare i programmi predefiniti per impostare l'esperienza utente predefinita.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programmi predefiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2021
ms.locfileid: "103885874"
---
# <a name="default-programs"></a><span data-ttu-id="2f301-103">Programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="2f301-103">Default Programs</span></span>

<span data-ttu-id="2f301-104">Utilizzare i **programmi predefiniti** per impostare l'esperienza utente predefinita.</span><span class="sxs-lookup"><span data-stu-id="2f301-104">Use **Default Programs** to set the default user experience.</span></span> <span data-ttu-id="2f301-105">Gli utenti possono accedere ai **programmi predefiniti** dal pannello di controllo o direttamente dal menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="2f301-105">Users can access **Default Programs** from Control Panel or directly from the **Start** menu.</span></span> <span data-ttu-id="2f301-106">[Impostare l'accesso al programma e lo strumento SPAD (computer defaults)](cpl-setprogramaccess.md) , l'esperienza dei valori predefiniti primari per gli utenti di Windows XP, è ora una parte dei **programmi predefiniti**.</span><span class="sxs-lookup"><span data-stu-id="2f301-106">[Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) tool, the primary defaults experience for users in Windows XP, is now one part of **Default Programs**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f301-107">Questo argomento non è applicabile a Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2f301-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="2f301-108">Il modo in cui le associazioni di file predefinite cambiano in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2f301-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="2f301-109">Per ulteriori informazioni, vedere la sezione relativa alle **modifiche apportate al modo in cui Windows 10 gestisce le app predefinite** in [questo post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="2f301-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

<span data-ttu-id="2f301-110">Quando un utente imposta le impostazioni predefinite del programma utilizzando **programmi predefiniti**, l'impostazione predefinita si applica solo a tale utente e non ad altri utenti che potrebbero utilizzare lo stesso computer.</span><span class="sxs-lookup"><span data-stu-id="2f301-110">When a user sets program defaults using **Default Programs**, the default setting applies only to that user and not to other users who might use the same computer.</span></span> <span data-ttu-id="2f301-111">**Programmi predefiniti** fornisce un set di API (deprecate in Windows 8) che consentono ai fornitori di software indipendenti (ISV) di includere i programmi o le applicazioni nel sistema predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f301-111">**Default Programs** provides a set of APIs (deprecated in Windows 8) that enable independent software vendors (ISVs) to include their programs or applications in the defaults system.</span></span> <span data-ttu-id="2f301-112">Il set di API consente inoltre agli ISV di gestire meglio il proprio stato come impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="2f301-112">The API set also helps ISVs better manage their status as defaults.</span></span>

<span data-ttu-id="2f301-113">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="2f301-113">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2f301-114">Introduzione ai programmi predefiniti e al set di API correlati</span><span class="sxs-lookup"><span data-stu-id="2f301-114">Introduction to Default Programs and Its Related API Set</span></span>](#introduction-to-default-programs-and-its-related-api-set)
-   [<span data-ttu-id="2f301-115">Registrazione di un'applicazione per l'utilizzo con i programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="2f301-115">Registering an Application for Use with Default Programs</span></span>](#registering-an-application-for-use-with-default-programs)
    -   [<span data-ttu-id="2f301-116">ProgID</span><span class="sxs-lookup"><span data-stu-id="2f301-116">ProgIDs</span></span>](#progids)
    -   [<span data-ttu-id="2f301-117">Sottochiave di registrazione e descrizioni dei valori</span><span class="sxs-lookup"><span data-stu-id="2f301-117">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
    -   [<span data-ttu-id="2f301-118">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="2f301-118">RegisteredApplications</span></span>](#registeredapplications)
    -   [<span data-ttu-id="2f301-119">Esempio di registrazione completa</span><span class="sxs-lookup"><span data-stu-id="2f301-119">Full Registration Example</span></span>](#full-registration-example)
-   [<span data-ttu-id="2f301-120">Diventare il browser predefinito</span><span class="sxs-lookup"><span data-stu-id="2f301-120">Becoming the Default Browser</span></span>](#becoming-the-default-browser)
-   [<span data-ttu-id="2f301-121">Interfaccia utente programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="2f301-121">Default Programs UI</span></span>](#default-programs-ui)
-   [<span data-ttu-id="2f301-122">Procedure consigliate per l'utilizzo di programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="2f301-122">Best Practices for Using Default Programs</span></span>](#best-practices-for-using-default-programs)
    -   [<span data-ttu-id="2f301-123">Durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="2f301-123">During Installation</span></span>](#during-installation)
    -   [<span data-ttu-id="2f301-124">Dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="2f301-124">After Installation</span></span>](#after-installation)
-   [<span data-ttu-id="2f301-125">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="2f301-125">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="2f301-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f301-126">Related topics</span></span>](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a><span data-ttu-id="2f301-127">Introduzione ai programmi predefiniti e al set di API correlati</span><span class="sxs-lookup"><span data-stu-id="2f301-127">Introduction to Default Programs and Its Related API Set</span></span>

<span data-ttu-id="2f301-128">I **programmi predefiniti** sono progettati principalmente per le applicazioni che usano tipi di file standard, ad esempio file con estensione MP3 o jpg o protocolli standard, ad esempio http o mailto.</span><span class="sxs-lookup"><span data-stu-id="2f301-128">**Default Programs** is primarily designed for applications that use standard file types such as .mp3 or .jpg files or standard protocols, such as HTTP or mailto.</span></span> <span data-ttu-id="2f301-129">Le applicazioni che usano i propri protocolli proprietari e associazioni di file in genere non usano la funzionalità **programmi predefiniti** .</span><span class="sxs-lookup"><span data-stu-id="2f301-129">Applications that use their own proprietary protocols and file associations do not typically use the **Default Programs** functionality.</span></span>

<span data-ttu-id="2f301-130">Dopo aver registrato un'applicazione per la funzionalità **programmi predefiniti** , le opzioni e le funzionalità seguenti sono disponibili tramite il set di API:</span><span class="sxs-lookup"><span data-stu-id="2f301-130">After you register an application for **Default Programs** functionality, the following options and functionality are available by using the API set:</span></span>

-   <span data-ttu-id="2f301-131">Ripristinare tutte le impostazioni predefinite registrate per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-131">Restore all registered defaults for an application.</span></span> <span data-ttu-id="2f301-132">Deprecato per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f301-132">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="2f301-133">Ripristinare un singolo valore predefinito registrato per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-133">Restore a single registered default for an application.</span></span> <span data-ttu-id="2f301-134">Deprecato per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f301-134">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="2f301-135">Eseguire una query per il proprietario di un valore predefinito specifico in una singola chiamata anziché eseguire una ricerca nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2f301-135">Query for the owner of a specific default in a single call instead of searching the registry.</span></span> <span data-ttu-id="2f301-136">È possibile eseguire una query per il valore predefinito di un'associazione di file, un protocollo o un verbo canonico del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="2f301-136">You can query for the default of a file association, protocol, or **Start** menu canonical verb.</span></span>
-   <span data-ttu-id="2f301-137">Avvia un'interfaccia utente per un'applicazione specifica in cui un utente può impostare impostazioni predefinite singole.</span><span class="sxs-lookup"><span data-stu-id="2f301-137">Launch a UI for a specific application where a user can set individual defaults.</span></span>
-   <span data-ttu-id="2f301-138">Rimuovere tutte le associazioni per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-138">Remove all per-user associations.</span></span>

<span data-ttu-id="2f301-139">**Programmi predefiniti** fornisce anche un'interfaccia utente che consente di registrare un'applicazione per fornire informazioni aggiuntive all'utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-139">**Default Programs** also provides a UI that enables you to register an application in order to provide additional information to the user.</span></span> <span data-ttu-id="2f301-140">Ad esempio, un'applicazione con firma digitale può includere un URL per il home page del produttore.</span><span class="sxs-lookup"><span data-stu-id="2f301-140">For example, a digitally signed application can include a URL to the manufacturer's home page.</span></span>

<span data-ttu-id="2f301-141">L'utilizzo del set di API associato può consentire una corretta funzione dell'applicazione con la funzionalità controllo dell'account utente introdotta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f301-141">Use of the associated API set can help an application function correctly under the user account control (UAC) feature introduced in Windows Vista.</span></span> <span data-ttu-id="2f301-142">In controllo dell'account utente, un amministratore appare al sistema come utente standard, in modo che l'amministratore non possa in genere scrivere nel sottoalbero del **\_ \_ computer locale HKEY** .</span><span class="sxs-lookup"><span data-stu-id="2f301-142">Under UAC, an administrator appears to the system as a standard user, so that administrator cannot typically write to the **HKEY\_LOCAL\_MACHINE** subtree.</span></span> <span data-ttu-id="2f301-143">Questa restrizione è una funzionalità di sicurezza che impedisce a un processo di fungere da amministratore senza la conoscenza dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="2f301-143">This restriction is a security feature that prevents a process from acting as an administrator without the administrator's knowledge.</span></span>

<span data-ttu-id="2f301-144">L'installazione di un programma da un utente viene in genere eseguita come processo con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="2f301-144">Installation of a program by a user is typically performed as an elevated process.</span></span> <span data-ttu-id="2f301-145">Tuttavia, i tentativi eseguiti da un'applicazione per modificare i comportamenti di associazione predefiniti a livello di computer dopo l'installazione non saranno riusciti.</span><span class="sxs-lookup"><span data-stu-id="2f301-145">However, attempts by an application to modify default association behaviors at a machine level post-installation will be unsuccessful.</span></span> <span data-ttu-id="2f301-146">Al contrario, i valori predefiniti devono essere registrati a livello di utente, impedendo a più utenti di sovrascrivere le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="2f301-146">Instead, defaults must be registered on a per-user level, which prevents multiple users from overwriting each other's defaults.</span></span>

<span data-ttu-id="2f301-147">La struttura del registro di sistema gerarchica per le associazioni di file e protocolli offre la precedenza ai valori predefiniti per utente rispetto ai valori predefiniti a livello di computer.</span><span class="sxs-lookup"><span data-stu-id="2f301-147">The hierarchical registry structure for file and protocol associations gives precedence to per-user defaults over machine-level defaults.</span></span> <span data-ttu-id="2f301-148">Alcune applicazioni includono punti nel codice che elevano temporaneamente i propri diritti quando attestano le impostazioni predefinite registrate **nel \_ \_ computer locale HKEY**.</span><span class="sxs-lookup"><span data-stu-id="2f301-148">Some applications include points in their code that temporarily elevate their rights when they claim defaults registered in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="2f301-149">Queste applicazioni possono generare risultati imprevisti se un'altra applicazione è già registrata come impostazione predefinita per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-149">These applications might experience unexpected results if another application is already registered as the per-user default.</span></span> <span data-ttu-id="2f301-150">L'utilizzo di **programmi predefiniti** impedisce questa ambiguità e garantisce risultati previsti a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-150">Use of **Default Programs** prevents this ambiguity and guarantees expected results on a per-user level.</span></span>

## <a name="registering-an-application-for-use-with-default-programs"></a><span data-ttu-id="2f301-151">Registrazione di un'applicazione per l'utilizzo con i programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="2f301-151">Registering an Application for Use with Default Programs</span></span>

<span data-ttu-id="2f301-152">Questa sezione illustra le sottochiavi del registro di sistema e i valori necessari per registrare un'applicazione con i **programmi predefiniti**.</span><span class="sxs-lookup"><span data-stu-id="2f301-152">This section shows you the registry subkeys and values needed to register an application with **Default Programs**.</span></span> <span data-ttu-id="2f301-153">Include un esempio completo.</span><span class="sxs-lookup"><span data-stu-id="2f301-153">It includes a full example.</span></span>

<span data-ttu-id="2f301-154">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="2f301-154">This section contains the following topics:</span></span>

-   [<span data-ttu-id="2f301-155">ProgID</span><span class="sxs-lookup"><span data-stu-id="2f301-155">ProgIDs</span></span>](#progids)
-   [<span data-ttu-id="2f301-156">Sottochiave di registrazione e descrizioni dei valori</span><span class="sxs-lookup"><span data-stu-id="2f301-156">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
-   [<span data-ttu-id="2f301-157">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="2f301-157">RegisteredApplications</span></span>](#registeredapplications)
-   [<span data-ttu-id="2f301-158">Esempio di registrazione completa</span><span class="sxs-lookup"><span data-stu-id="2f301-158">Full Registration Example</span></span>](#full-registration-example)

<span data-ttu-id="2f301-159">Per i **programmi predefiniti** è necessario che ogni applicazione registri in modo esplicito le associazioni di file, le associazioni MIME e i protocolli per i quali l'applicazione deve essere elencata come un possibile valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f301-159">**Default Programs** requires each application to register explicitly the file associations, MIME associations, and protocols for which the application should be listed as a possible default.</span></span> <span data-ttu-id="2f301-160">È possibile registrare le associazioni usando gli elementi del registro di sistema seguenti, descritti in dettaglio più avanti in questo argomento nella [sottochiave di registrazione e descrizioni dei valori](#registration-subkey-and-value-descriptions):</span><span class="sxs-lookup"><span data-stu-id="2f301-160">You register the associations by using the following registry elements, which are explained in detail later in this topic under [Registration Subkey and Value Descriptions](#registration-subkey-and-value-descriptions):</span></span>

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

<span data-ttu-id="2f301-161">Nell'esempio seguente vengono illustrate le voci del registro di sistema per un browser contoso fittizio denominato WebBrowser:</span><span class="sxs-lookup"><span data-stu-id="2f301-161">The following example shows the registry entries for a fictional Contoso browser that is called WebBrowser:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a><span data-ttu-id="2f301-162">ProgID</span><span class="sxs-lookup"><span data-stu-id="2f301-162">ProgIDs</span></span>

<span data-ttu-id="2f301-163">Un'applicazione deve fornire un [ProgID](fa-progids.md)specifico.</span><span class="sxs-lookup"><span data-stu-id="2f301-163">An application must provide a specific [ProgID](fa-progids.md).</span></span> <span data-ttu-id="2f301-164">Assicurarsi di includere tutte le informazioni scritte in genere nella sottochiave predefinita generica per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="2f301-164">Be sure to include all the information that is typically written into the generic default subkey for the extension.</span></span> <span data-ttu-id="2f301-165">Ad esempio, fictional Litware Media Player fornisce le classi software del **\_ \_ computer locale HKEY** specifiche dell'applicazione \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** sottochiave.</span><span class="sxs-lookup"><span data-stu-id="2f301-165">For example, the fictional Litware media player provides the application-specific **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**LitwarePlayer11.AssocFile.MP3** subkey.</span></span> <span data-ttu-id="2f301-166">Questa sottochiave include tutte le informazioni contenute nella sottochiave predefinita generica **HKEY \_ Local \_ Machine** \\ **software** \\ **Classis** \\ **. mp3** più eventuali informazioni aggiuntive che si desidera registrare nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-166">That subkey includes all the information in the generic default subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\ **.mp3** plus any additional information that you want the application to register.</span></span> <span data-ttu-id="2f301-167">In questo modo si garantisce che se l'utente ripristina l'associazione. mp3 al lettore Litware, le informazioni del lettore Litware sono intatte e non sono state sovrascritte da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-167">This ensures that if the user restores the .mp3 association to the Litware player, the Litware player's information is intact and has not been overwritten by another application.</span></span> <span data-ttu-id="2f301-168">La sovrascrittura potrebbe verificarsi se la sottochiave predefinita è l'unica fonte di tali informazioni.</span><span class="sxs-lookup"><span data-stu-id="2f301-168">(Overwriting might occur if the default subkey is the only source of that information.)</span></span>

<span data-ttu-id="2f301-169">Quando si esegue il mapping di un ProgID a un'estensione o a un protocollo di un nome di file, un'applicazione può eseguire il mapping uno-a-uno o uno-a-molti.</span><span class="sxs-lookup"><span data-stu-id="2f301-169">When you map a ProgID to a file name extension or protocol, an application can map one-to-one or one-to-many.</span></span> <span data-ttu-id="2f301-170">Nell'esempio di Contoso ContosoHTML punta a un singolo ProgID che fornisce informazioni ShellExecute per le estensioni. htm,. html,. shtml,. XHT e. XHTML.</span><span class="sxs-lookup"><span data-stu-id="2f301-170">In the Contoso example, ContosoHTML points to a single ProgID that provides shellexecute information for the .htm, .html, .shtml, .xht, and .xhtml extensions.</span></span> <span data-ttu-id="2f301-171">Poiché esiste un ProgID diverso per ogni protocollo, quando si usano i protocolli si abilita ogni protocollo per avere una propria stringa di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2f301-171">Because a different ProgID exists for each protocol, when you use protocols you enable each protocol to have its own execution string.</span></span>

<span data-ttu-id="2f301-172">Quando il tipo MIME può essere visualizzato inline in un browser, il ProgID per il tipo MIME deve contenere la sottochiave **CLSID** che usa l'identificatore di classe (CLSID) dell'applicazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2f301-172">When your MIME type can be viewed inline in a browser, the ProgID for the MIME type must contain the **CLSID** subkey that uses the class identifier (CLSID) of the corresponding application.</span></span> <span data-ttu-id="2f301-173">Questo CLSID viene utilizzato in una ricerca rispetto al CLSID nel database MIME archiviato nel tipo di contenuto del database MIME delle classi software **\_ del \_ computer locale HKEY** \\  \\  \\  \\  \\ .</span><span class="sxs-lookup"><span data-stu-id="2f301-173">This CLSID is used in a lookup against the CLSID in the MIME database that is stored in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**MIME**\\**Database**\\**Content Type**.</span></span> <span data-ttu-id="2f301-174">Se il tipo MIME non è destinato a essere visualizzato inline in un browser, questo passaggio può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="2f301-174">If your MIME type is not intended to be viewed inline in a browser, this step can be omitted.</span></span>

### <a name="registration-subkey-and-value-descriptions"></a><span data-ttu-id="2f301-175">Sottochiave di registrazione e descrizioni dei valori</span><span class="sxs-lookup"><span data-stu-id="2f301-175">Registration Subkey and Value Descriptions</span></span>

<span data-ttu-id="2f301-176">Questa sezione descrive le singole sottochiavi del registro di sistema e i valori usati per la registrazione di un'applicazione con i **programmi predefiniti**, come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2f301-176">This section describes the individual registry subkeys and values used in registering an application with **Default Programs**, as illustrated previously.</span></span>

### <a name="capabilities"></a><span data-ttu-id="2f301-177">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="2f301-177">Capabilities</span></span>

<span data-ttu-id="2f301-178">La sottochiave **capabilities** contiene tutte le informazioni sui **programmi predefiniti** per un'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="2f301-178">The **Capabilities** subkey contains all the **Default Programs** information for a specific application.</span></span> <span data-ttu-id="2f301-179">Il segnaposto% ApplicationCapabilityPath% si riferisce al percorso del registro di sistema dall' **\_ \_ utente corrente di HKEY** o dal **\_ \_ computer locale HKEY** alla sottochiave delle **funzionalità** dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-179">The placeholder %ApplicationCapabilityPath% refers to the registry path from either **HKEY\_CURRENT\_USER** or **HKEY\_LOCAL\_MACHINE** to the application's **Capabilities** subkey.</span></span> <span data-ttu-id="2f301-180">Questa sottochiave contiene i valori significativi indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2f301-180">This subkey contains the significant values shown in the following table.</span></span>



| <span data-ttu-id="2f301-181">Valore</span><span class="sxs-lookup"><span data-stu-id="2f301-181">Value</span></span>                  | <span data-ttu-id="2f301-182">Type</span><span class="sxs-lookup"><span data-stu-id="2f301-182">Type</span></span>                       | <span data-ttu-id="2f301-183">Significato</span><span class="sxs-lookup"><span data-stu-id="2f301-183">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f301-184">ApplicationDescription</span><span class="sxs-lookup"><span data-stu-id="2f301-184">ApplicationDescription</span></span> | <span data-ttu-id="2f301-185">REG \_ sz o reg \_ expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2f301-185">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="2f301-186">**Obbligatorio**.</span><span class="sxs-lookup"><span data-stu-id="2f301-186">**Required**.</span></span> <span data-ttu-id="2f301-187">Per consentire a un utente di effettuare una scelta di assegnazione predefinita informata, un'applicazione deve fornire una stringa che descrive le funzionalità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-187">To enable a user to make an informed default assignment choice, an application must provide a string that describes the application's capabilities.</span></span> <span data-ttu-id="2f301-188">Sebbene l'esempio precedente di Contoso assegni la descrizione direttamente al valore ApplicationDescription, le applicazioni in genere forniscono la descrizione come risorsa incorporata in un file con estensione dll per facilitare la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-188">Although the previous Contoso example assigns the description directly to the ApplicationDescription value, applications typically provide the description as a resource that is embedded in a .dll file to facilitate localization.</span></span> <span data-ttu-id="2f301-189">Se ApplicationDescription non viene specificato, l'applicazione non viene visualizzata negli elenchi dell'interfaccia utente dei potenziali programmi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2f301-189">If ApplicationDescription is not provided, the application does not appear in UI lists of potential default programs.</span></span>                                                            |
| <span data-ttu-id="2f301-190">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="2f301-190">ApplicationName</span></span>        | <span data-ttu-id="2f301-191">REG \_ sz o reg \_ expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2f301-191">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="2f301-192">**Facoltativo.**</span><span class="sxs-lookup"><span data-stu-id="2f301-192">**Optional.**</span></span> <span data-ttu-id="2f301-193">Nome con cui il programma viene visualizzato nell'interfaccia utente dei programmi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2f301-193">The name by which the program appears in the Default Programs UI.</span></span> <span data-ttu-id="2f301-194">Se questi dati non vengono forniti dall'applicazione, il nome del programma eseguibile associato al primo ProgID registrato per l'applicazione viene utilizzato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-194">If this data is not provided by the application, the name of the executable program that is associated with the first registered ProgID for the application is used in the UI.</span></span> <span data-ttu-id="2f301-195">ApplicationName deve sempre corrispondere al nome registrato in [RegisteredApplications](#registeredapplications).</span><span class="sxs-lookup"><span data-stu-id="2f301-195">ApplicationName must always match the name that is registered under [RegisteredApplications](#registeredapplications).</span></span> <span data-ttu-id="2f301-196">È possibile utilizzare ApplicationName se si desidera che tipi di applicazione diversi, ad esempio un browser e un client di posta elettronica, facciano riferimento allo stesso file eseguibile quando vengono visualizzati come nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="2f301-196">You can use ApplicationName if you want different application types, such as a browser and an email client, to point to the same executable file while they appear as different names.</span></span><br/> |
| <span data-ttu-id="2f301-197">Nascosto</span><span class="sxs-lookup"><span data-stu-id="2f301-197">Hidden</span></span>                 | <span data-ttu-id="2f301-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="2f301-198">REG\_DWORD</span></span>                 | <span data-ttu-id="2f301-199">**Facoltativo.**</span><span class="sxs-lookup"><span data-stu-id="2f301-199">**Optional.**</span></span> <span data-ttu-id="2f301-200">Impostare questo valore su 1 per non visualizzare l'applicazione dall'elenco dei programmi nella finestra di dialogo **Imposta programmi predefiniti** .</span><span class="sxs-lookup"><span data-stu-id="2f301-200">Set this value to 1 to suppress the application from the list of programs in the **Set your default programs** dialog.</span></span> <span data-ttu-id="2f301-201">Se questo valore è 0 o non è presente, l'applicazione viene visualizzata normalmente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="2f301-201">If this value is 0 or not present, then the application appears in the list normally.</span></span>                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a><span data-ttu-id="2f301-202">FileAssociations</span><span class="sxs-lookup"><span data-stu-id="2f301-202">FileAssociations</span></span>

<span data-ttu-id="2f301-203">La sottochiave **FileAssociations** contiene associazioni di file specifiche richieste dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-203">The **FileAssociations** subkey contains specific file associations that are claimed by the application.</span></span> <span data-ttu-id="2f301-204">Queste attestazioni vengono archiviate come valori, con un valore per ogni estensione.</span><span class="sxs-lookup"><span data-stu-id="2f301-204">These claims are stored as values, with one value for each extension.</span></span> <span data-ttu-id="2f301-205">Le associazioni fanno riferimento a un ProgID specifico dell'applicazione anziché a un ProgID generico.</span><span class="sxs-lookup"><span data-stu-id="2f301-205">Associations point to an application-specific ProgID instead of a generic ProgID.</span></span> <span data-ttu-id="2f301-206">Tuttavia, non è necessario che tutte le associazioni puntino allo stesso ProgID.</span><span class="sxs-lookup"><span data-stu-id="2f301-206">However, all associations are not required to point to the same ProgID.</span></span>

### <a name="mimeassociations"></a><span data-ttu-id="2f301-207">MIMEAssociations</span><span class="sxs-lookup"><span data-stu-id="2f301-207">MIMEAssociations</span></span>

<span data-ttu-id="2f301-208">La sottochiave **MIMEAssociations** contiene tipi MIME specifici richiesti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-208">The **MIMEAssociations** subkey contains specific MIME types that are claimed by the application.</span></span> <span data-ttu-id="2f301-209">Queste attestazioni vengono archiviate come valori, con un valore per ogni tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="2f301-209">These claims are stored as values, with one value for each MIME type.</span></span> <span data-ttu-id="2f301-210">Il nome del valore per ogni tipo MIME deve corrispondere esattamente al nome MIME archiviato nel database MIME.</span><span class="sxs-lookup"><span data-stu-id="2f301-210">The value name for each MIME type must exactly match the MIME name that is stored in the MIME database.</span></span> <span data-ttu-id="2f301-211">Al valore deve essere assegnato anche un ProgID specifico dell'applicazione che contiene il CLSID corrispondente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-211">The value must also be assigned an application-specific ProgID that contains the corresponding CLSID of the application.</span></span>

### <a name="startmenu"></a><span data-ttu-id="2f301-212">StartMenu</span><span class="sxs-lookup"><span data-stu-id="2f301-212">Startmenu</span></span>

<span data-ttu-id="2f301-213">La sottochiave **StartMenu** è associata alle voci di **posta elettronica** e **Internet** assegnabili dall'utente nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="2f301-213">The **Startmenu** subkey is associated with the user-assignable **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="2f301-214">Un'applicazione deve essere registrata separatamente come un contendente per tali voci.</span><span class="sxs-lookup"><span data-stu-id="2f301-214">An application must register separately as a contender for those entries.</span></span> <span data-ttu-id="2f301-215">Per ulteriori informazioni, vedere [la pagina relativa alla registrazione di programmi con i tipi di client](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="2f301-215">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

> [!Note]  
> <span data-ttu-id="2f301-216">A partire da Windows 7, nel menu **Start** non sono più presenti **Internet** e voci di **posta elettronica** .</span><span class="sxs-lookup"><span data-stu-id="2f301-216">As of Windows 7, there are no longer **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="2f301-217">I dati del registro di sistema associati alla voce di **posta elettronica** vengono comunque utilizzati per il client MAPI predefinito, ma i dati del registro di sistema associati alla voce **Internet** non vengono utilizzati da Windows.</span><span class="sxs-lookup"><span data-stu-id="2f301-217">The registry data associated with the **E-mail** entry is still used for the default MAPI client, but the registry data associated with the **Internet** entry is not used by Windows at all.</span></span>

 

<span data-ttu-id="2f301-218">Associando la registrazione del menu **Start** di un'applicazione alla registrazione dei **Programmi predefinita** , l'applicazione viene visualizzata come un potenziale valore predefinito nell'interfaccia utente di **set Associations** .</span><span class="sxs-lookup"><span data-stu-id="2f301-218">By associating the **Start** menu registration of an application with its **Default Programs** registration, the application appears as a potential default in the **Set associations** UI.</span></span> <span data-ttu-id="2f301-219">Se l'utente ha scelto l'applicazione come predefinita e quindi sceglie di ripristinare tutte le impostazioni predefinite dell'applicazione in un secondo momento, l'applicazione viene ripristinata nella posizione del menu **Start** per tale utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-219">If the user has chosen the application as the default and then chooses to restore all application defaults later, the application is restored to its **Start** menu position for that user.</span></span> <span data-ttu-id="2f301-220">Per ulteriori informazioni e per un'illustrazione, vedere la sezione relativa all' [interfaccia utente dei programmi predefiniti](#default-programs-ui) più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="2f301-220">For more information and an illustration, see the [Default Programs UI](#default-programs-ui) section later in this topic.</span></span>

<span data-ttu-id="2f301-221">La sottochiave **StartMenu** include due voci: StartMenuInternet e mail, che corrispondono alle posizioni canoniche **Internet** e di **posta elettronica** nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="2f301-221">The **Startmenu** subkey has two entries: StartMenuInternet and Mail, which correspond to the canonical **Internet** and **E-mail** positions in the **Start** menu.</span></span> <span data-ttu-id="2f301-222">Un'applicazione assegna a StartMenuInternet o mail un valore uguale al nome della sottochiave registrata dell'applicazione in **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** o **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **mail** (come descritto in [registrazione di programmi con tipi di client](reg-middleware-apps.md)).</span><span class="sxs-lookup"><span data-stu-id="2f301-222">An application assigns either StartMenuInternet or Mail a value equal to the name of the application's registered subkey under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** or **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** (as described in [Registering Programs with Client Types](reg-middleware-apps.md)).</span></span>

<span data-ttu-id="2f301-223">Nel caso della posizione canonica del **messaggio di posta elettronica** nel menu **Start** , rappresenta il client MAPI predefinito e pertanto si presuppone che sia in grado di passare le chiamate MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f301-223">In the case of the **E-mail** canonical position in the **Start** menu, it represents the default MAPI client and is therefore assumed capable of handing MAPI calls.</span></span> <span data-ttu-id="2f301-224">In Windows 7, anche se non è più disponibile una posizione canonica di **posta elettronica** nel menu **Start** , questa sottochiave continua a essere utilizzata per il client MAPI predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f301-224">Under Windows 7, while there is no longer an **E-mail** canonical position in the **Start** menu, this subkey continues to be used for the default MAPI client.</span></span> <span data-ttu-id="2f301-225">Un'applicazione che rivendica l'impostazione predefinita della posta dovrebbe registrarsi come gestore MAPI nella sottochiave seguente:</span><span class="sxs-lookup"><span data-stu-id="2f301-225">An application claiming the mail default should register as a MAPI handler under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

<span data-ttu-id="2f301-226">Se un client di posta elettronica non è in grado di supportare MAPI ma vuole comunque contendersi la **posizione canonica** del menu **Start** , può registrare una riga di comando nella sottochiave seguente:</span><span class="sxs-lookup"><span data-stu-id="2f301-226">If a mail client cannot support MAPI but still wants to contend for the **Start** menu **E-mail** canonical position, it can register a command line under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

<span data-ttu-id="2f301-227">Inoltre, in **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **mail** \\ *CanonicalName* aggiungere un valore predefinito con il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-227">Also, under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**\\*CanonicalName* add a default value with the application name.</span></span>

<span data-ttu-id="2f301-228">Queste voci consentono l'avvio dell'applicazione dalla posizione di **posta elettronica** del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="2f301-228">These entries allow the application to be launched from the **Start** menu's **E-mail** position.</span></span> <span data-ttu-id="2f301-229">Si noti che le chiamate MAPI vengono ancora apportate all'applicazione e che passano al gestore MAPI precedente oppure hanno esito negativo se non è stato impostato alcun gestore MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f301-229">Note that MAPI calls are still made to the application, and either fall through to the prior MAPI handler, or fail if no MAPI handler has been set.</span></span> <span data-ttu-id="2f301-230">Per ulteriori informazioni, vedere [la pagina relativa alla registrazione di programmi con i tipi di client](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="2f301-230">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

### <a name="urlassociations"></a><span data-ttu-id="2f301-231">UrlAssociations</span><span class="sxs-lookup"><span data-stu-id="2f301-231">UrlAssociations</span></span>

<span data-ttu-id="2f301-232">La sottochiave **UrlAssociations** contiene i protocolli URL specifici richiesti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-232">The **UrlAssociations** subkey contains the specific URL protocols that are claimed by the application.</span></span> <span data-ttu-id="2f301-233">Queste attestazioni vengono archiviate come valori, con un valore per ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="2f301-233">These claims are stored as values, with one value for each protocol.</span></span> <span data-ttu-id="2f301-234">Ogni protocollo deve puntare a un ProgID specifico dell'applicazione anziché a un ProgID generico.</span><span class="sxs-lookup"><span data-stu-id="2f301-234">Each protocol must point to an application-specific ProgID instead of to a generic ProgID.</span></span> <span data-ttu-id="2f301-235">Come indicato nell'esempio di Contoso, è possibile usare un ProgID diverso per ogni protocollo affinché ognuno disponga di una propria stringa di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2f301-235">As mentioned in the Contoso example, you can use a different ProgID for each protocol in order for each to have its own execution string.</span></span>

### <a name="registeredapplications"></a><span data-ttu-id="2f301-236">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="2f301-236">RegisteredApplications</span></span>

<span data-ttu-id="2f301-237">La sottochiave completa per **RegisteredApplications** è la seguente:</span><span class="sxs-lookup"><span data-stu-id="2f301-237">The full subkey for **RegisteredApplications** is:</span></span>

<span data-ttu-id="2f301-238">**HKEY \_ RegisteredApplications software del \_ computer locale** \\  \\ </span><span class="sxs-lookup"><span data-stu-id="2f301-238">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**RegisteredApplications**</span></span>

<span data-ttu-id="2f301-239">Questa sottochiave fornisce al sistema operativo il percorso del registro di sistema delle informazioni sui **programmi predefiniti** per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-239">This subkey provides the operating system with the registry location of the **Default Programs** information for the application.</span></span> <span data-ttu-id="2f301-240">Il percorso viene archiviato come valore il cui nome deve corrispondere al nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-240">The location is stored as a value whose name must match the name of the application.</span></span>

### <a name="full-registration-example"></a><span data-ttu-id="2f301-241">Esempio di registrazione completa</span><span class="sxs-lookup"><span data-stu-id="2f301-241">Full Registration Example</span></span>

<span data-ttu-id="2f301-242">Questo esempio mostra le sottochiavi e i valori usati per la registrazione del lettore multimediale Litware fittizio.</span><span class="sxs-lookup"><span data-stu-id="2f301-242">This example shows the subkeys and values that are used in registering the fictional Litware media player.</span></span> <span data-ttu-id="2f301-243">Nell'esempio sono incluse le voci ProgID per illustrare il modo in cui si integra.</span><span class="sxs-lookup"><span data-stu-id="2f301-243">The example includes the ProgID entries in order to show how it all fits together.</span></span>

<span data-ttu-id="2f301-244">La sottochiave seguente mostra il ProgID specifico dell'applicazione per il tipo MIME. mp3:</span><span class="sxs-lookup"><span data-stu-id="2f301-244">The following subkey shows the application-specific ProgID for the .mp3 MIME type:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

<span data-ttu-id="2f301-245">Di seguito è presente il ProgID specifico dell'applicazione che associa il programma Litware all'estensione di file. mp3.</span><span class="sxs-lookup"><span data-stu-id="2f301-245">Next is the application-specific ProgID that associates the Litware program with the .mp3 file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="2f301-246">Nelle voci successive viene mostrato il ProgID combinato sia per il tipo MIME. MPEG che per l'estensione del nome di file.</span><span class="sxs-lookup"><span data-stu-id="2f301-246">The next entries show the combined ProgID for both the .mpeg MIME type and file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="2f301-247">Le voci successive registrano il programma Litware nei **programmi predefiniti** e usano i ProgID precedentemente registrati</span><span class="sxs-lookup"><span data-stu-id="2f301-247">The next entries register the Litware program in **Default Programs** and use the previously registered ProgIDs</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

<span data-ttu-id="2f301-248">Infine, in questo esempio viene registrato il percorso della registrazione dei **programmi predefiniti** di Litware.</span><span class="sxs-lookup"><span data-stu-id="2f301-248">Lastly, this example registers the location of the Litware **Default Programs** registration.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a><span data-ttu-id="2f301-249">Diventare il browser predefinito</span><span class="sxs-lookup"><span data-stu-id="2f301-249">Becoming the Default Browser</span></span>

<span data-ttu-id="2f301-250">La registrazione del browser deve seguire le procedure consigliate descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="2f301-250">Browser registration must follow the best practices outlined in this topic.</span></span> <span data-ttu-id="2f301-251">Quando il browser è installato, Windows può presentare all'utente una notifica di sistema tramite la quale l'utente può selezionare il browser come impostazione predefinita del sistema.</span><span class="sxs-lookup"><span data-stu-id="2f301-251">When the browser is installed, Windows can present the user with a system notification through which the user can select the browser as the system default.</span></span> <span data-ttu-id="2f301-252">Questa notifica viene visualizzata quando vengono soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f301-252">This notification is shown when these conditions are met:</span></span>

-   <span data-ttu-id="2f301-253">Il programma di installazione del browser chiama [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con il flag **SHCNE \_ ASSOCCHANGED** per indicare a Windows che sono stati registrati nuovi gestori del protocollo.</span><span class="sxs-lookup"><span data-stu-id="2f301-253">The browser's installer calls [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the **SHCNE\_ASSOCCHANGED** flag to tell Windows that new protocol handlers have been registered.</span></span>
-   <span data-ttu-id="2f301-254">Windows rileva che una o più nuove applicazioni sono state registrate per gestire i protocolli http://e https://e che l'utente non ha ancora ricevuto una notifica.</span><span class="sxs-lookup"><span data-stu-id="2f301-254">Windows detects that one or more new applications have registered to handle both http:// and https:// protocols, and the user has not yet been notified.</span></span> <span data-ttu-id="2f301-255">In altre parole, nessuno dei seguenti elementi è stato visualizzato all'utente: una notifica di sistema che annuncia l'applicazione, un riquadro a comparsa OpenWith che contiene l'applicazione o la pagina del pannello di controllo imposta impostazioni predefinite utente (SUD) per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-255">In other words, none of the following have been shown to the user: a system notification advertising the application, an OpenWith flyout that contains the application, or the Set User Defaults (SUD) Control Panel page for the application.</span></span>

<span data-ttu-id="2f301-256">Nell'esempio seguente viene illustrato il codice di registrazione consigliato che deve essere eseguito dal programma di installazione del browser dopo la scrittura delle chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2f301-256">The following example shows the recommended registration code that the browser's installer should run after it writes its registry keys.</span></span>

<span data-ttu-id="2f301-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) notifica innanzitutto al sistema che sono disponibili nuove opzioni di associazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) first notifies the system that new association choices are available.</span></span> <span data-ttu-id="2f301-258">La chiamata **SHChangeNotify** è necessaria per garantire il corretto funzionamento delle impostazioni predefinite del sistema.</span><span class="sxs-lookup"><span data-stu-id="2f301-258">The **SHChangeNotify** call is required to ensure the proper functioning of system defaults.</span></span>

<span data-ttu-id="2f301-259">Un'istruzione [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) consente quindi al tempo necessario ai processi di sistema di gestire la notifica.</span><span class="sxs-lookup"><span data-stu-id="2f301-259">A [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) statement then allows time for system processes to handle the notification.</span></span>


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



<span data-ttu-id="2f301-260">Se l'utente ignora o ignora la notifica risultante o il riquadro a comparsa senza effettuare una nuova selezione predefinita del browser, il browser predefinito rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="2f301-260">If the user dismisses or ignores the resulting notification or flyout without making a new default browser selection, the default browser remains unchanged.</span></span> <span data-ttu-id="2f301-261">Si noti che l'utente può anche modificare il browser predefinito in qualsiasi momento tramite altri meccanismi, inclusa l'impostazione delle impostazioni predefinite dell'utente nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="2f301-261">Note that the user can also change the default browser at any time through other mechanisms, including Set User Defaults in the Control Panel.</span></span>

## <a name="default-programs-ui"></a><span data-ttu-id="2f301-262">Interfaccia utente programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="2f301-262">Default Programs UI</span></span>

<span data-ttu-id="2f301-263">Nelle illustrazioni di questa sezione viene illustrata l'interfaccia utente per i **programmi predefiniti** come visualizzato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-263">The illustrations in this section show the UI for **Default Programs** as seen by the user.</span></span>

<span data-ttu-id="2f301-264">La figura seguente mostra la finestra principali **programmi predefiniti** nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="2f301-264">The following illustration shows the main **Default Programs** window in Control Panel.</span></span>

![screenshot della pagina di immissione dei programmi predefinita](images/defaultprogramsmain.png)

<span data-ttu-id="2f301-266">Quando un utente sceglie l'opzione **Imposta programmi predefiniti** , viene visualizzata la finestra seguente.</span><span class="sxs-lookup"><span data-stu-id="2f301-266">When a user chooses the **Set your default programs** option, the following window appears.</span></span> <span data-ttu-id="2f301-267">Gli utenti possono utilizzare questa pagina per assegnare un programma predefinito per tutti i tipi di file e protocolli per i quali il programma è un possibile valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f301-267">Users can use this page to assign a default program for all file types and protocols for which the program is a possible default.</span></span> <span data-ttu-id="2f301-268">Come illustrato nella figura seguente, tutti i programmi [registrati](#registering-an-application-for-use-with-default-programs) e l'icona del programma vengono visualizzati nella casella **programmi** a sinistra.</span><span class="sxs-lookup"><span data-stu-id="2f301-268">As shown in the following illustration, all [registered](#registering-an-application-for-use-with-default-programs) programs and the program icon appear in the **Programs** box on the left.</span></span>

![screenshot della pagina impostare i programmi predefiniti](images/setyourdefaultprograms.png)

<span data-ttu-id="2f301-270">Quando l'utente seleziona un programma dall'elenco, vengono visualizzati l'icona e il provider del programma.</span><span class="sxs-lookup"><span data-stu-id="2f301-270">When the user selects a program from the list, the program icon and provider are displayed.</span></span> <span data-ttu-id="2f301-271">Se l'URL è incorporato nel certificato con firma digitale del programma, il programma può anche visualizzare un URL.</span><span class="sxs-lookup"><span data-stu-id="2f301-271">If the URL is embedded in the program's digitally signed certificate, the program can also display a URL.</span></span> <span data-ttu-id="2f301-272">I programmi senza firma digitale non possono visualizzare un URL.</span><span class="sxs-lookup"><span data-stu-id="2f301-272">Programs that are not digitally signed cannot display a URL.</span></span>

<span data-ttu-id="2f301-273">Viene visualizzato anche un testo descrittivo, fornito dal programma durante la registrazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-273">Descriptive text, which is supplied by the program during registration, is also displayed.</span></span> <span data-ttu-id="2f301-274">Questo testo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2f301-274">This text is required.</span></span> <span data-ttu-id="2f301-275">Sotto la casella Descrizione è indicato il numero di valori predefiniti attualmente assegnati al programma dal numero intero che è stato registrato per la gestione.</span><span class="sxs-lookup"><span data-stu-id="2f301-275">Beneath the description box is an indication of how many defaults the program is currently assigned out of the full number it is registered to handle.</span></span>

<span data-ttu-id="2f301-276">Per assegnare o ripristinare un programma come valore predefinito per tutti i file e i protocolli per i quali è stato registrato, l'utente fa clic sull'opzione **imposta questo programma come predefinito** .</span><span class="sxs-lookup"><span data-stu-id="2f301-276">To assign or restore a program as the default for all files and protocols for which it is registered, the user clicks the **Set this program as default** option.</span></span>

<span data-ttu-id="2f301-277">Per assegnare singoli tipi di file e protocolli a un programma, l'utente fa clic sull'opzione **scegliere le impostazioni predefinite per il programma** , che consente di visualizzare le **associazioni set per una** finestra del programma come quella illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2f301-277">To assign individual file types and protocols to a program, the user clicks the **Choose defaults for this program** option, which displays a **Set associations for a program** window like the one in the following illustration.</span></span>

> [!Note]  
> <span data-ttu-id="2f301-278">Si consiglia di chiamare le **associazioni set per un programma** usando [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span><span class="sxs-lookup"><span data-stu-id="2f301-278">We recommend you call the **Set associations for a program** by using [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span></span>

 

![screenshot della pagina set associazioni per un programma](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a><span data-ttu-id="2f301-280">Procedure consigliate per l'utilizzo di programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="2f301-280">Best Practices for Using Default Programs</span></span>

<span data-ttu-id="2f301-281">In questa sezione vengono fornite indicazioni sulle procedure consigliate per l'utilizzo di **programmi predefiniti** quando si registrano le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2f301-281">This section provides best practice guidelines for using **Default Programs** when you register applications.</span></span> <span data-ttu-id="2f301-282">Offre anche suggerimenti di progettazione per la creazione di un'applicazione che fornisce agli utenti funzionalità di **programmi predefiniti** ottimali.</span><span class="sxs-lookup"><span data-stu-id="2f301-282">It also offers design suggestions for creating an application that provides users with optimal **Default Programs** functionality.</span></span>

### <a name="during-installation"></a><span data-ttu-id="2f301-283">Durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="2f301-283">During Installation</span></span>

<span data-ttu-id="2f301-284">Oltre alle procedure di installazione normalmente in Windows XP, un'applicazione basata su Windows Vista o versioni successive deve eseguire la registrazione con la funzionalità **programmi predefiniti** per sfruttare i vantaggi della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="2f301-284">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista or later based application must register with the **Default Programs** feature to take advantage of its functionality.</span></span>

<span data-ttu-id="2f301-285">Eseguire la sequenza di passaggi seguente durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-285">Perform the following sequence of steps during installation.</span></span> <span data-ttu-id="2f301-286">I passaggi 1-3 corrispondono ai passaggi utilizzati in Windows XP. il passaggio 4 era una novità di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f301-286">Steps 1-3 match the steps that were used in Windows XP; step 4 was new in Windows Vista.</span></span>

1.  <span data-ttu-id="2f301-287">Installare i file binari necessari.</span><span class="sxs-lookup"><span data-stu-id="2f301-287">Install the necessary binary files.</span></span>
2.  <span data-ttu-id="2f301-288">Scrivere i ProgID nel \_ computer locale HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="2f301-288">Write ProgIDs to HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="2f301-289">Si noti che le applicazioni devono creare ProgID specifici dell'applicazione per le rispettive associazioni.</span><span class="sxs-lookup"><span data-stu-id="2f301-289">Note that applications must create application-specific ProgIDs for their associations.</span></span>
3.  <span data-ttu-id="2f301-290">Registrare l'applicazione con i **programmi predefiniti** come descritto in precedenza in [registrazione di un'applicazione per l'uso con i programmi predefiniti](#registering-an-application-for-use-with-default-programs).</span><span class="sxs-lookup"><span data-stu-id="2f301-290">Register the application with **Default Programs** as previously explained in [Registering an Application for Use with Default Programs](#registering-an-application-for-use-with-default-programs).</span></span>

### <a name="after-installation"></a><span data-ttu-id="2f301-291">Dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="2f301-291">After Installation</span></span>

<span data-ttu-id="2f301-292">In questa sezione viene illustrato il modo in cui il prompt dell'applicazione deve presentare le opzioni predefinite a ogni utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-292">This section discusses how the application prompt should first present its default options to each user.</span></span> <span data-ttu-id="2f301-293">Viene inoltre illustrato il modo in cui un'applicazione può monitorarne lo stato come predefinito per le associazioni e i protocolli possibili.</span><span class="sxs-lookup"><span data-stu-id="2f301-293">It also discusses how an application can monitor its status as the default for its possible associations and protocols.</span></span>

### <a name="first-run-experiences"></a><span data-ttu-id="2f301-294">Esperienze di prima esecuzione</span><span class="sxs-lookup"><span data-stu-id="2f301-294">First Run Experiences</span></span>

<span data-ttu-id="2f301-295">Quando l'applicazione viene eseguita da un utente per la prima volta, è consigliabile che l'applicazione visualizzi l'interfaccia utente che in genere include le due opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f301-295">When the application is run by a user for the first time, it is recommended that the application display UI to the user that typically includes these two choices:</span></span>

-   <span data-ttu-id="2f301-296">Accettare le impostazioni predefinite dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-296">Accept the default application settings.</span></span> <span data-ttu-id="2f301-297">Questa opzione è selezionata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2f301-297">This option is selected by default.</span></span>
-   <span data-ttu-id="2f301-298">Personalizzare le impostazioni predefinite dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f301-298">Customize the default application settings.</span></span>

<span data-ttu-id="2f301-299">Prima di Windows 8, se l'utente accetta le impostazioni predefinite, l'applicazione chiama [**IApplicationAssociationRegistration:: SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), che converte tutte le associazioni a livello di computer dichiarate durante l'installazione in impostazioni per utente per tale utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-299">Prior to Windows 8, if the user accepts the default settings, your application calls [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), which converts all machine-level associations that are declared during installation to per-user settings for that user.</span></span>

<span data-ttu-id="2f301-300">Se l'utente decide di personalizzare le impostazioni, l'applicazione chiama [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) per visualizzare l'interfaccia utente dell'associazione di file.</span><span class="sxs-lookup"><span data-stu-id="2f301-300">If the user decides to customize the settings, your application calls [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) to display the file association UI.</span></span> <span data-ttu-id="2f301-301">Nella figura seguente è illustrata questa finestra per il Media Player di Litware fittizio.</span><span class="sxs-lookup"><span data-stu-id="2f301-301">The following illustration shows this window for the fictional Litware media player.</span></span>

![screenshot della pagina delle associazioni set per un programma per Litware](images/setassociationsforaprogramforlitware.png)

<span data-ttu-id="2f301-303">La finestra Associazione file Mostra le impostazioni predefinite registrate dall'applicazione e Mostra anche l'impostazione predefinita corrente per altre estensioni e protocolli.</span><span class="sxs-lookup"><span data-stu-id="2f301-303">The file association window shows the defaults that the application registered and also shows the current default for other extensions and protocols.</span></span> <span data-ttu-id="2f301-304">Al termine della personalizzazione dei valori predefiniti, l'utente fa clic sul pulsante **Salva** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="2f301-304">After the user finishes customizing their defaults, they click the **Save** button to commit the changes.</span></span> <span data-ttu-id="2f301-305">Se l'utente fa clic su **Annulla**, la finestra viene chiusa senza salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="2f301-305">If the user clicks **Cancel**, the window closes without saving changes.</span></span>

<span data-ttu-id="2f301-306">È consigliabile usare questa interfaccia utente per le applicazioni anziché per crearne una personalizzata.</span><span class="sxs-lookup"><span data-stu-id="2f301-306">You should use this UI for your applications instead of creating your own.</span></span> <span data-ttu-id="2f301-307">In questo modo, si salvano le risorse necessarie in precedenza per sviluppare l'interfaccia utente di associazione file.</span><span class="sxs-lookup"><span data-stu-id="2f301-307">By doing so, you save the resources that were previously required to develop file association UI.</span></span> <span data-ttu-id="2f301-308">Si garantisce inoltre che le associazioni vengano salvate correttamente.</span><span class="sxs-lookup"><span data-stu-id="2f301-308">You also guarantee that associations are saved correctly.</span></span>

### <a name="set-an-application-to-check-whether-it-is-the-default"></a><span data-ttu-id="2f301-309">Impostare un'applicazione per verificare se è l'impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="2f301-309">Set an Application to Check Whether It Is the Default</span></span>

> [!Note]  
> <span data-ttu-id="2f301-310">Questa operazione non è più supportata a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f301-310">This is no longer supported as of Windows 8.</span></span>

 

<span data-ttu-id="2f301-311">Le applicazioni in genere controllano se sono impostate come predefinite quando vengono eseguite.</span><span class="sxs-lookup"><span data-stu-id="2f301-311">Applications typically check whether they are set as the default when they are run.</span></span> <span data-ttu-id="2f301-312">Per eseguire questa verifica, impostare le applicazioni chiamando [**IApplicationAssociationRegistration:: QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) o [**IApplicationAssociationRegistration:: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span><span class="sxs-lookup"><span data-stu-id="2f301-312">Set your applications to make this check by calling [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) or [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span></span>

<span data-ttu-id="2f301-313">Se l'applicazione determina che non è l'impostazione predefinita, può presentare un'interfaccia utente che chiede all'utente se accettare la situazione corrente o se impostarla come predefinita.</span><span class="sxs-lookup"><span data-stu-id="2f301-313">If the application determines that it is not the default, it can present UI that asks the user whether to accept the current situation or to make the application the default.</span></span> <span data-ttu-id="2f301-314">Includere sempre una casella di controllo in questa interfaccia utente selezionata per impostazione predefinita e che presenta l'opzione che non viene più richiesta.</span><span class="sxs-lookup"><span data-stu-id="2f301-314">Always include a check box in this UI that is selected by default and that presents the option not to be asked again.</span></span>

> [!Note]  
> <span data-ttu-id="2f301-315">La scelta del valore predefinito deve essere basata sull'utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-315">The choice of default should be user driven.</span></span> <span data-ttu-id="2f301-316">Un'applicazione non deve mai recuperare un valore predefinito senza richiedere l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2f301-316">An application should never reclaim a default without asking the user.</span></span>

 

<span data-ttu-id="2f301-317">Nella figura seguente è illustrata una finestra di dialogo di esempio.</span><span class="sxs-lookup"><span data-stu-id="2f301-317">The following illustration shows an example dialog box.</span></span>

![Screenshot di una finestra di dialogo di esempio](images/notthedefaultui.png)

## <a name="additional-resources"></a><span data-ttu-id="2f301-319">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="2f301-319">Additional Resources</span></span>

-   [<span data-ttu-id="2f301-320">**IApplicationAssociationRegistration**</span><span class="sxs-lookup"><span data-stu-id="2f301-320">**IApplicationAssociationRegistration**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [<span data-ttu-id="2f301-321">**IApplicationAssociationRegistrationUI**</span><span class="sxs-lookup"><span data-stu-id="2f301-321">**IApplicationAssociationRegistrationUI**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a><span data-ttu-id="2f301-322">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f301-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f301-323">Procedure consigliate per le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="2f301-323">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="2f301-324">Scenario di esempio di associazione di file</span><span class="sxs-lookup"><span data-stu-id="2f301-324">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="2f301-325">Linee guida per la gestione di applicazioni predefinite in Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="2f301-325">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="2f301-326">Impostazione dell'accesso al programma e delle impostazioni predefinite del computer (SPAD)</span><span class="sxs-lookup"><span data-stu-id="2f301-326">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 

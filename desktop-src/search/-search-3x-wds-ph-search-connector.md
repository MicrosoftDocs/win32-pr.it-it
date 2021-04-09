---
description: Esplora risorse controlla la creazione di un connettore di ricerca per un gestore di protocollo tramite le voci della chiave del registro di sistema. Tramite il registro di sistema, gli implementatori e le terze parti possono consentire ai gestori di protocolli nuovi e legacy di partecipare alla ricerca di Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Creazione di un connettore di ricerca per un gestore di protocollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128598"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a><span data-ttu-id="099b8-104">Creazione di un connettore di ricerca per un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-104">Creating a Search Connector for a Protocol Handler</span></span>

<span data-ttu-id="099b8-105">Esplora risorse controlla la creazione di un connettore di ricerca per un gestore di protocollo tramite le voci della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="099b8-105">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries.</span></span> <span data-ttu-id="099b8-106">Tramite il registro di sistema, gli implementatori e le terze parti possono consentire ai gestori di protocolli nuovi e legacy di partecipare alla ricerca di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="099b8-106">Through the registry both implementers and third parties can enable new and legacy protocol handlers to participate in Windows 7 Search.</span></span>

<span data-ttu-id="099b8-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="099b8-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="099b8-108">Informazioni sui connettori di ricerca per i gestori di protocollo in Windows 7</span><span class="sxs-lookup"><span data-stu-id="099b8-108">About Search Connectors for Protocol Handlers in Windows 7</span></span>](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [<span data-ttu-id="099b8-109">Abilitazione di gestori di protocollo per partecipare alla ricerca</span><span class="sxs-lookup"><span data-stu-id="099b8-109">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
    -   [<span data-ttu-id="099b8-110">Disabilitazione della creazione del connettore di ricerca del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-110">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
    -   [<span data-ttu-id="099b8-111">Personalizzazione del nome, della descrizione o del FolderType per un connettore di ricerca del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-111">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [<span data-ttu-id="099b8-112">Uso del reindirizzamento delle stringhe del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="099b8-112">Using Registry String Redirection</span></span>](#using-registry-string-redirection)
    -   [<span data-ttu-id="099b8-113">Ripristino di un connettore di ricerca del gestore di protocollo eliminato</span><span class="sxs-lookup"><span data-stu-id="099b8-113">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)
-   [<span data-ttu-id="099b8-114">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="099b8-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="099b8-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="099b8-115">Related topics</span></span>](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a><span data-ttu-id="099b8-116">Informazioni sui connettori di ricerca per i gestori di protocollo in Windows 7</span><span class="sxs-lookup"><span data-stu-id="099b8-116">About Search Connectors for Protocol Handlers in Windows 7</span></span>

<span data-ttu-id="099b8-117">In Windows 7, le ricerche dal menu **Start** o da Esplora risorse includono solo i file nelle posizioni indicizzate e gli elementi non file System come gli archivi dati remoti o gli elementi del gestore di protocollo con un connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="099b8-117">In Windows 7, searches from the **Start** menu or Windows Explorer include only files in indexed locations, and non-file system items such as remote data stores or protocol handler items that have a search connector.</span></span> <span data-ttu-id="099b8-118">Oltre a includere gli elementi del gestore di protocollo nell'ambito del menu **Start** e delle ricerche della shell, il connettore di ricerca Abilita il menu **Start** per raggruppare gli elementi del gestore di protocollo nei risultati del menu **Start** , con il vantaggio risultante che l'utente può fare clic sull'intestazione di gruppo e visualizzare i risultati solo dal gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="099b8-118">In addition to including the protocol handler items in the scope of **Start** menu and Shell searches, the search connector enables the **Start** menu to group protocol handler items together in **Start** menu results, with the resulting benefit that the user can click the group header and view results from only the protocol handler.</span></span> <span data-ttu-id="099b8-119">In alternativa, l'utente può passare alla cartella **ricerche** , aprire il file del connettore di ricerca ed eseguire una ricerca che includa solo gli elementi del gestore di protocollo specifico associato al connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="099b8-119">Alternatively, the user can navigate to the **Searches** folder, open the search connector file, and perform a search that includes only items from the specific protocol handler associated with that search connector.</span></span>

<span data-ttu-id="099b8-120">Quando un utente avvia per la prima volta un'applicazione che registra un gestore di protocollo, Esplora risorse genera un file del connettore di ricerca (con estensione searchConnector-MS) per il gestore di protocollo nella cartella **ricerche** dell'utente.</span><span class="sxs-lookup"><span data-stu-id="099b8-120">When a user first starts an application that registers a protocol handler, Windows Explorer generates a search connector file (.searchConnector-ms) for the protocol handler in the user's **Searches** folder.</span></span> <span data-ttu-id="099b8-121">Le applicazioni con gestori di protocollo possono scegliere di disabilitare questo comportamento o personalizzare il nome e la descrizione del connettore di ricerca del gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="099b8-121">Applications with protocol handlers can choose to disable this behavior or customize the name and description of the protocol handler search connector.</span></span>

> [!Note]  
> <span data-ttu-id="099b8-122">Il percorso della cartella **ricerche** dell'utente è% UserProfile% \\ searchs oppure FOLDERID \_ SavedSearches.</span><span class="sxs-lookup"><span data-stu-id="099b8-122">The location of the user's **Searches** folder is %userprofile%\\Searches, or FOLDERID\_SavedSearches.</span></span> <span data-ttu-id="099b8-123">Il GUID per FOLDERID \_ SavedSearches è {7d1d3a04-Debb-4115-95cf-2f29da2920da}.</span><span class="sxs-lookup"><span data-stu-id="099b8-123">The GUID for FOLDERID\_SavedSearches is {7d1d3a04-debb-4115-95cf-2f29da2920da}.</span></span>

 

<span data-ttu-id="099b8-124">Esplora risorse consente di controllare la creazione di un connettore di ricerca per un gestore di protocollo tramite le voci della chiave del registro di sistema descritte nelle seguenti sezioni:</span><span class="sxs-lookup"><span data-stu-id="099b8-124">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries described in the following sections:</span></span>

-   [<span data-ttu-id="099b8-125">Abilitazione di gestori di protocollo per partecipare alla ricerca</span><span class="sxs-lookup"><span data-stu-id="099b8-125">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
-   [<span data-ttu-id="099b8-126">Disabilitazione della creazione del connettore di ricerca del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-126">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
-   [<span data-ttu-id="099b8-127">Personalizzazione del nome, della descrizione o del FolderType per un connettore di ricerca del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-127">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [<span data-ttu-id="099b8-128">Ripristino di un connettore di ricerca del gestore di protocollo eliminato</span><span class="sxs-lookup"><span data-stu-id="099b8-128">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> <span data-ttu-id="099b8-129">Non esiste alcun mezzo programmatico per creare un connettore di ricerca per un gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="099b8-129">There are no programmatic means to create a search connector for a protocol handler.</span></span> <span data-ttu-id="099b8-130">Devono essere configurate tramite il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="099b8-130">They must be configured through the registry.</span></span>

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a><span data-ttu-id="099b8-131">Abilitazione di gestori di protocollo per partecipare alla ricerca</span><span class="sxs-lookup"><span data-stu-id="099b8-131">Enabling Protocol Handlers to Participate in Search</span></span>

<span data-ttu-id="099b8-132">Le chiavi del registro di sistema e i relativi valori possibili sono illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="099b8-132">Registry keys and their possible values are outlined in the following table.</span></span> <span data-ttu-id="099b8-133">Un gestore di protocollo può popolare alcune o tutte queste chiavi del registro di sistema dove <protocol> viene sostituito con il nome effettivo del protocollo, ad esempio MAPI, file o CSC.</span><span class="sxs-lookup"><span data-stu-id="099b8-133">A protocol handler can populate some or all of these registry keys where <protocol> is replaced with the actual name of its protocol, such as MAPI, file, or csc, for example.</span></span>



| <span data-ttu-id="099b8-134">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="099b8-134">Registry key</span></span>                                                                                                                 | <span data-ttu-id="099b8-135">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="099b8-135">Possible value(s)</span></span>                                                                                                                     | <span data-ttu-id="099b8-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="099b8-136">Type</span></span>       | <span data-ttu-id="099b8-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="099b8-137">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="099b8-138">HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ Version</span><span class="sxs-lookup"><span data-stu-id="099b8-138">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Version</span></span>                     | <span data-ttu-id="099b8-139">Non esiste (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="099b8-139">Does not exist (default).</span></span> <span data-ttu-id="099b8-140">In caso contrario, è maggiore o uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="099b8-140">Otherwise it is 1 or greater.</span></span>                                                                               | <span data-ttu-id="099b8-141">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="099b8-141">REG\_DWORD</span></span> | <span data-ttu-id="099b8-142">Questo valore viene usato per rilevare le modifiche alle registrazioni dei modelli di percorso per le radici di ricerca che sono già state elaborate.</span><span class="sxs-lookup"><span data-stu-id="099b8-142">This value is used to detect changes to the location template registrations for search roots that have already been processed.</span></span> <span data-ttu-id="099b8-143">Se non esiste, utilizzare 0 come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="099b8-143">If does not exist, use 0 as a default.</span></span> <span data-ttu-id="099b8-144">In alternativa, incrementare la versione per informare Esplora risorse che è necessario rigenerare il connettore di ricerca perché è stata installata una versione più recente del gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="099b8-144">Alternatively, increment the version to inform Windows Explorer that the search connector should be regenerated because a newer version of the protocol handler has been installed.</span></span> |
| <span data-ttu-id="099b8-145">HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ DoNotCreateSearchConnectors</span><span class="sxs-lookup"><span data-stu-id="099b8-145">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\DoNotCreateSearchConnectors</span></span> | <span data-ttu-id="099b8-146">Non esiste (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="099b8-146">Does not exist (default).</span></span> <span data-ttu-id="099b8-147">In caso contrario, impostare su 1.</span><span class="sxs-lookup"><span data-stu-id="099b8-147">Otherwise set to 1.</span></span>                                                                                         | <span data-ttu-id="099b8-148">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="099b8-148">REG\_DWORD</span></span> | <span data-ttu-id="099b8-149">Se non esiste, creare un file con estensione searchconnector-ms nella cartella ricerche.</span><span class="sxs-lookup"><span data-stu-id="099b8-149">If it does not exist, create a .searchconnector-ms file in the Searches folder.</span></span> <span data-ttu-id="099b8-150">Se 1, contrassegnare come elaborata e non eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="099b8-150">If 1, mark as processed and do nothing.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="099b8-151">HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ default \\ Description</span><span class="sxs-lookup"><span data-stu-id="099b8-151">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Description</span></span>        | <span data-ttu-id="099b8-152">Stringa localizzabile che contiene la descrizione del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="099b8-152">A localizable string containing the description of the search connector.</span></span>                                                              | <span data-ttu-id="099b8-153">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="099b8-153">REG\_SZ</span></span>    | <span data-ttu-id="099b8-154">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="099b8-154">Optional.</span></span> <span data-ttu-id="099b8-155">Viene usato nell'elemento Description del file con estensione searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="099b8-155">It is used in the Description element of the .searchconnector-ms file.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="099b8-156">HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ \\ nome predefinito</span><span class="sxs-lookup"><span data-stu-id="099b8-156">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Name</span></span>               | <span data-ttu-id="099b8-157">Stringa localizzata per assegnare un nome al connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="099b8-157">A localized string to name the search connector.</span></span> <span data-ttu-id="099b8-158">Usato come nome del file con estensione searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="099b8-158">Used as the name of the .searchconnector-ms file.</span></span>                                    | <span data-ttu-id="099b8-159">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="099b8-159">REG\_SZ</span></span>    | <span data-ttu-id="099b8-160">Ogni percorso deve avere un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="099b8-160">Each location must have a unique name.</span></span> <span data-ttu-id="099b8-161">In assenza di questo valore, verrà utilizzato il nome visualizzato fornito dall' [interfaccia IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="099b8-161">In the absence of this value, the display name provided by the protocol handler's [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) will be used.</span></span>                                                                                                                             |
| <span data-ttu-id="099b8-162">HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ default \\ FolderType</span><span class="sxs-lookup"><span data-stu-id="099b8-162">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\FolderType</span></span>         | <span data-ttu-id="099b8-163">GUID che identifica il [FOLDERTYPEID](../shell/foldertypeid.md) da applicare al connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="099b8-163">A GUID identifying the [FOLDERTYPEID](../shell/foldertypeid.md) to apply to the search connector.</span></span> | <span data-ttu-id="099b8-164">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="099b8-164">REG\_SZ</span></span>    | <span data-ttu-id="099b8-165">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="099b8-165">Optional.</span></span> <span data-ttu-id="099b8-166">Usato nell'elemento folderType del file con estensione searchconnector-ms per indicare quali modelli devono essere usati per visualizzare i risultati.</span><span class="sxs-lookup"><span data-stu-id="099b8-166">Used in the folderType element of the .searchconnector-ms file to indicate what templates should be used to display results.</span></span> <span data-ttu-id="099b8-167">Ad esempio, il valore GUID di FOLDERTYPEID \_ Documents.</span><span class="sxs-lookup"><span data-stu-id="099b8-167">For example, the GUID value of FOLDERTYPEID\_Documents.</span></span>                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a><span data-ttu-id="099b8-168">Disabilitazione della creazione del connettore di ricerca del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-168">Disabling Protocol Handler Search Connector Creation</span></span>

<span data-ttu-id="099b8-169">Se l'applicazione espone elementi tramite un gestore di protocollo per l'uso nell'applicazione stessa e non si vuole esporre gli elementi tramite la shell (nel menu **Start** e nelle ricerche in Esplora risorse), è necessario disabilitare la creazione di un connettore di ricerca per il gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="099b8-169">If your application exposes items through a protocol handler for use in the application itself and you do not want to expose the items through the Shell (in **Start** menu and Windows Explorer searches), you need to disable the creation of a search connector for your protocol handler.</span></span>

<span data-ttu-id="099b8-170">Per disabilitare la creazione del connettore di ricerca, impostare DoNotCreateSearchConnectors su 0x00000001 (1), come illustrato nell'esempio di chiave del registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="099b8-170">To disable search connector creation set DoNotCreateSearchConnectors to 0x00000001(1), as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

<span data-ttu-id="099b8-171">Se DoNotCreateSearchConnectors è impostato su 1, è consigliabile esporre la proprietà [System. Shell. OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) per ogni elemento esposto dal gestore di protocollo e impostare il valore di questa proprietà su **true**.</span><span class="sxs-lookup"><span data-stu-id="099b8-171">If DoNotCreateSearchConnectors is set to 1, then we recommend that you expose the [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) property on each item exposed by the protocol handler, and set the value of this property to **TRUE**.</span></span> <span data-ttu-id="099b8-172">In questo modo, gli elementi del gestore di protocollo non verranno visualizzati nel gruppo **file** del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="099b8-172">Doing so will prevent the protocol handler items from appearing under the **Start** menu **Files** group.</span></span>

<span data-ttu-id="099b8-173">Se DoNotCreateSearchConnectors è presente e impostato su zero, Esplora risorse creerà un connettore di ricerca per il gestore di protocollo e gli elementi del gestore di protocollo verranno restituiti nel menu **Start** e nelle ricerche in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="099b8-173">If DoNotCreateSearchConnectors is present and set to zero, then Windows Explorer will create a search connector for the protocol handler, and the protocol handler items will be returned in in **Start** menu and Windows Explorer searches.</span></span>

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a><span data-ttu-id="099b8-174">Personalizzazione del nome, della descrizione o del FolderType per un connettore di ricerca del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-174">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>

<span data-ttu-id="099b8-175">Il nome del connettore di ricerca viene usato non solo per identificare il connettore di ricerca nella cartella **ricerche** , ma come l'intestazione di gruppo per i risultati in ricerche nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="099b8-175">The search connector name is used not only to identify the search connector in the **Searches** folder, but as the group header for the results in **Start** menu searches.</span></span> <span data-ttu-id="099b8-176">È quindi importante fornire un nome descrittivo per il connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="099b8-176">Hence, it is important to provide a descriptive name for the search connector.</span></span> <span data-ttu-id="099b8-177">Se nella chiave del registro di sistema non viene specificato un nome, per impostazione predefinita Esplora risorse usa il nome fornito dall' [interfaccia IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) per la radice di ricerca del gestore di protocollo e la descrizione vuota.</span><span class="sxs-lookup"><span data-stu-id="099b8-177">If a name is not provided in the registry key, by default Windows Explorer uses the name provided by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) for the protocol handler's search root and blank description.</span></span> <span data-ttu-id="099b8-178">È possibile eseguire l'override del nome predefinito tramite una voce della chiave del registro di sistema senza dover rinominare l'interfaccia IShellFolder.</span><span class="sxs-lookup"><span data-stu-id="099b8-178">You can override the default name through a registry key entry without having to rename the IShellFolder Interface.</span></span> <span data-ttu-id="099b8-179">Anche se non è visibile come nome del connettore di ricerca, è anche possibile eseguire l'override della descrizione per il connettore di ricerca fornendo una descrizione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="099b8-179">Although it is not as visible as the search connector name, you can also override the description for the search connector by providing your own description.</span></span>

<span data-ttu-id="099b8-180">Per eseguire l'override del nome o della descrizione predefinita, impostare le voci come illustrato nell'esempio di registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="099b8-180">To override the default name or description, set the entries as shown in the following registry example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

<span data-ttu-id="099b8-181">Inoltre, la voce FolderType può essere impostata su uno dei GUID di [FOLDERTYPEID](../shell/foldertypeid.md) .</span><span class="sxs-lookup"><span data-stu-id="099b8-181">In addition, the FolderType entry can be set to one of the [FOLDERTYPEID](../shell/foldertypeid.md) GUIDs.</span></span> <span data-ttu-id="099b8-182">Il valore deve essere il GUID effettivo e non il nome.</span><span class="sxs-lookup"><span data-stu-id="099b8-182">The value should be the actual GUID, and not its name.</span></span> <span data-ttu-id="099b8-183">Ad esempio, {94d6ddcc-4a68-4175-A374-bd584a510b78} anziché FOLDERTYPEID \_ Music.</span><span class="sxs-lookup"><span data-stu-id="099b8-183">For example, {94d6ddcc-4a68-4175-a374-bd584a510b78} rather than FOLDERTYPEID\_Music.</span></span> <span data-ttu-id="099b8-184">Il GUID di un FOLDERTYPEID può essere ottenuto nel file di intestazione Shlguid. h nella [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="099b8-184">The GUID for a FOLDERTYPEID can be obtained in the Shlguid.h header file in the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a><span data-ttu-id="099b8-185">Uso del reindirizzamento delle stringhe del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="099b8-185">Using Registry String Redirection</span></span>

<span data-ttu-id="099b8-186">È possibile usare una [stringa reindirizzata](../intl/using-registry-string-redirection.md) per verificare che il nome fornito per il connettore di ricerca possa essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="099b8-186">You can use a [redirected string](../intl/using-registry-string-redirection.md) to ensure that the name you provide for the search connector can be localized.</span></span> <span data-ttu-id="099b8-187">È possibile includere stringhe localizzabili per le chiavi del registro di sistema Name e Description anziché immettere la stringa effettiva nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="099b8-187">You can include localizable strings for the name and description registry keys instead of entering the actual string into the registry.</span></span>

<span data-ttu-id="099b8-188">Per includere una stringa localizzabile per i valori del nome o della descrizione, impostare il valore come illustrato nell'esempio di chiave del registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="099b8-188">To include a localizable string for the Name or Description values, set the value as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

<span data-ttu-id="099b8-189">La stringa localizzabile assume il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="099b8-189">The localizable string takes the following format:</span></span>

-   <span data-ttu-id="099b8-190">@dllname.dll,-resourceID, dove:</span><span class="sxs-lookup"><span data-stu-id="099b8-190">@dllname.dll,-resourceID, where:</span></span>
    -   <span data-ttu-id="099b8-191">@dllname.dll è il percorso della DLL che contiene la risorsa stringa</span><span class="sxs-lookup"><span data-stu-id="099b8-191">@dllname.dll is the path to the DLL that contains the string resource</span></span>
    -   <span data-ttu-id="099b8-192">resourceID è l'ID di risorsa Integer della risorsa stringa</span><span class="sxs-lookup"><span data-stu-id="099b8-192">resourceID is the integer resource ID of the string resource</span></span>

<span data-ttu-id="099b8-193">Il formato di una stringa indiretta e di una stringa indiretta aggiunta con un modificatore di versione è descritto nella [funzione SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="099b8-193">The format for an indirect string, and an indirect string appended with a version modifier, is described in [SHLoadIndirectString Function](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span>

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a><span data-ttu-id="099b8-194">Ripristino di un connettore di ricerca del gestore di protocollo eliminato</span><span class="sxs-lookup"><span data-stu-id="099b8-194">Restoring a Deleted Protocol Handler Search Connector</span></span>

<span data-ttu-id="099b8-195">Poiché i connettori di ricerca sono file nel computer dell'utente, possono essere eliminati erroneamente.</span><span class="sxs-lookup"><span data-stu-id="099b8-195">Because search connectors are files on the user's computer, they can be mistakenly deleted.</span></span> <span data-ttu-id="099b8-196">Per ripristinare tutti i connettori di ricerca del gestore di protocollo eliminati, ripristinare le librerie predefinite.</span><span class="sxs-lookup"><span data-stu-id="099b8-196">To restore all deleted protocol handler search connectors, restore the default libraries.</span></span> <span data-ttu-id="099b8-197">A tale scopo, aprire Esplora risorse, fare clic con il pulsante destro del mouse sulla cartella **librerie** e quindi scegliere **Ripristina librerie predefinite**.</span><span class="sxs-lookup"><span data-stu-id="099b8-197">To so do, open Windows Explorer, right-click the **Libraries** folder, and then select **Restore Default Libraries**.</span></span>

![screenshot che mostra l'opzione di menu Ripristina librerie predefinite](images/libraries.png)

## <a name="additional-resources"></a><span data-ttu-id="099b8-199">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="099b8-199">Additional Resources</span></span>

-   [<span data-ttu-id="099b8-200">IShellItem:: GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="099b8-200">IShellItem::GetDisplayName</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [<span data-ttu-id="099b8-201">\_NORMALDISPLAY SIGDN</span><span class="sxs-lookup"><span data-stu-id="099b8-201">SIGDN\_NORMALDISPLAY</span></span>](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a><span data-ttu-id="099b8-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="099b8-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="099b8-203">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="099b8-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="099b8-204">Informazioni sui gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-204">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="099b8-205">Sviluppo di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-205">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="099b8-206">Notifica dell'indice delle modifiche</span><span class="sxs-lookup"><span data-stu-id="099b8-206">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="099b8-207">Aggiunta di icone e menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="099b8-207">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="099b8-208">Esempio di codice: estensioni della Shell per i gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-208">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="099b8-209">Installazione e registrazione di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-209">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="099b8-210">Debug di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="099b8-210">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 

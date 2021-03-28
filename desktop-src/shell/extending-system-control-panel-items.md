---
description: Alcuni degli elementi di sistema disponibili nel pannello di controllo sono estendibili. Per installare un'estensione del pannello di controllo, registrare l'estensione della shell nel modo seguente, dove nome è il nome predefinito dell'elemento di sistema (vedere la tabella riportata di seguito).
title: Estensione degli elementi del pannello di controllo di sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993869"
---
# <a name="extending-system-control-panel-items"></a><span data-ttu-id="1d84f-104">Estensione degli elementi del pannello di controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="1d84f-104">Extending System Control Panel Items</span></span>

<span data-ttu-id="1d84f-105">Alcuni degli elementi di sistema disponibili nel pannello di controllo sono estendibili.</span><span class="sxs-lookup"><span data-stu-id="1d84f-105">Some of the system items found in the Control Panel are extensible.</span></span> <span data-ttu-id="1d84f-106">Per installare un'estensione del pannello di controllo, registrare l'estensione della shell nel modo seguente, dove *nome* è il nome predefinito dell'elemento di sistema (vedere la tabella riportata di seguito).</span><span class="sxs-lookup"><span data-stu-id="1d84f-106">To install a Control Panel extension, register your Shell extension as follows, where *name* is the predefined name of the system item (see table below).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

<span data-ttu-id="1d84f-107">Questa operazione è simile alla modalità di registrazione di un'estensione per un oggetto shell predefinito.</span><span class="sxs-lookup"><span data-stu-id="1d84f-107">This is similar to the way you would register an extension for a predefined Shell object.</span></span> <span data-ttu-id="1d84f-108">Poiché le uniche estensioni della shell supportate dagli elementi del pannello di controllo sono finestre delle proprietà, la registrazione deve trovarsi nella sottochiave **ShellEx** \\ **PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="1d84f-108">Because the only Shell extensions supported by Control Panel items are property sheets, the registration must be under the **shellex**\\**PropertySheetHandlers** subkey.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d84f-109">Elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="1d84f-109">Control Panel item</span></span></th>
<th><span data-ttu-id="1d84f-110"><em>nome</em></span><span class="sxs-lookup"><span data-stu-id="1d84f-110"><em>name</em></span></span></th>
<th><span data-ttu-id="1d84f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d84f-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d84f-112">Visualizza</span><span class="sxs-lookup"><span data-stu-id="1d84f-112">Display</span></span></td>
<td><span data-ttu-id="1d84f-113">Reception</span><span class="sxs-lookup"><span data-stu-id="1d84f-113">Desk</span></span></td>
<td><span data-ttu-id="1d84f-114">Supporta anche la sostituzione della pagina <strong>Desktop</strong> .</span><span class="sxs-lookup"><span data-stu-id="1d84f-114">Also supports replacement of the <strong>Desktop</strong> page.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1d84f-115">Questa operazione non è più supportata in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d84f-115">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d84f-116">Impostazioni di visualizzazione avanzate</span><span class="sxs-lookup"><span data-stu-id="1d84f-116">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="1d84f-117">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="1d84f-117">Device</span></span></td>
<td><span data-ttu-id="1d84f-118">Proprietà avanzate non specifiche dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="1d84f-118">Nonhardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1d84f-119">Questa operazione non è più supportata in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d84f-119">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d84f-120">Impostazioni di visualizzazione avanzate</span><span class="sxs-lookup"><span data-stu-id="1d84f-120">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="1d84f-121">Visualizza</span><span class="sxs-lookup"><span data-stu-id="1d84f-121">Display</span></span></td>
<td><span data-ttu-id="1d84f-122">Proprietà avanzate specifiche dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="1d84f-122">Hardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1d84f-123">Questa operazione non è più supportata in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d84f-123">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d84f-124">Opzioni Internet</span><span class="sxs-lookup"><span data-stu-id="1d84f-124">Internet Options</span></span></td>
<td><span data-ttu-id="1d84f-125">Internet</span><span class="sxs-lookup"><span data-stu-id="1d84f-125">Internet</span></span></td>
<td><span data-ttu-id="1d84f-126">Il numero massimo di pagine di estensione è 18.</span><span class="sxs-lookup"><span data-stu-id="1d84f-126">The maximum number of extension pages is 18.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d84f-127">Tastiera</span><span class="sxs-lookup"><span data-stu-id="1d84f-127">Keyboard</span></span></td>
<td><span data-ttu-id="1d84f-128">Tastiera</span><span class="sxs-lookup"><span data-stu-id="1d84f-128">Keyboard</span></span></td>
<td><span data-ttu-id="1d84f-129">Il numero massimo di pagine di estensione è 30.</span><span class="sxs-lookup"><span data-stu-id="1d84f-129">The maximum number of extension pages is 30.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d84f-130">Mouse</span><span class="sxs-lookup"><span data-stu-id="1d84f-130">Mouse</span></span></td>
<td><span data-ttu-id="1d84f-131">Mouse</span><span class="sxs-lookup"><span data-stu-id="1d84f-131">Mouse</span></span></td>
<td><span data-ttu-id="1d84f-132">Supporta anche la sostituzione di pagine standard.</span><span class="sxs-lookup"><span data-stu-id="1d84f-132">Also supports replacement of standard pages.</span></span> <span data-ttu-id="1d84f-133">Il numero massimo di pagine di estensione è 8.</span><span class="sxs-lookup"><span data-stu-id="1d84f-133">The maximum number of extension pages is 8.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d84f-134">Opzioni risparmio energia</span><span class="sxs-lookup"><span data-stu-id="1d84f-134">Power Options</span></span></td>
<td><span data-ttu-id="1d84f-135">Potenza</span><span class="sxs-lookup"><span data-stu-id="1d84f-135">Power</span></span></td>
<td><span data-ttu-id="1d84f-136">Il numero massimo di pagine, incluse le pagine standard, è 18.</span><span class="sxs-lookup"><span data-stu-id="1d84f-136">The maximum number of pages, including standard pages, is 18.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d84f-137">Sistema</span><span class="sxs-lookup"><span data-stu-id="1d84f-137">System</span></span></td>
<td><span data-ttu-id="1d84f-138">Sistema</span><span class="sxs-lookup"><span data-stu-id="1d84f-138">System</span></span></td>
<td><span data-ttu-id="1d84f-139">Il numero massimo di pagine di estensione è 8.</span><span class="sxs-lookup"><span data-stu-id="1d84f-139">The maximum number of extension pages is 8.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1d84f-140">Questa operazione non è più supportata in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d84f-140">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1d84f-141">L'elemento **Installazione applicazioni** nel pannello di controllo di Windows XP non è una finestra delle proprietà e pertanto non può essere esteso dai metodi descritti qui.</span><span class="sxs-lookup"><span data-stu-id="1d84f-141">The **Add or Remove Programs** item in the Windows XP Control Panel is not a property sheet and therefore cannot be extended by the methods discussed here.</span></span> <span data-ttu-id="1d84f-142">Il relativo contenuto viene invece ottenuto dagli autori dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d84f-142">Instead, its content is obtained from application publishers.</span></span> <span data-ttu-id="1d84f-143">Per ulteriori informazioni sull'aggiunta di contenuto per l'aggiunta **o la rimozione di programmi**, vedere [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)e [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span><span class="sxs-lookup"><span data-stu-id="1d84f-143">For more information on adding content to **Add or Remove Programs**, see [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps), and [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d84f-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d84f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d84f-145">Elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="1d84f-145">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="1d84f-146">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="1d84f-146">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="1d84f-147">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="1d84f-147">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1d84f-148">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="1d84f-148">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="1d84f-149">Elaborazione del messaggio del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="1d84f-149">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="1d84f-150">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="1d84f-150">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1d84f-151">Assegnazione delle categorie del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="1d84f-151">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="1d84f-152">Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="1d84f-152">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="1d84f-153">Accesso al pannello di controllo in modalità provvisoria in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d84f-153">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 





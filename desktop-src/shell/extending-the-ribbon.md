---
description: Informazioni su come estendere la barra multifunzione di Esplora risorse.
title: Estensione della barra multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525321"
---
# <a name="extending-the-ribbon"></a><span data-ttu-id="431e6-103">Estensione della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="431e6-103">Extending the Ribbon</span></span>

<span data-ttu-id="431e6-104">In Esplora risorse, la barra multifunzione consente di semplificare e rendere più individuabili le attività comuni di gestione dei file degli utenti finali, ma sono state apportate modifiche per gli sviluppatori di app.</span><span class="sxs-lookup"><span data-stu-id="431e6-104">In Windows Explorer, the Ribbon helps make common end-user file management activities easier and more discoverable, but there are changes afoot for app developers.</span></span> <span data-ttu-id="431e6-105">La barra dei comandi precedente, ad esempio, è stata liberamente estendibile, ma al momento la barra multifunzione è più limitata.</span><span class="sxs-lookup"><span data-stu-id="431e6-105">For example, the old command bar was freely extensible but the Ribbon is more restricted at this time.</span></span> <span data-ttu-id="431e6-106">Inoltre, la barra multifunzione non viene visualizzata per impostazione predefinita per tutte le estensioni dello spazio dei nomi, quindi è necessario acconsentire esplicitamente per ottenere la barra multifunzione. in caso contrario, si otterrà la barra dei comandi precedente.</span><span class="sxs-lookup"><span data-stu-id="431e6-106">Also, the Ribbon is not shown by default for all namespace extensions, so you have to opt in to get the Ribbon; otherwise, you get the older command bar.</span></span>

<span data-ttu-id="431e6-107">Le azioni disponibili per gli utenti sulla barra multifunzione rientrano in tre categorie di estensibilità:</span><span class="sxs-lookup"><span data-stu-id="431e6-107">Actions available to users on the Ribbon fall into three extensibility categories:</span></span>

-   <span data-ttu-id="431e6-108">L'estendibilità non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="431e6-108">Extensibility is not needed.</span></span> <span data-ttu-id="431e6-109">Esempi: copia, incolla, Elimina.</span><span class="sxs-lookup"><span data-stu-id="431e6-109">Examples: Copy, Paste, Delete.</span></span> <span data-ttu-id="431e6-110">Windows gestisce automaticamente questi verbi.</span><span class="sxs-lookup"><span data-stu-id="431e6-110">Windows handles these verbs for you.</span></span>
-   <span data-ttu-id="431e6-111">L'estendibilità non è attualmente consentita: esempi: zip, chiusura sessione e altre azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="431e6-111">Extensibility is not currently allowed: Examples: Zip, Close Session, and other custom actions.</span></span> <span data-ttu-id="431e6-112">Utilizzare il menu di scelta rapida per coprire questi scenari.</span><span class="sxs-lookup"><span data-stu-id="431e6-112">Use the context menu to cover these scenarios.</span></span>
-   <span data-ttu-id="431e6-113">L'estendibilità è incorporata nell'azione stessa.</span><span class="sxs-lookup"><span data-stu-id="431e6-113">Extensibility is built into the action itself.</span></span> <span data-ttu-id="431e6-114">Esempi: ricerca, posta elettronica, stampa, nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="431e6-114">Examples: Search, Email, Print, New Item.</span></span> <span data-ttu-id="431e6-115">È necessario registrarsi per questi verbi per includere l'app o il formato di file nella barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="431e6-115">You need to register for these verbs to include your app or file format in the Ribbon .</span></span>

<span data-ttu-id="431e6-116">Questo documento descrive come è possibile acconsentire esplicitamente per ottenere la barra multifunzione e come eseguire la registrazione per gestire i verbi della barra multifunzione specifici.</span><span class="sxs-lookup"><span data-stu-id="431e6-116">This document describes how you can opt-in to get the Ribbon, and how to register to handle specific Ribbon verbs.</span></span>

## <a name="opting-in-to-the-ribbon"></a><span data-ttu-id="431e6-117">Scelta della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="431e6-117">Opting in to the Ribbon</span></span>

<span data-ttu-id="431e6-118">Per acconsentire esplicitamente alla barra multifunzione, l'implementazione di [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) deve specificare la **\_ barra multifunzione EP** in [**IExplorerPaneVisibility:: GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) e restituire **EPS \_ Force** EPS \| **\_ default \_ on**.</span><span class="sxs-lookup"><span data-stu-id="431e6-118">To opt in to the Ribbon, your [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) implementation should specify **EP\_Ribbon** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) and return **EPS\_FORCE** \| **EPS\_DEFAULT\_ON**.</span></span>

## <a name="extending-the-ribbon-for-file-extensions"></a><span data-ttu-id="431e6-119">Estensione della barra multifunzione per le estensioni di file</span><span class="sxs-lookup"><span data-stu-id="431e6-119">Extending the Ribbon for File Extensions</span></span>

<span data-ttu-id="431e6-120">Questi pulsanti della barra multifunzione sono estendibili in base alle estensioni di file:</span><span class="sxs-lookup"><span data-stu-id="431e6-120">These Ribbon buttons are extensible based on file extensions:</span></span>

-   <span data-ttu-id="431e6-121">Estrai tutto</span><span class="sxs-lookup"><span data-stu-id="431e6-121">Extract All</span></span>
-   <span data-ttu-id="431e6-122">Montaggio \| Burn (ISO)</span><span class="sxs-lookup"><span data-stu-id="431e6-122">Mount \| Burn (an ISO)</span></span>
-   <span data-ttu-id="431e6-123">Riproduci \| tutto \| Aggiungi a playlist (verbo: Accoda)</span><span class="sxs-lookup"><span data-stu-id="431e6-123">Play \| Play All \| Add to Playlist (verb: Enqueue)</span></span>
-   <span data-ttu-id="431e6-124">Apri</span><span class="sxs-lookup"><span data-stu-id="431e6-124">Open</span></span>
-   <span data-ttu-id="431e6-125">Modifica</span><span class="sxs-lookup"><span data-stu-id="431e6-125">Edit</span></span>
-   <span data-ttu-id="431e6-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="431e6-126">Properties</span></span>

<span data-ttu-id="431e6-127">Quando si esegue la registrazione per gestire in modo statico i verbi pertinenti per i nuovi tipi di file, la barra multifunzione gestisce i verbi in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="431e6-127">When you register to statically handle the relevant verbs for new file types, the Ribbon handles the verbs appropriately.</span></span> <span data-ttu-id="431e6-128">Si esegue la registrazione come per i verbi del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="431e6-128">You register just as you would for context menu verbs.</span></span> <span data-ttu-id="431e6-129">Per ulteriori informazioni sulle associazioni di file e sulla registrazione per i verbi, vedere [verbi e associazioni di file](fa-verbs.md) e [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="431e6-129">For more information about file associations and registering for verbs, see [Verbs and File Associations](fa-verbs.md) and [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="registering-as-a-default-handler-for-actionids"></a><span data-ttu-id="431e6-130">Registrazione come gestore predefinito per dizionario</span><span class="sxs-lookup"><span data-stu-id="431e6-130">Registering as a Default Handler for ActionIds</span></span>

<span data-ttu-id="431e6-131">Per prima cosa, registrare il ProgId nella sottochiave AssocActionId appropriata.</span><span class="sxs-lookup"><span data-stu-id="431e6-131">First, register your ProgId under the appropriate AssocActionId subkey.</span></span> <span data-ttu-id="431e6-132">Ogni sottochiave AssocActionId rappresenta un verbo o un'azione che gli utenti possono richiamare dalla barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="431e6-132">Each AssocActionId subkey represents a verb or action that users can invoke from the Ribbon.</span></span> <span data-ttu-id="431e6-133">In questo esempio l'app esegue la registrazione per il ActionID ZipSelection per estendere il pulsante "Estrai tutto" sulla barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="431e6-133">In this example, the app registers for the ZipSelection ActionID to extend the "Extract All" button on the Ribbon.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

<span data-ttu-id="431e6-134">Una volta completata la registrazione, è necessario registrarsi per gestire i protocolli esattamente come si farebbe normalmente, come descritto in [programmi predefiniti](default-programs.md).</span><span class="sxs-lookup"><span data-stu-id="431e6-134">Once that registration is complete, you must then register to handle protocols just as you normally would, as described in [Default Programs](default-programs.md).</span></span>

 

 




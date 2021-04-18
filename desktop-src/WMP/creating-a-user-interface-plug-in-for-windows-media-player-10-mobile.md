---
title: Creazione di un plug-in dell'interfaccia utente per Windows Media Player 10 Mobile
description: Creazione di un plug-in dell'interfaccia utente per Windows Media Player 10 Mobile
ms.assetid: 050418b7-d99c-49ab-8ce6-6511b194ffe6
keywords:
- Windows Media Player Mobile, plug-in
- Plug-in di Windows Media Player Mobile, interfaccia utente
- Plug-in di Windows Media Player Mobile
- plug-in, interfaccia utente
- plug-in, Windows Media Player Mobile
- plug-in dell'interfaccia utente, Windows Media Player Mobile
- Plug-in dell'interfaccia utente, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d649ef1d8ed1b8fb1e1b54dc7eed106f798b1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298385"
---
# <a name="creating-a-user-interface-plug-in-for-windows-media-player-10-mobile"></a><span data-ttu-id="0c2ca-110">Creazione di un plug-in dell'interfaccia utente per Windows Media Player 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="0c2ca-110">Creating a User Interface Plug-in for Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="0c2ca-111">Windows Media Player 10 Mobile USA lo stesso modello di plug-in dell'interfaccia utente del Media Player desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-111">Windows Media Player 10 Mobile uses the same UI plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="0c2ca-112">Tuttavia, Windows Media Player 10 Mobile può interagire solo con i plug-in di interfaccia utente in background. A causa dei modelli di plug-in simili, le stesse chiamate API applicabili ai plug-in di interfaccia utente in background sul desktop si applicano anche ai plug-in di interfaccia utente in background in un dispositivo Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-112">However, Windows Media Player 10 Mobile can only interact with background UI plug-ins. Because of the similar plug-in models, the same API calls that apply to background UI plug-ins on the desktop also apply to background UI plug-ins on a Windows Mobile device.</span></span>

<span data-ttu-id="0c2ca-113">Le sezioni seguenti descrivono come creare un plug-in in background dell'interfaccia utente usando il codice generato dalla procedura guidata dalla procedura guidata per il plug-in di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-113">The following sections describe how to create a background UI plug-in by using wizard-generated code from the Windows Media Player Plug-in Wizard.</span></span>



| <span data-ttu-id="0c2ca-114">Sezione</span><span class="sxs-lookup"><span data-stu-id="0c2ca-114">Section</span></span>                                                                | <span data-ttu-id="0c2ca-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c2ca-115">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c2ca-116">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="0c2ca-116">Getting Started</span></span>](getting-started.md)                                 | <span data-ttu-id="0c2ca-117">Vengono descritti gli elementi necessari per installare e come utilizzare la procedura guidata plug-in di Windows Media Player per automatizzare la creazione di un plug-in di interfaccia utente in background.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-117">Describes what you need to install and how to use the Windows Media Player Plug-in Wizard to help automate the creation of a background UI plug-in.</span></span>    |
| [<span data-ttu-id="0c2ca-118">Modifica del codice generato dalla procedura guidata</span><span class="sxs-lookup"><span data-stu-id="0c2ca-118">Modifying Wizard-generated Code</span></span>](modifying-wizard-generated-code.md) | <span data-ttu-id="0c2ca-119">Viene descritto cosa è necessario modificare dal codice generato dalla procedura guidata creato nella sezione precedente, in modo che funzioni con Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-119">Describes what you need to modify from the wizard-generated code created in the previous section so that it works with Windows Media Player 10 Mobile.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0c2ca-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c2ca-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c2ca-121">**Guida alla programmazione di plug-in dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="0c2ca-121">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 





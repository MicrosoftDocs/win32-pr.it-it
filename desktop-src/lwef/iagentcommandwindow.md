---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298497"
---
# <a name="iagentcommandwindow"></a><span data-ttu-id="15fca-103">IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="15fca-103">IAgentCommandWindow</span></span>

<span data-ttu-id="15fca-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15fca-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="15fca-105">**IAgentCommandWindow** definisce un'interfaccia che consente alle applicazioni di impostare ed eseguire query sulle proprietà della finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="15fca-105">**IAgentCommandWindow** defines an interface that allows applications to set and query the properties of the Voice Commands Window.</span></span> <span data-ttu-id="15fca-106">La finestra comandi vocali è una risorsa condivisa progettata principalmente per consentire agli utenti di visualizzare i comandi abilitati per la voce.</span><span class="sxs-lookup"><span data-stu-id="15fca-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="15fca-107">Se il riconoscimento vocale è disabilitato, la finestra dei comandi vocali viene ancora visualizzata, con il testo "input vocale disabilitato" (nella lingua del carattere).</span><span class="sxs-lookup"><span data-stu-id="15fca-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="15fca-108">Se non è installato alcun motore vocale che corrisponda all'impostazione della lingua del carattere, viene visualizzata la finestra "input vocale non disponibile".</span><span class="sxs-lookup"><span data-stu-id="15fca-108">If no speech engine is installed that matches the character's language setting, the window displays, "Speech input not available."</span></span> <span data-ttu-id="15fca-109">Se il client di input-attivo non ha definito parametri vocali per i comandi e ha disabilitato i comandi vocali globali, nella finestra viene visualizzato "nessun comando vocale".</span><span class="sxs-lookup"><span data-stu-id="15fca-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="15fca-110">È anche possibile eseguire una query sulle proprietà della finestra dei comandi vocali indipendentemente dal fatto che l'input vocale sia disabilitato o che sia installato un motore di riconoscimento vocale compatibile.</span><span class="sxs-lookup"><span data-stu-id="15fca-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

<span data-ttu-id="15fca-111">**Metodi nell'ordine Vtable**</span><span class="sxs-lookup"><span data-stu-id="15fca-111">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="15fca-112">Metodi IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="15fca-112">IAgentCommandWindow Methods</span></span>                             | <span data-ttu-id="15fca-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15fca-113">Description</span></span>                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15fca-114">**SetVisible**</span><span class="sxs-lookup"><span data-stu-id="15fca-114">**SetVisible**</span></span>](iagentcommandwindow--setvisible.md)   | <span data-ttu-id="15fca-115">Imposta il valore della proprietà [**Visible**](visible-property.md) della finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="15fca-115">Sets the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span>    |
| [<span data-ttu-id="15fca-116">**GetVisible**</span><span class="sxs-lookup"><span data-stu-id="15fca-116">**GetVisible**</span></span>](iagentcommandwindow--getvisible.md)   | <span data-ttu-id="15fca-117">Restituisce il valore della proprietà [**Visible**](visible-property.md) della finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="15fca-117">Returns the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span> |
| [<span data-ttu-id="15fca-118">**GetPosition**</span><span class="sxs-lookup"><span data-stu-id="15fca-118">**GetPosition**</span></span>](iagentcommandwindow--getposition.md) | <span data-ttu-id="15fca-119">Restituisce la posizione della finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="15fca-119">Returns the position of the Voice Commands Window.</span></span>                                                  |
| [<span data-ttu-id="15fca-120">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="15fca-120">**GetSize**</span></span>](iagentcommandwindow--getsize.md)         | <span data-ttu-id="15fca-121">Restituisce le dimensioni della finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="15fca-121">Returns the size of the Voice Commands Window.</span></span>                                                      |



 

 

 





---
title: Comandi (nozioni di base sulla progettazione)
description: I comandi sono azioni che gli utenti possono eseguire durante l'uso dell'app. Informazioni sulle linee guida per l'aggiunta di comandi ai menu, alla barra multifunzione e alle barre degli strumenti dell'app.
ms.assetid: 64DF83BC-CC6D-4F0F-A1B2-AB3CF6DA33B3
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: ece3f8f4fe395bb6ccf20a2b8b3db6bb36b00aee
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761140"
---
# <a name="commands-design-basics"></a><span data-ttu-id="8e366-104">Comandi (nozioni di base sulla progettazione)</span><span class="sxs-lookup"><span data-stu-id="8e366-104">Commands (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="8e366-105">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="8e366-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="8e366-106">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="8e366-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="8e366-107">I comandi sono azioni che gli utenti possono eseguire durante l'uso dell'app.</span><span class="sxs-lookup"><span data-stu-id="8e366-107">Commands are actions users can take while using your app.</span></span> <span data-ttu-id="8e366-108">Informazioni sulle linee guida per l'aggiunta di comandi ai menu, alla barra multifunzione e alle barre degli strumenti dell'app.</span><span class="sxs-lookup"><span data-stu-id="8e366-108">Learn the guidelines for adding commands to your app's menus, ribbons, and toolbars.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8e366-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8e366-109">In this section</span></span>



| <span data-ttu-id="8e366-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="8e366-110">Topic</span></span>                                   | <span data-ttu-id="8e366-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e366-111">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e366-112">Menu</span><span class="sxs-lookup"><span data-stu-id="8e366-112">Menus</span></span>](cmd-menus.md)<br/>       | <span data-ttu-id="8e366-113">I menu sono elenchi gerarchici di comandi o opzioni disponibili per gli utenti nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="8e366-113">Menus are hierarchical lists of commands or options available to users in the current context.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="8e366-114">Barre multifunzione</span><span class="sxs-lookup"><span data-stu-id="8e366-114">Ribbons</span></span>](cmd-ribbons.md)<br/>   | <span data-ttu-id="8e366-115">Le barre multifunzione sono il modo moderno per aiutare gli utenti a trovare, comprendere e usare i comandi in modo efficiente e diretto con un numero minimo di clic, con una minore necessità di ricorrere a tentativi ed errori e senza dover fare riferimento alla guida.</span><span class="sxs-lookup"><span data-stu-id="8e366-115">Ribbons are the modern way to help users find, understand, and use commands efficiently and directly with a minimum number of clicks, with less need to resort to trial-and-error, and without having to refer to Help.</span></span><br/> |
| [<span data-ttu-id="8e366-116">Barre degli strumenti</span><span class="sxs-lookup"><span data-stu-id="8e366-116">Toolbars</span></span>](cmd-toolbars.md)<br/> | <span data-ttu-id="8e366-117">Le barre degli strumenti rappresentano un modo per raggruppare i comandi per un accesso efficiente.</span><span class="sxs-lookup"><span data-stu-id="8e366-117">Toolbars are a way to group commands for efficient access.</span></span><br/>                                                                                                                                                              |



 

 


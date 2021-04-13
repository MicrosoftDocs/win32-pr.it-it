---
title: Non essere esclusivo
description: Non essere esclusivo
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395643"
---
# <a name="be-non-exclusive"></a><span data-ttu-id="3ffee-103">Non essere esclusivo</span><span class="sxs-lookup"><span data-stu-id="3ffee-103">Be Non-Exclusive</span></span>

<span data-ttu-id="3ffee-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3ffee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3ffee-105">I caratteri interattivi possono essere utilizzati nell'interfaccia utente come assistenti, guide, intrattenitori, cantastorie, agenti di vendita o in diversi altri ruoli.</span><span class="sxs-lookup"><span data-stu-id="3ffee-105">Interactive characters can be employed in the user interface as assistants, guides, entertainers, storytellers, sales agents, or in a variety of other roles.</span></span> <span data-ttu-id="3ffee-106">Un carattere che esegue o assiste automaticamente non deve essere progettato in modo contrario al principio di progettazione per mantenere il controllo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3ffee-106">A character that automatically performs or assists should not be designed contrary to the design principle of keeping the user in control.</span></span> <span data-ttu-id="3ffee-107">Quando si aggiunge un carattere all'interfaccia di un sito Web o di un'applicazione convenzionale, utilizzare il carattere come miglioramento, anziché come sostituzione di, l'interfaccia principale.</span><span class="sxs-lookup"><span data-stu-id="3ffee-107">When adding a character to the interface of a website or conventional application, use the character as an enhancement, rather than a replacement of, the primary interface.</span></span> <span data-ttu-id="3ffee-108">Evitare di implementare funzionalità o operazioni che richiedono esclusivamente un carattere.</span><span class="sxs-lookup"><span data-stu-id="3ffee-108">Avoid implementing any feature or operation that exclusively requires a character.</span></span>

<span data-ttu-id="3ffee-109">Allo stesso modo, consentire all'utente di scegliere quando si desidera interagire con il carattere.</span><span class="sxs-lookup"><span data-stu-id="3ffee-109">Similarly, let the user choose when they want to interact with your character.</span></span> <span data-ttu-id="3ffee-110">Un utente dovrebbe essere in grado di chiudere il carattere e restituire solo con l'autorizzazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3ffee-110">A user should be able to dismiss the character and have it return only with the user's permission.</span></span> <span data-ttu-id="3ffee-111">La forzatura dell'interazione tra caratteri sugli utenti può avere un effetto negativo grave.</span><span class="sxs-lookup"><span data-stu-id="3ffee-111">Forcing character interaction on users can have a serious negative effect.</span></span> <span data-ttu-id="3ffee-112">Per supportare il controllo utente dell'interazione dei caratteri, Microsoft Agent include automaticamente i comandi Nascondi e Mostra.</span><span class="sxs-lookup"><span data-stu-id="3ffee-112">To support user control of character interaction, Microsoft Agent automatically includes Hide and Show commands.</span></span> <span data-ttu-id="3ffee-113">L'API di Microsoft Agent supporta inoltre questi metodi, pertanto è possibile includere il supporto per queste funzioni nella propria interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3ffee-113">The Microsoft Agent API also supports these methods, so you can include support for these functions in your own interface.</span></span> <span data-ttu-id="3ffee-114">Inoltre, l'interfaccia utente dell'agente Microsoft include proprietà globali che consentono all'utente di eseguire l'override di determinate opzioni di output dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="3ffee-114">In addition, Microsoft Agent's user interface includes global properties that enable the user to override certain character output options.</span></span> <span data-ttu-id="3ffee-115">Per assicurarsi che le preferenze dell'utente siano gestite, non è possibile eseguire l'override di queste proprietà tramite l'API.</span><span class="sxs-lookup"><span data-stu-id="3ffee-115">To ensure that the user's preferences are maintained, these properties cannot be overridden through the API.</span></span>

 

 





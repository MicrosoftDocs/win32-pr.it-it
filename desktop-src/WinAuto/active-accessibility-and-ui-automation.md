---
title: Active Accessibility e automazione interfaccia utente
description: Microsoft Active Accessibility è progettato per l'utilizzo con Windows XP e i sistemi operativi precedenti.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298879"
---
# <a name="active-accessibility-and-ui-automation"></a><span data-ttu-id="62efb-103">Active Accessibility e automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="62efb-103">Active Accessibility and UI Automation</span></span>

<span data-ttu-id="62efb-104">Microsoft Active Accessibility è progettato per l'utilizzo con Windows XP e i sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="62efb-104">Microsoft Active Accessibility is designed for use with Windows XP and earlier operating systems.</span></span> <span data-ttu-id="62efb-105">Gli sviluppatori di controlli personalizzati e di applicazioni client tecnologiche accessibili per Windows XP e Windows Vista dovrebbero prendere in considerazione l'uso di [automazione interfaccia utente](entry-uiauto-win32.md) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62efb-105">Developers of custom controls and accessible technology client applications for Windows XP and Windows Vista should consider using Microsoft [UI Automation](entry-uiauto-win32.md) instead.</span></span>

<span data-ttu-id="62efb-106">Automazione interfaccia utente Microsoft è un sistema completo che fornisce informazioni più precise sull'interfaccia utente e offre all'utente la possibilità di interagire con i controlli.</span><span class="sxs-lookup"><span data-stu-id="62efb-106">Microsoft UI Automation is a full-featured system that provides more precise information about the user interface and gives the user more ability to interact with controls.</span></span> <span data-ttu-id="62efb-107">In particolare, fornisce un supporto migliorato per il testo.</span><span class="sxs-lookup"><span data-stu-id="62efb-107">In particular, it provides greatly enhanced support for text.</span></span>

<span data-ttu-id="62efb-108">Un set di oggetti proxy fornisce supporto per l'automazione dell'interfaccia utente per i controlli standard di Microsoft Win32 e Windows Form.</span><span class="sxs-lookup"><span data-stu-id="62efb-108">A set of proxy objects provides UI Automation support for standard Microsoft Win32 and Windows Forms controls.</span></span> <span data-ttu-id="62efb-109">È disponibile un supporto più completo per i controlli specificamente scritti con l'automazione dell'interfaccia utente, inclusi gli elementi Windows Presentation Foundation nativi (WPF), che non supportano direttamente Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="62efb-109">Richer support is available for controls specifically written with UI Automation in mind, including native Windows Presentation Foundation (WPF) elements, which do not directly support Microsoft Active Accessibility.</span></span> <span data-ttu-id="62efb-110">I controlli personalizzati che supportano l'automazione dell'interfaccia utente possono essere scritti in codice gestito o non gestito.</span><span class="sxs-lookup"><span data-stu-id="62efb-110">Custom controls that support UI Automation can be written in either managed or unmanaged code.</span></span>

<span data-ttu-id="62efb-111">I client Microsoft Active Accessibility hanno accesso limitato, tramite un livello di bridging, agli elementi dell'interfaccia utente che supportano solo l'automazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="62efb-111">Microsoft Active Accessibility clients have limited access, through a bridging layer, to UI elements that support only UI Automation.</span></span> <span data-ttu-id="62efb-112">Per ulteriori informazioni, vedere [Appendice G: Active Accessibility Bridge per l'automazione interfaccia utente](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span><span class="sxs-lookup"><span data-stu-id="62efb-112">For more information, see [Appendix G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span></span>

<span data-ttu-id="62efb-113">Per ulteriori informazioni sulle analogie e le differenze tra Active Accessibility Microsoft e l'automazione dell'interfaccia utente, vedere [confronto tra microsoft Active Accessibility e automazione interfaccia utente](microsoft-active-accessibility-and-ui-automation-compared.md).</span><span class="sxs-lookup"><span data-stu-id="62efb-113">For more information about the similarities and differences between Microsoft Active Accessibility and UI Automation, see [Microsoft Active Accessibility and UI Automation Compared](microsoft-active-accessibility-and-ui-automation-compared.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62efb-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62efb-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="62efb-115">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="62efb-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62efb-116">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="62efb-116">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="62efb-117">Automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="62efb-117">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 





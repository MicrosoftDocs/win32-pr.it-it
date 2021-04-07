---
title: Registro eventi di Windows
description: L'API registro eventi di Windows definisce lo schema usato per scrivere un manifesto di strumentazione.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872934"
---
# <a name="windows-event-log"></a><span data-ttu-id="f8661-103">Registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="f8661-103">Windows Event Log</span></span>

## <a name="purpose"></a><span data-ttu-id="f8661-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="f8661-104">Purpose</span></span>

<span data-ttu-id="f8661-105">L'API registro eventi di Windows definisce lo schema usato per scrivere un manifesto di strumentazione.</span><span class="sxs-lookup"><span data-stu-id="f8661-105">The Windows Event Log API defines the schema that you use to write an instrumentation manifest.</span></span> <span data-ttu-id="f8661-106">Un manifesto di strumentazione identifica il provider di eventi e gli eventi registrati.</span><span class="sxs-lookup"><span data-stu-id="f8661-106">An instrumentation manifest identifies your event provider and the events that it logs.</span></span> <span data-ttu-id="f8661-107">L'API include anche le funzioni utilizzate da un consumer di eventi, ad esempio il [Visualizzatore eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), per leggere ed eseguire il rendering degli eventi.</span><span class="sxs-lookup"><span data-stu-id="f8661-107">The API also includes the functions that an event consumer, such as the [Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), would use to read and render the events.</span></span> <span data-ttu-id="f8661-108">Per scrivere gli eventi definiti nel manifesto, usare le funzioni incluse nell'API [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="f8661-108">To write the events defined in the manifest, use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span>

<span data-ttu-id="f8661-109">Il registro eventi di Windows sostituisce l'API di [registrazione eventi](/windows/desktop/EventLog/event-logging) a partire dal sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f8661-109">Windows Event Log supersedes the [Event Logging](/windows/desktop/EventLog/event-logging) API beginning with the Windows Vista operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f8661-110">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="f8661-110">Developer audience</span></span>

<span data-ttu-id="f8661-111">Il registro eventi di Windows è progettato per i programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="f8661-111">Windows Event Log is designed for C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f8661-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="f8661-112">Run-time requirements</span></span>

<span data-ttu-id="f8661-113">Il registro eventi di Windows è incluso nel sistema operativo a partire da Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f8661-113">Windows Event Log is included in the operating system beginning with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="f8661-114">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="f8661-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="f8661-115">Per la cronologia delle versioni completa [, vedere Novità](what-s-new.md).</span><span class="sxs-lookup"><span data-stu-id="f8661-115">For complete version history, see [What's New](what-s-new.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f8661-116">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f8661-116">In this section</span></span>


| <span data-ttu-id="f8661-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="f8661-117">Topic</span></span>                                                        | <span data-ttu-id="f8661-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8661-118">Description</span></span>                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8661-119">Utilizzo del registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="f8661-119">Using Windows Event Log</span></span>](using-windows-event-log.md)        | <span data-ttu-id="f8661-120">Guida procedurale che illustra come usare l'API registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="f8661-120">Procedural guide that shows how to use the Windows Event Log API.</span></span>                                 |
| [<span data-ttu-id="f8661-121">Riferimento al registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="f8661-121">Windows Event Log Reference</span></span>](windows-event-log-reference.md)| <span data-ttu-id="f8661-122">Tipi di dati, funzioni, enumerazioni, strutture, costanti e schemi inclusi nell'API.</span><span class="sxs-lookup"><span data-stu-id="f8661-122">The data types, functions, enumerations, structures, constants, and schemas that the API includes.</span></span>|
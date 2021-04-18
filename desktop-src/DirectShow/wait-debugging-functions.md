---
description: Funzioni di debug di attesa
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funzioni di debug di attesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308946"
---
# <a name="wait-debugging-functions"></a><span data-ttu-id="5452e-103">Funzioni di debug di attesa</span><span class="sxs-lookup"><span data-stu-id="5452e-103">Wait Debugging Functions</span></span>

<span data-ttu-id="5452e-104">Microsoft DirectShow fornisce diverse funzioni per il debug di attese infinite.</span><span class="sxs-lookup"><span data-stu-id="5452e-104">Microsoft DirectShow provides several functions for debugging infinite waits.</span></span>

<span data-ttu-id="5452e-105">Nelle compilazioni al dettaglio, le funzioni [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funzionano come le controparti API Windows, **WaitForMultipleObjects** e **WaitForSingleObject**, con intervalli di timeout infiniti.</span><span class="sxs-lookup"><span data-stu-id="5452e-105">In retail builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions work like their Windows API counterparts, **WaitForMultipleObjects** and **WaitForSingleObject**, with infinite time-out intervals.</span></span>

<span data-ttu-id="5452e-106">Nelle build di debug queste funzioni usano un valore di timeout globale.</span><span class="sxs-lookup"><span data-stu-id="5452e-106">In debug builds, these functions use a global time-out value.</span></span> <span data-ttu-id="5452e-107">Se il timeout scade, la funzione attiva un'asserzione.</span><span class="sxs-lookup"><span data-stu-id="5452e-107">If the time-out expires, the function triggers an assert.</span></span> <span data-ttu-id="5452e-108">La seguente chiave del registro di sistema specifica il valore di timeout, in millisecondi:</span><span class="sxs-lookup"><span data-stu-id="5452e-108">The following registry key specifies the time-out value, in milliseconds:</span></span>

<span data-ttu-id="5452e-109">**\_ \_ \\ <DebugRoot> \\ <Module Name> \\ timeout computer locale HKEY**</span><span class="sxs-lookup"><span data-stu-id="5452e-109">**HKEY\_LOCAL\_MACHINE\\<DebugRoot>\\<Module Name>\\TIMEOUT**</span></span>

<span data-ttu-id="5452e-110">dove *<DebugRoot>* è il percorso del registro di sistema descritto nell'argomento [funzioni di output di debug](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5452e-110">where *<DebugRoot>* is the registry path described in the topic [Debug Output Functions](debug-output-functions.md).</span></span>

<span data-ttu-id="5452e-111">Se la chiave non esiste, per impostazione predefinita il valore di timeout è infinito.</span><span class="sxs-lookup"><span data-stu-id="5452e-111">If the key does not exist, the time-out value defaults to INFINITE.</span></span> <span data-ttu-id="5452e-112">È possibile usare la funzione [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) per eseguire l'override della voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5452e-112">You can use the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function to override the registry entry.</span></span>



| <span data-ttu-id="5452e-113">Funzione</span><span class="sxs-lookup"><span data-stu-id="5452e-113">Function</span></span>                                                       | <span data-ttu-id="5452e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5452e-114">Description</span></span>                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="5452e-115">**DbgSetWaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="5452e-115">**DbgSetWaitTimeout**</span></span>](dbgsetwaittimeout.md)                 | <span data-ttu-id="5452e-116">Imposta il valore di timeout del debug.</span><span class="sxs-lookup"><span data-stu-id="5452e-116">Sets the debugging time-out value.</span></span>                              |
| [<span data-ttu-id="5452e-117">**DbgWaitForMultipleObjects**</span><span class="sxs-lookup"><span data-stu-id="5452e-117">**DbgWaitForMultipleObjects**</span></span>](dbgwaitformultipleobjects.md) | <span data-ttu-id="5452e-118">Attende la segnalazione di qualsiasi (o tutti) degli oggetti specificati.</span><span class="sxs-lookup"><span data-stu-id="5452e-118">Waits for any (or all) of the specified objects to be signaled.</span></span> |
| [<span data-ttu-id="5452e-119">**DbgWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="5452e-119">**DbgWaitForSingleObject**</span></span>](dbgwaitforsingleobject.md)       | <span data-ttu-id="5452e-120">Attende che un oggetto venga segnalato.</span><span class="sxs-lookup"><span data-stu-id="5452e-120">Waits for an object to become signaled.</span></span>                         |



 

 

 




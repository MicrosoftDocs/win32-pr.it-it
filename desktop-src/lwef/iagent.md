---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330020"
---
# <a name="iagent"></a><span data-ttu-id="4fb9b-103">IAgent</span><span class="sxs-lookup"><span data-stu-id="4fb9b-103">IAgent</span></span>

<span data-ttu-id="4fb9b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4fb9b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4fb9b-105">**IAgent** definisce un'interfaccia che consente alle applicazioni di caricare caratteri, ricevere eventi e controllare lo stato corrente del server Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-105">**IAgent** defines an interface that allows applications to load characters, receive events, and check the current state of the Microsoft Agent Server.</span></span> <span data-ttu-id="4fb9b-106">Queste funzioni sono disponibili anche da [**IAgentEx**](iagentex.md).</span><span class="sxs-lookup"><span data-stu-id="4fb9b-106">These functions are also available from [**IAgentEx**](iagentex.md).</span></span>

<span data-ttu-id="4fb9b-107">Il metodo getsuspended incluso nelle versioni precedenti è obsoleto e restituisce **false** per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-107">The GetSuspended method included in previous versions is obsolete and returns **False** for backward compatibility.</span></span>

<span data-ttu-id="4fb9b-108">**Metodi nell'ordine Vtable**</span><span class="sxs-lookup"><span data-stu-id="4fb9b-108">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="4fb9b-109">Metodi IAgent</span><span class="sxs-lookup"><span data-stu-id="4fb9b-109">IAgent Methods</span></span>                               | <span data-ttu-id="4fb9b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb9b-110">Description</span></span>                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="4fb9b-111">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="4fb9b-111">**Load**</span></span>](load-method.md)                  | <span data-ttu-id="4fb9b-112">Carica un file di dati del carattere.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-112">Loads a character's data file.</span></span>                                |
| [<span data-ttu-id="4fb9b-113">**Scaricare**</span><span class="sxs-lookup"><span data-stu-id="4fb9b-113">**Unload**</span></span>](unload-method.md)              | <span data-ttu-id="4fb9b-114">Scarica il file di dati di un carattere.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-114">Unloads a character's data file.</span></span>                              |
| [<span data-ttu-id="4fb9b-115">**Registrazione**</span><span class="sxs-lookup"><span data-stu-id="4fb9b-115">**Register**</span></span>](iagent--register.md)         | <span data-ttu-id="4fb9b-116">Registra un sink di notifica per il client.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-116">Registers a notification sink for the client.</span></span>                 |
| [<span data-ttu-id="4fb9b-117">**Unegister**</span><span class="sxs-lookup"><span data-stu-id="4fb9b-117">**Unegister**</span></span>](iagent--unregister.md)      | <span data-ttu-id="4fb9b-118">Annulla la registrazione di un sink di notifica del client.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-118">Unregisters a client's notification sink.</span></span>                     |
| [<span data-ttu-id="4fb9b-119">**Getcharacter**</span><span class="sxs-lookup"><span data-stu-id="4fb9b-119">**GetCharacter**</span></span>](iagent--getcharacter.md) | <span data-ttu-id="4fb9b-120">Restituisce l'interfaccia IAgentCharacter per un carattere caricato.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-120">Returns the IAgentCharacter interface for a loaded character.</span></span> |



 

 

 





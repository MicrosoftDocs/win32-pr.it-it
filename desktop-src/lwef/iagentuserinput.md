---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398945"
---
# <a name="iagentuserinput"></a><span data-ttu-id="cd01a-103">IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="cd01a-103">IAgentUserInput</span></span>

<span data-ttu-id="cd01a-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cd01a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="cd01a-105">Quando il server invia una notifica al client di input attivo con [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), restituisce informazioni tramite l'oggetto [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="cd01a-105">When the server notifies the input-active client with [**IAgentNotifySink::Command**](iagentnotifysink--command.md), it returns information through the [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="cd01a-106">**IAgentUserInput** definisce un'interfaccia che consente alle applicazioni di eseguire query su questi valori.</span><span class="sxs-lookup"><span data-stu-id="cd01a-106">**IAgentUserInput** defines an interface that allows applications to query these values.</span></span>

<span data-ttu-id="cd01a-107">**Metodi nell'ordine Vtable**</span><span class="sxs-lookup"><span data-stu-id="cd01a-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="cd01a-108">Metodi IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="cd01a-108">IAgentUserInput Methods</span></span>                                         | <span data-ttu-id="cd01a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd01a-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd01a-110">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="cd01a-110">**GetCount**</span></span>](iagentuserinput--getcount.md)                   | <span data-ttu-id="cd01a-111">Restituisce il numero di alternative del comando restituite in un evento di [**comando**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="cd01a-111">Returns the number of command alternatives returned in a [**Command**](command-event.md) event.</span></span>                                         |
| [<span data-ttu-id="cd01a-112">**GetItemID**</span><span class="sxs-lookup"><span data-stu-id="cd01a-112">**GetItemID**</span></span>](iagentuserinput--getitemid.md)                 | <span data-ttu-id="cd01a-113">Restituisce l'ID per un'alternativa del [**comando**](command-event.md) specifica.</span><span class="sxs-lookup"><span data-stu-id="cd01a-113">Returns the ID for a specific [**Command**](command-event.md) alternative.</span></span>                                                              |
| [<span data-ttu-id="cd01a-114">**GetItemConfidence**</span><span class="sxs-lookup"><span data-stu-id="cd01a-114">**GetItemConfidence**</span></span>](iagentuserinput--getitemconfidence.md) | <span data-ttu-id="cd01a-115">Restituisce il valore della proprietà [**confidenza**](confidence-property.md) per un'alternativa del [**comando**](command-event.md) specifica.</span><span class="sxs-lookup"><span data-stu-id="cd01a-115">Returns the value of the [**Confidence**](confidence-property.md) property for a specific [**Command**](command-event.md) alternative.</span></span> |
| [<span data-ttu-id="cd01a-116">**GetItemText**</span><span class="sxs-lookup"><span data-stu-id="cd01a-116">**GetItemText**</span></span>](iagentuserinput--getitemtext.md)             | <span data-ttu-id="cd01a-117">Restituisce il valore del testo [**vocale**](voice-property.md) per un'alternativa del [**comando**](command-event.md) specifica.</span><span class="sxs-lookup"><span data-stu-id="cd01a-117">Returns the value of [**Voice**](voice-property.md) text for a specific [**Command**](command-event.md) alternative.</span></span>                   |
| [<span data-ttu-id="cd01a-118">**GetAllItemData**</span><span class="sxs-lookup"><span data-stu-id="cd01a-118">**GetAllItemData**</span></span>](iagentuserinput--getallitemdata.md)       | <span data-ttu-id="cd01a-119">Restituisce i dati per tutte le alternative dei [**comandi**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="cd01a-119">Returns the data for all [**Command**](command-event.md) alternatives.</span></span>                                                                  |



 

 

 
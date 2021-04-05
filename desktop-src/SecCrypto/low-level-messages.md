---
description: Le funzioni di messaggio di basso livello codificano i dati per la trasmissione e la decodifica dei dati ricevuti. Anche le funzioni di messaggio di basso livello decrittografano e verificano le firme dei messaggi ricevuti.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Funzioni di messaggio di basso livello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752130"
---
# <a name="low-level-message-functions"></a><span data-ttu-id="e6957-104">Funzioni di messaggio di basso livello</span><span class="sxs-lookup"><span data-stu-id="e6957-104">Low-level Message Functions</span></span>

<span data-ttu-id="e6957-105">Le [*funzioni di messaggio di basso livello*](../secgloss/l-gly.md) codificano i dati per la trasmissione e la decodifica dei dati ricevuti.</span><span class="sxs-lookup"><span data-stu-id="e6957-105">The [*low-level message functions*](../secgloss/l-gly.md) encode data for transmission and decode data that has been received.</span></span> <span data-ttu-id="e6957-106">Anche le funzioni di messaggio di basso livello decrittografano e verificano le firme dei messaggi ricevuti.</span><span class="sxs-lookup"><span data-stu-id="e6957-106">Low-level message functions also decrypt and verify the signatures of received messages.</span></span>

<span data-ttu-id="e6957-107">Quando un messaggio viene aperto utilizzando una funzione di apertura dei messaggi di basso livello, rimane aperto e disponibile (mantiene il proprio [*stato*](../secgloss/s-gly.md)) finché non viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="e6957-107">When a message is opened using a low-level message open function, it remains open and available (maintains its [*state*](../secgloss/s-gly.md)) until it is closed.</span></span> <span data-ttu-id="e6957-108">In questo modo è possibile costruire un messaggio a fasi usando più chiamate alla funzione [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .</span><span class="sxs-lookup"><span data-stu-id="e6957-108">This allows a message to be constructed piecemeal using multiple calls to the [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) function.</span></span>

<span data-ttu-id="e6957-109">L'utilizzo di funzioni di messaggio di basso livello richiede più chiamate di funzione rispetto all'utilizzo di funzioni di messaggio semplificate (vedere [messaggi semplificati](simplified-messages.md)).</span><span class="sxs-lookup"><span data-stu-id="e6957-109">Using low-level message functions requires more function calls than using simplified message functions (see [Simplified Messages](simplified-messages.md)).</span></span> <span data-ttu-id="e6957-110">Se vengono usate le funzioni di messaggio semplificate, il lavoro viene eseguito all'interno delle funzioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="e6957-110">If the simplified message functions are used, more of the work is done inside the functions of the API.</span></span>

<span data-ttu-id="e6957-111">L'utilizzo di funzioni di messaggio di basso livello implica il lavoro aggiuntivo di effettuare chiamate ad altre funzioni di crittografia o certificati.</span><span class="sxs-lookup"><span data-stu-id="e6957-111">Using low-level message functions involves the additional work of making calls to other certificate or cryptographic functions.</span></span> <span data-ttu-id="e6957-112">Ad esempio, è possibile che i dati delle chiamate alle funzioni di certificato siano necessari per inizializzare le strutture utilizzate dalle funzioni di messaggio di basso livello.</span><span class="sxs-lookup"><span data-stu-id="e6957-112">For example, data from calls to certificate functions may be needed to initialize structures used by these low-level message functions.</span></span> <span data-ttu-id="e6957-113">Le funzioni di messaggio semplificate inizializzano molte di queste strutture internamente.</span><span class="sxs-lookup"><span data-stu-id="e6957-113">Simplified message functions initialize many of these structures internally.</span></span>

<span data-ttu-id="e6957-114">Nella tabella seguente sono elencate le sezioni con le descrizioni delle procedure e gli esempi di codice C dell'utilizzo delle funzioni di messaggio di basso livello.</span><span class="sxs-lookup"><span data-stu-id="e6957-114">The following table lists sections with procedure descriptions and C code examples of using the low-level message functions.</span></span>



| <span data-ttu-id="e6957-115">Sezione</span><span class="sxs-lookup"><span data-stu-id="e6957-115">Section</span></span>                                                                               | <span data-ttu-id="e6957-116">Contenuto</span><span class="sxs-lookup"><span data-stu-id="e6957-116">Contents</span></span>                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e6957-117">Funzioni di messaggio di basso livello</span><span class="sxs-lookup"><span data-stu-id="e6957-117">Low-level Message Functions</span></span>](cryptography-functions.md) | <span data-ttu-id="e6957-118">Elenca le funzioni di messaggio di basso livello.</span><span class="sxs-lookup"><span data-stu-id="e6957-118">Lists the low-level message functions.</span></span>             |
| [<span data-ttu-id="e6957-119">Firma dei dati</span><span class="sxs-lookup"><span data-stu-id="e6957-119">Signing Data</span></span>](signing-data.md)                                                      | <span data-ttu-id="e6957-120">Descrive le attività necessarie per la firma dei dati.</span><span class="sxs-lookup"><span data-stu-id="e6957-120">Details the tasks needed to sign data.</span></span>             |
| [<span data-ttu-id="e6957-121">Codifica dei dati in busta</span><span class="sxs-lookup"><span data-stu-id="e6957-121">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)                                | <span data-ttu-id="e6957-122">Descrive le attività necessarie per codificare i dati in busta.</span><span class="sxs-lookup"><span data-stu-id="e6957-122">Details the tasks needed to encode enveloped data.</span></span> |
| [<span data-ttu-id="e6957-123">Decodifica dei dati in busta</span><span class="sxs-lookup"><span data-stu-id="e6957-123">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)                                | <span data-ttu-id="e6957-124">Descrive le attività necessarie per decodificare i dati in busta.</span><span class="sxs-lookup"><span data-stu-id="e6957-124">Details the tasks needed to decode enveloped data.</span></span> |



 

 

 

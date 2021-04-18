---
description: Se non si riesce a trovare gli analizzatori di coerenza interni necessari tra le azioni personalizzate ICE elencate nella Guida di riferimento a ICE, sarà necessario preparare il proprio ghiaccio per convalidare il pacchetto.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Creazione di un ghiaccio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311007"
---
# <a name="building-an-ice"></a><span data-ttu-id="52d12-103">Creazione di un ghiaccio</span><span class="sxs-lookup"><span data-stu-id="52d12-103">Building An ICE</span></span>

<span data-ttu-id="52d12-104">Se non si riesce a trovare gli [analizzatori di coerenza interni](internal-consistency-evaluators-ices.md) necessari tra le azioni personalizzate Ice elencate nella Guida di [riferimento a Ice](ice-reference.md), sarà necessario preparare il proprio ghiaccio per convalidare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="52d12-104">If you are unable to find the [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) you need among the existing ICE custom actions listed in the [ICE Reference](ice-reference.md), you will need to prepare your own ICE to validate your package.</span></span>

<span data-ttu-id="52d12-105">Quando si creano azioni personalizzate ICE, è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="52d12-105">When authoring ICE custom actions you should do the following:</span></span>

-   <span data-ttu-id="52d12-106">Basare i ghiacci solo sulle azioni personalizzate dei tipi elencati nella tabella illustrata.</span><span class="sxs-lookup"><span data-stu-id="52d12-106">Base the ICEs only on custom actions of types listed in the table shown.</span></span>
-   <span data-ttu-id="52d12-107">Chiamare [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e pubblicare un \_ tipo di messaggio utente INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="52d12-107">Call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and post an INSTALLMESSAGE\_USER type of message.</span></span> <span data-ttu-id="52d12-108">Quando si creano i messaggi ICE, seguire il formato dei messaggi nelle [linee guida](ice-message-guidelines.md)per i messaggi di ghiaccio.</span><span class="sxs-lookup"><span data-stu-id="52d12-108">When authoring your ICE messages follow the message format in the [ICE Message Guidelines](ice-message-guidelines.md).</span></span>
-   <span data-ttu-id="52d12-109">Scrivere il ghiaccio in modo che acquisisca eventuali errori dell'API e restituisca sempre l'errore \_ Success.</span><span class="sxs-lookup"><span data-stu-id="52d12-109">Write your ICE such that it captures any API errors and always returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="52d12-110">Questa operazione è necessaria per consentire l'esecuzione di azioni personalizzate successive in seguito all'errore di un ghiaccio.</span><span class="sxs-lookup"><span data-stu-id="52d12-110">This is necessary to allow subsequent custom actions to run following the failure of an ICE.</span></span>

<span data-ttu-id="52d12-111">Le azioni personalizzate ICE sono limitate ai tipi di azione personalizzati seguenti.</span><span class="sxs-lookup"><span data-stu-id="52d12-111">ICE custom actions are limited to the following custom action types.</span></span>



| <span data-ttu-id="52d12-112">Tipo di azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="52d12-112">Custom action type</span></span>                                 | <span data-ttu-id="52d12-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52d12-113">Description</span></span>               |
|----------------------------------------------------|---------------------------|
| [<span data-ttu-id="52d12-114">Tipo di azione personalizzata 1</span><span class="sxs-lookup"><span data-stu-id="52d12-114">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="52d12-115">DLL nel flusso binario</span><span class="sxs-lookup"><span data-stu-id="52d12-115">DLL in binary stream</span></span>      |
| [<span data-ttu-id="52d12-116">Tipo di azione personalizzata 2</span><span class="sxs-lookup"><span data-stu-id="52d12-116">Custom Action Type 2</span></span>](custom-action-type-2.md)   | <span data-ttu-id="52d12-117">EXE nel flusso binario</span><span class="sxs-lookup"><span data-stu-id="52d12-117">EXE in binary stream</span></span>      |
| [<span data-ttu-id="52d12-118">Tipo di azione personalizzata 5</span><span class="sxs-lookup"><span data-stu-id="52d12-118">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="52d12-119">JScript nel flusso binario</span><span class="sxs-lookup"><span data-stu-id="52d12-119">JScript in binary stream</span></span>  |
| [<span data-ttu-id="52d12-120">Tipo di azione personalizzata 6</span><span class="sxs-lookup"><span data-stu-id="52d12-120">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="52d12-121">VBScript nel flusso binario</span><span class="sxs-lookup"><span data-stu-id="52d12-121">VBScript in binary stream</span></span> |
| [<span data-ttu-id="52d12-122">Tipo di azione personalizzata 37</span><span class="sxs-lookup"><span data-stu-id="52d12-122">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="52d12-123">Codice JScript come stringa</span><span class="sxs-lookup"><span data-stu-id="52d12-123">JScript code as string</span></span>    |
| [<span data-ttu-id="52d12-124">Tipo di azione personalizzata 38</span><span class="sxs-lookup"><span data-stu-id="52d12-124">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="52d12-125">Codice VBScript come stringa</span><span class="sxs-lookup"><span data-stu-id="52d12-125">VBScript code as string</span></span>   |



 

<span data-ttu-id="52d12-126">Quando si crea un'azione personalizzata ICE, non eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="52d12-126">When authoring an ICE custom action, do not do the following:</span></span>

-   <span data-ttu-id="52d12-127">Non presupporre che l'handle del motore ricevuto dal ghiaccio sia un'istanza di installazione del database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="52d12-127">Do not assume that the handle to the engine that the ICE receives is an installation instance of the installer database.</span></span> <span data-ttu-id="52d12-128">Se non si tratta di un'istanza di installazione, alcune proprietà non sono definite, le directory di origine e di destinazione non vengono risolte e gli Stati della funzionalità corrente non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="52d12-128">If it is not a installation instance, certain properties are not defined, the source and target directories are not resolved, and current feature states are not defined.</span></span>
-   <span data-ttu-id="52d12-129">Non fare affidamento sull'esecuzione precedente, o non sull'esecuzione, di qualsiasi azione del programma di installazione, azione personalizzata o un altro ghiaccio.</span><span class="sxs-lookup"><span data-stu-id="52d12-129">Do not rely on the prior execution, or non-execution, of any installer action, custom action, or another ICE.</span></span> <span data-ttu-id="52d12-130">Poiché un ghiaccio precedente potrebbe avere creato colonne temporanee in qualsiasi tabella, gli autori devono fare riferimento alle colonne in base al nome laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="52d12-130">Because a prior ICE may have created temporary columns in any table, authors should reference columns by name whenever possible.</span></span> <span data-ttu-id="52d12-131">I ghiacci devono eseguire la pulizia di eventuali colonne o tabelle temporanee prima di uscire.</span><span class="sxs-lookup"><span data-stu-id="52d12-131">ICEs should cleanup any temporary columns or tables before they exit.</span></span>
-   <span data-ttu-id="52d12-132">Non presupporre che gli autori abbiano accesso a un'immagine della directory di origine del database.</span><span class="sxs-lookup"><span data-stu-id="52d12-132">Do not assume that authors have access to an image of the source directory of the database.</span></span>
-   <span data-ttu-id="52d12-133">Non presupporre che le modifiche apportate al database non vengano mantenute.</span><span class="sxs-lookup"><span data-stu-id="52d12-133">Do not assume that changes made to the database do not persist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52d12-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52d12-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52d12-135">Esempio di ghiaccio in C++</span><span class="sxs-lookup"><span data-stu-id="52d12-135">Sample ICE in C++</span></span>](sample-ice-in-c-.md)
</dt> <dt>

[<span data-ttu-id="52d12-136">Esempio di ghiaccio in VBScript</span><span class="sxs-lookup"><span data-stu-id="52d12-136">Sample ICE in VBScript</span></span>](sample-ice-in-vbscript.md)
</dt> </dl>

 

 




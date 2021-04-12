---
title: Modifica di flussi
description: Modifica di flussi
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- CreateEditableStream (funzione)
- EditStreamCut (funzione)
- EditStreamCopy (funzione)
- EditStreamPaste (funzione)
- EditStreamClone (funzione)
- EditStreamSetInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471462"
---
# <a name="editing-streams"></a><span data-ttu-id="6f0b0-109">Modifica di flussi</span><span class="sxs-lookup"><span data-stu-id="6f0b0-109">Editing Streams</span></span>

<span data-ttu-id="6f0b0-110">È possibile creare un flusso che è possibile modificare usando la funzione [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) .</span><span class="sxs-lookup"><span data-stu-id="6f0b0-110">You can create a stream that you can edit by using the [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) function.</span></span> <span data-ttu-id="6f0b0-111">Questa funzione Inizializza l'ambiente per la modifica di un flusso.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-111">This function initializes the environment for editing a stream.</span></span> <span data-ttu-id="6f0b0-112">Ciò include la creazione di un'interfaccia per il nuovo flusso e le tabelle di modifica interne che rilevano le modifiche apportate al flusso.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-112">This includes creating an interface to the new stream, and internal edit tables that track changes made to the stream.</span></span> <span data-ttu-id="6f0b0-113">**CreateEditableStream** restituisce un puntatore di flusso a un flusso modificabile richiesto da altre funzioni di modifica del flusso.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-113">**CreateEditableStream** returns a stream pointer to an editable stream that is required by other stream-editing functions.</span></span> <span data-ttu-id="6f0b0-114">Il puntatore di flusso modificabile può essere usato anche da altre funzioni AVIFile che accettano i puntatori di flusso.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-114">The editable stream pointer can also be used by other AVIFile functions that accept stream pointers.</span></span>

<span data-ttu-id="6f0b0-115">È possibile tagliare uno o più esempi da un flusso modificabile usando la funzione [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) .</span><span class="sxs-lookup"><span data-stu-id="6f0b0-115">You can cut one or more samples from an editable stream by using the [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) function.</span></span> <span data-ttu-id="6f0b0-116">Per rimuovere gli esempi dal flusso modificabile, questa funzione aggiunge una voce alla tabella di modifica.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-116">To remove samples from the editable stream, this function adds an entry to the edit table.</span></span> <span data-ttu-id="6f0b0-117">La funzione quindi inserisce una copia degli esempi tagliati in un nuovo flusso temporaneo il cui puntatore di interfaccia viene restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-117">The function then places a copy of the cut samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="6f0b0-118">È possibile copiare uno o più esempi da un flusso modificabile in un flusso temporaneo usando la funzione [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) .</span><span class="sxs-lookup"><span data-stu-id="6f0b0-118">You can copy one or more samples from an editable stream into a temporary stream by using the [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) function.</span></span> <span data-ttu-id="6f0b0-119">**EditStreamCopy** inserisce copie degli esempi in un nuovo flusso temporaneo il cui puntatore di interfaccia viene restituito in una variabile.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-119">**EditStreamCopy** places copies of the samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="6f0b0-120">È possibile copiare uno o più esempi da un flusso e incollarli in un flusso modificabile usando la funzione [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) .</span><span class="sxs-lookup"><span data-stu-id="6f0b0-120">You can copy one or more samples from a stream and paste them into an editable stream by using the [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) function.</span></span> <span data-ttu-id="6f0b0-121">Per inserire gli esempi in corrispondenza della posizione specificata, questa funzione aggiunge una voce nella tabella di modifica del flusso modificabile di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-121">To insert the samples at the specified position, this function adds an entry in the edit table of the target editable stream.</span></span>

<span data-ttu-id="6f0b0-122">È possibile duplicare un flusso modificabile usando la funzione [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) .</span><span class="sxs-lookup"><span data-stu-id="6f0b0-122">You can duplicate an editable stream by using the [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) function.</span></span> <span data-ttu-id="6f0b0-123">Questa funzione restituisce un puntatore all'interfaccia del flusso del nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-123">This function returns a pointer to the stream interface of the new stream.</span></span> <span data-ttu-id="6f0b0-124">È possibile copiare questi flussi negli Appunti o usarli per mantenere una traccia delle modifiche apportate a un flusso.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-124">You can copy these streams to the clipboard or use them to maintain a trail of edits made to a stream.</span></span>

<span data-ttu-id="6f0b0-125">È possibile modificare molte delle caratteristiche di un flusso modificabile usando la funzione [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) .</span><span class="sxs-lookup"><span data-stu-id="6f0b0-125">You can change several of the characteristics of an editable stream by using the [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) function.</span></span> <span data-ttu-id="6f0b0-126">Questa funzione aggiorna l'impostazione di priorità, la lingua, la scala e la velocità, l'ora di inizio, l'impostazione della qualità, le dimensioni e le coordinate del rettangolo di destinazione e la descrizione testuale del flusso.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-126">This function updates the priority setting, language, scale and rate, starting time, quality setting, destination rectangle dimensions and coordinates, and the textual description of the stream.</span></span> <span data-ttu-id="6f0b0-127">Questi elementi vengono archiviati nella struttura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) associata al flusso modificabile.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-127">These items are stored in the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure associated with the editable stream.</span></span>

<span data-ttu-id="6f0b0-128">È anche possibile modificare la descrizione testuale di un flusso modificabile usando la funzione [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) .</span><span class="sxs-lookup"><span data-stu-id="6f0b0-128">You can also change the textual description of an editable stream by using the [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) function.</span></span> <span data-ttu-id="6f0b0-129">Questa funzione aggiorna il membro **szName** della struttura **AVISTREAMINFO** associata al flusso modificabile.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-129">This function updates the **szName** member of the **AVISTREAMINFO** structure associated with the editable stream.</span></span>

<span data-ttu-id="6f0b0-130">Le funzioni di modifica funzionano sui flussi.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-130">The editing functions work on streams.</span></span> <span data-ttu-id="6f0b0-131">È necessario tagliare e incollare ogni flusso singolarmente, quindi utilizzare la funzione [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) per creare un nuovo puntatore di file.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-131">You need to cut and paste each stream individually, and then use the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function to create a new file pointer.</span></span>

> [!Note]  
> <span data-ttu-id="6f0b0-132">Le tabelle di modifica in un flusso modificabile mantengono tutte le modifiche per un flusso.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-132">The edit tables in an editable stream maintain all the changes for a stream.</span></span> <span data-ttu-id="6f0b0-133">Il flusso di origine non viene mai modificato.</span><span class="sxs-lookup"><span data-stu-id="6f0b0-133">The source stream is never changed.</span></span>

 

 

 





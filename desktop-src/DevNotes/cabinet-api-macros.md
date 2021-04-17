---
description: 'Altre informazioni su: macro API cabinet'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macro API cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522866"
---
# <a name="cabinet-api-macros"></a><span data-ttu-id="e5343-103">Macro API cabinet</span><span class="sxs-lookup"><span data-stu-id="e5343-103">Cabinet API Macros</span></span>

<span data-ttu-id="e5343-104">Questa sezione illustra in dettaglio le macro usate dall'API CAB:</span><span class="sxs-lookup"><span data-stu-id="e5343-104">This section details the macros used by the Cabinet API:</span></span>

## <a name="fci-macros"></a><span data-ttu-id="e5343-105">Macro FCI</span><span class="sxs-lookup"><span data-stu-id="e5343-105">FCI Macros</span></span>

<span data-ttu-id="e5343-106">Le macro seguenti vengono usate dall'istanza FCI:</span><span class="sxs-lookup"><span data-stu-id="e5343-106">The following macros are used by FCI:</span></span>



| <span data-ttu-id="e5343-107">Macro</span><span class="sxs-lookup"><span data-stu-id="e5343-107">Macro</span></span>                                              | <span data-ttu-id="e5343-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5343-108">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5343-109">**FNFCIALLOC**</span><span class="sxs-lookup"><span data-stu-id="e5343-109">**FNFCIALLOC**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | <span data-ttu-id="e5343-110">Usato per allocare memoria in un contesto dell'istanza del cluster di failover.</span><span class="sxs-lookup"><span data-stu-id="e5343-110">Used to allocate memory in an FCI context.</span></span><br/>                                          |
| [<span data-ttu-id="e5343-111">**FNFCICLOSE**</span><span class="sxs-lookup"><span data-stu-id="e5343-111">**FNFCICLOSE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | <span data-ttu-id="e5343-112">Utilizzato per chiudere un file.</span><span class="sxs-lookup"><span data-stu-id="e5343-112">Used to close a file.</span></span><br/>                                                               |
| [<span data-ttu-id="e5343-113">**FNFCIDELETE**</span><span class="sxs-lookup"><span data-stu-id="e5343-113">**FNFCIDELETE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | <span data-ttu-id="e5343-114">Utilizzato per eliminare un file.</span><span class="sxs-lookup"><span data-stu-id="e5343-114">Used to delete a file.</span></span><br/>                                                              |
| [<span data-ttu-id="e5343-115">**FNFCIFILEPLACED**</span><span class="sxs-lookup"><span data-stu-id="e5343-115">**FNFCIFILEPLACED**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | <span data-ttu-id="e5343-116">Utilizzato per notificare quando un file viene inserito nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="e5343-116">Used to notify when a file is placed in the cabinet.</span></span><br/>                                |
| [<span data-ttu-id="e5343-117">**FNFCIFREE**</span><span class="sxs-lookup"><span data-stu-id="e5343-117">**FNFCIFREE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | <span data-ttu-id="e5343-118">Utilizzato per liberare la memoria allocata in precedenza in un contesto dell'istanza FCI.</span><span class="sxs-lookup"><span data-stu-id="e5343-118">Used to free previously allocated memory in an FCI context.</span></span><br/>                         |
| [<span data-ttu-id="e5343-119">**FNFCIGETNEXTCABINET**</span><span class="sxs-lookup"><span data-stu-id="e5343-119">**FNFCIGETNEXTCABINET**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | <span data-ttu-id="e5343-120">Utilizzato per richiedere informazioni per il file CAB successivo.</span><span class="sxs-lookup"><span data-stu-id="e5343-120">Used to request information for the next cabinet.</span></span><br/>                                   |
| [<span data-ttu-id="e5343-121">**FNFCIGETOPENINFO**</span><span class="sxs-lookup"><span data-stu-id="e5343-121">**FNFCIGETOPENINFO**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | <span data-ttu-id="e5343-122">Utilizzato per aprire un file e recuperare la data, l'ora e gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="e5343-122">Used to open a file and retrieve file date, time, and attributes.</span></span><br/>                   |
| [<span data-ttu-id="e5343-123">**FNFCIGETTEMPFILE**</span><span class="sxs-lookup"><span data-stu-id="e5343-123">**FNFCIGETTEMPFILE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | <span data-ttu-id="e5343-124">Utilizzato per ottenere un nome di file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="e5343-124">Used to obtain a temporary file name.</span></span><br/>                                               |
| [<span data-ttu-id="e5343-125">**FNFCIOPEN**</span><span class="sxs-lookup"><span data-stu-id="e5343-125">**FNFCIOPEN**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | <span data-ttu-id="e5343-126">Utilizzato per aprire un file in un contesto dell'istanza del cluster di failover.</span><span class="sxs-lookup"><span data-stu-id="e5343-126">Used to open a file in an FCI context.</span></span><br/>                                              |
| [<span data-ttu-id="e5343-127">**FNFCIREAD**</span><span class="sxs-lookup"><span data-stu-id="e5343-127">**FNFCIREAD**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciread)                     | <span data-ttu-id="e5343-128">Utilizzato per leggere i dati da un file.</span><span class="sxs-lookup"><span data-stu-id="e5343-128">Used to read data from a file.</span></span><br/>                                                      |
| [<span data-ttu-id="e5343-129">**FNFCISEEK**</span><span class="sxs-lookup"><span data-stu-id="e5343-129">**FNFCISEEK**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | <span data-ttu-id="e5343-130">Utilizzato per spostare un puntatore di file in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="e5343-130">Used to move a file pointer to a specified location.</span></span><br/>                                |
| [<span data-ttu-id="e5343-131">**FNFCISTATUS**</span><span class="sxs-lookup"><span data-stu-id="e5343-131">**FNFCISTATUS**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | <span data-ttu-id="e5343-132">Utilizzato per aggiornare l'utente.</span><span class="sxs-lookup"><span data-stu-id="e5343-132">Used to update the user.</span></span><br/>                                                            |
| [<span data-ttu-id="e5343-133">**FNFCIWRITE**</span><span class="sxs-lookup"><span data-stu-id="e5343-133">**FNFCIWRITE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | <span data-ttu-id="e5343-134">Utilizzato per scrivere i dati in un file.</span><span class="sxs-lookup"><span data-stu-id="e5343-134">Used to write data to a file.</span></span><br/>                                                       |
| [<span data-ttu-id="e5343-135">**TCOMPfromLZXWindow**</span><span class="sxs-lookup"><span data-stu-id="e5343-135">**TCOMPfromLZXWindow**</span></span>](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | <span data-ttu-id="e5343-136">Converte le dimensioni di Windows in un valore LXZ TCOMP per [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span><span class="sxs-lookup"><span data-stu-id="e5343-136">Converts windows size into an LXZ TCOMP value for [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span></span><br/> |



 

## <a name="fdi-macros"></a><span data-ttu-id="e5343-137">Macro IDE</span><span class="sxs-lookup"><span data-stu-id="e5343-137">FDI Macros</span></span>

<span data-ttu-id="e5343-138">Le macro seguenti vengono usate da IDE:</span><span class="sxs-lookup"><span data-stu-id="e5343-138">The following macros are used by FDI:</span></span>



| <span data-ttu-id="e5343-139">Macro</span><span class="sxs-lookup"><span data-stu-id="e5343-139">Macro</span></span>                              | <span data-ttu-id="e5343-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5343-140">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5343-141">**FNALLOC**</span><span class="sxs-lookup"><span data-stu-id="e5343-141">**FNALLOC**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | <span data-ttu-id="e5343-142">Usato per allocare memoria in un contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="e5343-142">Used to allocate memory in an FDI context.</span></span><br/>                               |
| [<span data-ttu-id="e5343-143">**FNCLOSE**</span><span class="sxs-lookup"><span data-stu-id="e5343-143">**FNCLOSE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnclose)         | <span data-ttu-id="e5343-144">Usato per chiudere un file in un contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="e5343-144">Used to close a file in an FDI context.</span></span><br/>                                  |
| [<span data-ttu-id="e5343-145">**FNFDINOTIFY**</span><span class="sxs-lookup"><span data-stu-id="e5343-145">**FNFDINOTIFY**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | <span data-ttu-id="e5343-146">Utilizzato per aggiornare l'applicazione sullo stato del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="e5343-146">Used to update the application on the status of the decoder.</span></span><br/>             |
| [<span data-ttu-id="e5343-147">**FNFREE**</span><span class="sxs-lookup"><span data-stu-id="e5343-147">**FNFREE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfree)           | <span data-ttu-id="e5343-148">Usato per liberare la memoria allocata in precedenza in un contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="e5343-148">Used to free previously allocated memory in an FDI context.</span></span><br/>              |
| [<span data-ttu-id="e5343-149">**FNOPEN**</span><span class="sxs-lookup"><span data-stu-id="e5343-149">**FNOPEN**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnopen)           | <span data-ttu-id="e5343-150">Utilizzato per aprire un file in un contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="e5343-150">Used to open a file in an FDI context.</span></span><br/>                                   |
| [<span data-ttu-id="e5343-151">**FNREAD**</span><span class="sxs-lookup"><span data-stu-id="e5343-151">**FNREAD**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnread)           | <span data-ttu-id="e5343-152">Usato per leggere i dati da un file in un contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="e5343-152">Used to read data from a file in an FDI context.</span></span><br/>                         |
| [<span data-ttu-id="e5343-153">**FNSEEK**</span><span class="sxs-lookup"><span data-stu-id="e5343-153">**FNSEEK**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnseek)           | <span data-ttu-id="e5343-154">Usato per spostare un puntatore di file nella posizione specificata in un contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="e5343-154">Used to move a file pointer to the specified location in an FDI context.</span></span><br/> |
| [<span data-ttu-id="e5343-155">**FNWRITE**</span><span class="sxs-lookup"><span data-stu-id="e5343-155">**FNWRITE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | <span data-ttu-id="e5343-156">Usato per scrivere i dati in un file in un contesto IDE.</span><span class="sxs-lookup"><span data-stu-id="e5343-156">Used to write data to a file in an FDI context.</span></span><br/>                          |



 

## <a name="related-topics"></a><span data-ttu-id="e5343-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5343-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5343-158">Informazioni di riferimento sull'API cabinet</span><span class="sxs-lookup"><span data-stu-id="e5343-158">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="e5343-159">Uso dell'API cabinet</span><span class="sxs-lookup"><span data-stu-id="e5343-159">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 





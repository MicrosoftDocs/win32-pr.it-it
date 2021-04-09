---
title: Nuova funzionalità Cronologia file
description: Nuova funzionalità Cronologia file
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104118579"
---
# <a name="new-file-history-feature"></a><span data-ttu-id="9d1ba-103">Nuova funzionalità Cronologia file</span><span class="sxs-lookup"><span data-stu-id="9d1ba-103">New File History feature</span></span>

## <a name="platform"></a><span data-ttu-id="9d1ba-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="9d1ba-104">Platform</span></span>

<span data-ttu-id="9d1ba-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="9d1ba-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="9d1ba-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d1ba-106">Description</span></span>

<span data-ttu-id="9d1ba-107">La nuova funzionalità Cronologia file sostituisce la funzione di backup e ripristino esistente e offre protezione per i file utente archiviati nelle librerie utente.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-107">The new File History feature replaces the existing Backup and Restore function, and offers protection for user files stored in user libraries.</span></span> <span data-ttu-id="9d1ba-108">Viene fornito un set di API che consente agli sviluppatori di abilitare a livello di codice la cronologia dei file e selezionare una destinazione di archiviazione specifica.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-108">A set of APIs is provided that allows developers to programmatically enable File History and select a specific storage target.</span></span> <span data-ttu-id="9d1ba-109">La documentazione per queste API è disponibile in MSDN.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-109">Documentation for these APIs is available on MSDN.</span></span>

<span data-ttu-id="9d1ba-110">Potrebbe influire sui flussi di lavoro correlati alla protezione dei dati e alla documentazione che dipendono dalla funzionalità di backup e ripristino di Windows.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-110">It may affect workflows related to data protection and documentation that depend on the Windows Backup and Restore feature.</span></span>

<span data-ttu-id="9d1ba-111">Non è consigliabile usare entrambe le funzionalità nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-111">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="9d1ba-112">Cronologia file controlla se esiste una pianificazione di backup ed è attiva e se ne trova una, non consente agli utenti di attivarla.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-112">File History checks if a Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="9d1ba-113">In questo caso, gli utenti che desiderano utilizzare la cronologia file dovranno eliminare la pianificazione di backup di Windows.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-113">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9d1ba-114">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="9d1ba-114">Manifestation</span></span>

<span data-ttu-id="9d1ba-115">I flussi di lavoro possono essere interrotti e la documentazione relativa al metodo precedente per accedere alla funzionalità di backup e ripristino di Windows deve essere aggiornata per riflettere queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-115">Workflows may be interrupted and documentation for the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="solution"></a><span data-ttu-id="9d1ba-116">Soluzione</span><span class="sxs-lookup"><span data-stu-id="9d1ba-116">Solution</span></span>

<span data-ttu-id="9d1ba-117">Rivedere le app che contengono flussi di lavoro che incidono negativamente sulla nuova funzionalità di cronologia file per rimuovere eventuali conflitti e incorporare il nuovo set di API.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-117">Revise apps that contain workflows that are adversely impacted by the new File History feature to remove any conflicts and incorporate the new set of APIs.</span></span>

## <a name="tests"></a><span data-ttu-id="9d1ba-118">Test</span><span class="sxs-lookup"><span data-stu-id="9d1ba-118">Tests</span></span>

<span data-ttu-id="9d1ba-119">L'API consente agli sviluppatori di determinare se è attivata la cronologia file.</span><span class="sxs-lookup"><span data-stu-id="9d1ba-119">The API allows developers to determine if File History is turned on.</span></span>

 

 





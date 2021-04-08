---
title: Archivio comune SIS e file di Common-Store
description: Tutti i file di backup gestiti dal backup dell'archivio a istanza singola (SIS) sono denominati file di archivio comuni.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Backup di archivi comuni
- Backup dell'archivio a istanza singola (SIS), archivi comuni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872765"
---
# <a name="the-sis-common-store-and-common-store-files"></a><span data-ttu-id="a806f-105">Archivio comune SIS e file di Common-Store</span><span class="sxs-lookup"><span data-stu-id="a806f-105">The SIS Common Store and Common-Store Files</span></span>

<span data-ttu-id="a806f-106">Tutti i file di backup gestiti dal backup dell'archivio a istanza singola (SIS) sono denominati *file di archivio comuni*.</span><span class="sxs-lookup"><span data-stu-id="a806f-106">All backing files maintained by single-instance store (SIS) backup are called *common-store files*.</span></span> <span data-ttu-id="a806f-107">Un *archivio comune* è presente in ogni volume gestito da SIS e contiene tutti i file di archivio comuni presenti in tale volume.</span><span class="sxs-lookup"><span data-stu-id="a806f-107">One *common store* exists on each SIS-maintained volume and contains all of the common-store files that exist on that volume.</span></span> <span data-ttu-id="a806f-108">Questa directory si trova nella directory radice del volume ed è denominata " \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="a806f-108">This directory is located in the root directory of the volume and is named "\\SIS Common Store".</span></span> <span data-ttu-id="a806f-109">L'archivio comune viene implementato come una directory protetta da un accesso utente normale, perché i file di archivio comuni sono destinati all'accesso diretto solo alle funzioni API di backup SIS e non alle applicazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="a806f-109">The common store is implemented as a directory that is protected against normal user access, because common-store files are intended to be accessed directly only by SIS backup API functions and not backup and restore applications.</span></span>

<span data-ttu-id="a806f-110">Di seguito sono riportate le proprietà di un file di archivio comune:</span><span class="sxs-lookup"><span data-stu-id="a806f-110">The properties of a common-store file are the following:</span></span>

-   <span data-ttu-id="a806f-111">Un file di archivio comune può includere uno o più collegamenti che vi fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="a806f-111">A common-store file may have one or more links pointing to it.</span></span>
-   <span data-ttu-id="a806f-112">Una volta creato, il contenuto di un file di archivio comune non cambia mai.</span><span class="sxs-lookup"><span data-stu-id="a806f-112">After it is created, the contents of a common-store file never change.</span></span>
-   <span data-ttu-id="a806f-113">I nomi dei file di archivio comuni sono univoci a livello globale, ovvero sono univoci in tutti i volumi in tutti i sistemi del mondo e il binding tra un nome di file di archivio comune e i relativi dati è statico a livello globale.</span><span class="sxs-lookup"><span data-stu-id="a806f-113">The names of common-store files are globally unique—that is, they are unique across all volumes across all systems in the world, and the binding between a common-store file name and its data is globally static.</span></span>

<span data-ttu-id="a806f-114">Quando SIS è abilitato in un volume, una copia dei file duplicati viene quindi creata nell'archivio comune e tutti i file duplicati vengono sostituiti con i [collegamenti SIS](sis-links-and-reparse-points.md) che puntano al file di archivio comune.</span><span class="sxs-lookup"><span data-stu-id="a806f-114">When SIS is enabled on a volume, one copy of the duplicate files is then created to the common store, and all of the duplicate files are replaced with [SIS links](sis-links-and-reparse-points.md) pointing to the common-store file.</span></span> <span data-ttu-id="a806f-115">Per ulteriori informazioni, vedere [Abilitazione o disabilitazione di SIS in un volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) nella documentazione di TechNet.</span><span class="sxs-lookup"><span data-stu-id="a806f-115">For more information, see [Enabling or Disabling SIS on a Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in the TechNet documentation.</span></span>

<span data-ttu-id="a806f-116">Quando si accede a uno dei collegamenti SIS per un'operazione di scrittura, il filtro SIS innanzitutto ripristina il contenuto originale del file di collegamento SIS dal file di archivio comune, il reparse point che collega il file di collegamento SIS all'archivio comune viene rimosso, quindi l'operazione di scrittura viene eseguita sul file di destinazione originale.</span><span class="sxs-lookup"><span data-stu-id="a806f-116">When one of the SIS links is accessed for a write operation, the SIS filter first restores the original contents of the SIS link file from the common-store file, the reparse point linking the SIS link file to the common store is removed, and then the write operation is performed on the original destination file.</span></span>

<span data-ttu-id="a806f-117">Il file di archivio comune viene rimosso solo quando l'ultimo collegamento SIS che punta a esso viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="a806f-117">The common-store file is removed only when the last SIS link pointing to it is deleted.</span></span>

 

 
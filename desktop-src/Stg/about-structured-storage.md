---
title: Informazioni sull'archiviazione strutturata
description: I file System tradizionali incontrano problemi quando tentano di archiviare in modo efficiente più tipi di oggetti in un unico documento.
ms.assetid: a571f7c2-0490-463c-813e-de4a9fd12a2d
keywords:
- Informazioni sull'archiviazione strutturata
- Archiviazione strutturata Strctd STG, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d048907c196c871af943e5a15cc95b367724a31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709079"
---
# <a name="about-structured-storage"></a><span data-ttu-id="8a58d-105">Informazioni sull'archiviazione strutturata</span><span class="sxs-lookup"><span data-stu-id="8a58d-105">About Structured Storage</span></span>

<span data-ttu-id="8a58d-106">I file System tradizionali incontrano problemi quando tentano di archiviare in modo efficiente più tipi di oggetti in un unico documento.</span><span class="sxs-lookup"><span data-stu-id="8a58d-106">Traditional file systems encounter challenges when they attempt to store efficiently multiple kinds of objects in one document.</span></span> <span data-ttu-id="8a58d-107">COM fornisce una soluzione: un file system all'interno di un file.</span><span class="sxs-lookup"><span data-stu-id="8a58d-107">COM provides a solution: a file system within a file.</span></span> <span data-ttu-id="8a58d-108">L'archiviazione strutturata COM definisce come trattare una singola entità file come una raccolta strutturata di due tipi di oggetti, ovvero archivi e flussi, che eseguono le directory e i file come.</span><span class="sxs-lookup"><span data-stu-id="8a58d-108">COM structured storage defines how to treat a single file entity as a structured collection of two types of objects—storages and streams—that perform like directories and files.</span></span> <span data-ttu-id="8a58d-109">Questo schema è denominato *archiviazione strutturata*.</span><span class="sxs-lookup"><span data-stu-id="8a58d-109">This scheme is called *structured storage*.</span></span> <span data-ttu-id="8a58d-110">Lo scopo dell'archiviazione strutturata consiste nel ridurre le sanzioni e il sovraccarico delle prestazioni associati all'archiviazione di oggetti distinti in un file flat.</span><span class="sxs-lookup"><span data-stu-id="8a58d-110">The purpose of structured storage is to reduce the performance penalties and overhead associated with storing separate objects in a flat file.</span></span>

<span data-ttu-id="8a58d-111">Questa sezione contiene una panoramica dei vantaggi e delle nozioni fondamentali dell'archiviazione strutturata, dei set di proprietà e dell'archiviazione strutturata asincrona, oltre a un aspetto cronologico dei file System:</span><span class="sxs-lookup"><span data-stu-id="8a58d-111">This section contains an overview of structured storage benefits and fundamentals, property sets and asynchronous structured storage as well as a historical look at file systems:</span></span>

-   <span data-ttu-id="8a58d-112">Implementazione del file composto</span><span class="sxs-lookup"><span data-stu-id="8a58d-112">Compound file implementation</span></span>
-   <span data-ttu-id="8a58d-113">Implementazione di file system NTFS</span><span class="sxs-lookup"><span data-stu-id="8a58d-113">NTFS file system implementation</span></span>
-   <span data-ttu-id="8a58d-114">Implementazione autonoma</span><span class="sxs-lookup"><span data-stu-id="8a58d-114">Stand-alone implementation</span></span>

<span data-ttu-id="8a58d-115">Questa sezione include collegamenti all' [evoluzione di file System](the-evolution-of-file-systems.md), [archiviazione e flussi](storages-and-streams.md), [file composti](compound-files.md), [nozioni di base sull'archiviazione strutturata](structured-storage-fundamentals.md)e [esempi di archiviazione strutturata](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="8a58d-115">This section includes links to [The Evolution of File Systems](the-evolution-of-file-systems.md), [Storages and Streams](storages-and-streams.md), [Compound Files](compound-files.md), [Structured Storage Fundamentals](structured-storage-fundamentals.md), and [Structured Storage Samples](using-structured-storage.md).</span></span>

 

 





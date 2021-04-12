---
title: Archiviazione strutturata
description: L'archiviazione strutturata fornisce la persistenza di file e dati in COM gestendo un singolo file come una raccolta strutturata di oggetti noti come flussi e archivi.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Archiviazione strutturata Strctd STG
- Archivio strutturato Strctd STG, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338238"
---
# <a name="structured-storage"></a><span data-ttu-id="7f107-105">Archiviazione strutturata</span><span class="sxs-lookup"><span data-stu-id="7f107-105">Structured Storage</span></span>

## <a name="purpose"></a><span data-ttu-id="7f107-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="7f107-106">Purpose</span></span>

<span data-ttu-id="7f107-107">L'archiviazione strutturata fornisce la persistenza di file e dati in COM gestendo un singolo file come una raccolta strutturata di oggetti noti come flussi e archivi.</span><span class="sxs-lookup"><span data-stu-id="7f107-107">Structured Storage provides file and data persistence in COM by handling a single file as a structured collection of objects known as storages and streams.</span></span>

<span data-ttu-id="7f107-108">Lo scopo dell'archiviazione strutturata consiste nel ridurre le sanzioni e il sovraccarico delle prestazioni associati all'archiviazione di oggetti distinti in un singolo file.</span><span class="sxs-lookup"><span data-stu-id="7f107-108">The purpose of Structured Storage is to reduce the performance penalties and overhead associated with storing separate objects in a single file.</span></span> <span data-ttu-id="7f107-109">L'archiviazione strutturata fornisce una soluzione definendo la modalità di gestione di una singola entità file come raccolta strutturata di due tipi di oggetti archiviazione e flussi tramite un'implementazione standard denominata file composti.</span><span class="sxs-lookup"><span data-stu-id="7f107-109">Structured Storage provides a solution by defining how to handle a single file entity as a structured collection of two types of objects storages and streams through a standard implementation called Compound Files.</span></span> <span data-ttu-id="7f107-110">Ciò consente all'utente di interagire con e gestire un file composto come se si trattasse di un singolo file piuttosto che di una gerarchia nidificata di oggetti separati.</span><span class="sxs-lookup"><span data-stu-id="7f107-110">This enables the user to interact with, and manage, a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7f107-111">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="7f107-111">Where applicable</span></span>

<span data-ttu-id="7f107-112">L'archiviazione strutturata può essere usata nei sistemi operativi Microsoft basati su COM.</span><span class="sxs-lookup"><span data-stu-id="7f107-112">Structured Storage can be used on Microsoft COM-based operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7f107-113">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="7f107-113">Developer audience</span></span>

<span data-ttu-id="7f107-114">La documentazione di archiviazione strutturata è destinata a programmatori C e C++ esperti e a sviluppatori di sistemi basati su COM.</span><span class="sxs-lookup"><span data-stu-id="7f107-114">The Structured Storage documentation is intended for experienced C and C++ programmers and COM-based system developers.</span></span>

<span data-ttu-id="7f107-115">L'archiviazione strutturata supporta principalmente i linguaggi di programmazione C e C++, tuttavia qualsiasi tecnologia basata su COM supporterà anche qualsiasi linguaggio di programmazione che utilizza i puntatori di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7f107-115">Structured Storage primarily supports C and C++ programming languages, however any COM-based technology will also support any programming language that utilizes interface pointers.</span></span>

<span data-ttu-id="7f107-116">Una conoscenza approfondita delle tecnologie COM è un prerequisito per l'utilizzo dello sviluppo di un archivio strutturato.</span><span class="sxs-lookup"><span data-stu-id="7f107-116">A solid understanding of COM technologies is prerequisite to the developmental use of Structured Storage.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7f107-117">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="7f107-117">Run-time requirements</span></span>

<span data-ttu-id="7f107-118">Per ulteriori informazioni sui sistemi operativi necessari per utilizzare un particolare elemento API, vedere la sezione requisiti della documentazione relativa all'elemento.</span><span class="sxs-lookup"><span data-stu-id="7f107-118">For more information about which operating systems are required to use a particular API element, see the Requirements section of the documentation for the element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7f107-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7f107-119">In this section</span></span>



| <span data-ttu-id="7f107-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="7f107-120">Topic</span></span>                                                               | <span data-ttu-id="7f107-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f107-121">Description</span></span>                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f107-122">Overview</span><span class="sxs-lookup"><span data-stu-id="7f107-122">Overview</span></span>](about-structured-storage.md)<br/>                 | <span data-ttu-id="7f107-123">Informazioni generali sull'archiviazione strutturata.</span><span class="sxs-lookup"><span data-stu-id="7f107-123">General information about Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="7f107-124">Uso dell'archiviazione strutturata</span><span class="sxs-lookup"><span data-stu-id="7f107-124">Using Structured Storage</span></span>](using-structured-storage.md)<br/> | <span data-ttu-id="7f107-125">Uso delle informazioni per l'archiviazione strutturata.</span><span class="sxs-lookup"><span data-stu-id="7f107-125">Using information for Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="7f107-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7f107-126">Reference</span></span>](structured-storage-reference.md)<br/>            | <span data-ttu-id="7f107-127">Documentazione di interfacce, funzioni, strutture ed enumerazioni specifiche dell'archiviazione strutturata.</span><span class="sxs-lookup"><span data-stu-id="7f107-127">Documentation of Structured Storage specific interfaces, functions, structures, and enumerations.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="7f107-128">Esempi</span><span class="sxs-lookup"><span data-stu-id="7f107-128">Samples</span></span>](samples.md)<br/>                                   | <span data-ttu-id="7f107-129">Esempi di codice scritti in C++.</span><span class="sxs-lookup"><span data-stu-id="7f107-129">Code examples written in C++.</span></span> <span data-ttu-id="7f107-130">Per ulteriori informazioni, vedere [nomi in IStorage](names-in-istorage.md), [intestazione set di proprietà](property-set-header.md), [sezione](section.md), archiviazione di [set di proprietà](storing-property-sets.md)e [utilizzo di archiviazione strutturata](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="7f107-130">For more information, see [Names in IStorage](names-in-istorage.md), [Property Set Header](property-set-header.md), [Section](section.md), [Storing Property Sets](storing-property-sets.md), and [Using Structured Storage](using-structured-storage.md).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7f107-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f107-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f107-132">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="7f107-132">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> </dl>

 


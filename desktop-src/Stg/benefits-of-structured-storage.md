---
title: Vantaggi dell'archiviazione strutturata
description: COM fornisce un set di servizi chiamati collettivamente archiviazione strutturata.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Archiviazione strutturata Strctd STG, vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708209"
---
# <a name="benefits-of-structured-storage"></a><span data-ttu-id="0b77c-104">Vantaggi dell'archiviazione strutturata</span><span class="sxs-lookup"><span data-stu-id="0b77c-104">Benefits of Structured Storage</span></span>

<span data-ttu-id="0b77c-105">COM fornisce un set di servizi chiamati collettivamente archiviazione strutturata.</span><span class="sxs-lookup"><span data-stu-id="0b77c-105">COM provides a set of services collectively called structured storage.</span></span> <span data-ttu-id="0b77c-106">Tra i vantaggi di questi servizi è la riduzione del sovraccarico delle prestazioni e del sovraccarico associato all'archiviazione di oggetti separati in un file flat.</span><span class="sxs-lookup"><span data-stu-id="0b77c-106">Among the benefits of these services is the reduction of performance penalties and overhead associated with storing separate objects in a flat file.</span></span> <span data-ttu-id="0b77c-107">Invece di un file flat, COM archivia gli oggetti distinti in un singolo file strutturato costituito da due elementi principali: oggetti di archiviazione e oggetti flusso.</span><span class="sxs-lookup"><span data-stu-id="0b77c-107">Instead of a flat file, COM stores the separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="0b77c-108">Insieme, funzionano come un file system all'interno di un file.</span><span class="sxs-lookup"><span data-stu-id="0b77c-108">Together, they function like a file system within a file.</span></span>

<span data-ttu-id="0b77c-109">L'archiviazione strutturata risolve i problemi di prestazioni eliminando la necessità di riscrivere completamente un file nell'archivio ogni volta che un nuovo oggetto viene aggiunto a un file composto o un oggetto esistente aumenta di dimensione.</span><span class="sxs-lookup"><span data-stu-id="0b77c-109">Structured storage solves performance problems by eliminating the need to totally rewrite a file to storage whenever a new object is added to a compound file, or an existing object increases in size.</span></span> <span data-ttu-id="0b77c-110">I nuovi dati vengono scritti nel successivo percorso disponibile nell'archivio permanente e l'oggetto di archiviazione aggiorna la tabella dei puntatori che gestisce per tenere traccia dei percorsi degli oggetti di archiviazione e degli oggetti flusso.</span><span class="sxs-lookup"><span data-stu-id="0b77c-110">The new data is written to the next available location in permanent storage, and the storage object updates the table of pointers it maintains to track the locations of its storage objects and stream objects.</span></span> <span data-ttu-id="0b77c-111">Allo stesso tempo, l'archiviazione strutturata consente agli utenti finali di interagire e gestire un file composto come se si trattasse di un singolo file anziché di una gerarchia nidificata di oggetti separati.</span><span class="sxs-lookup"><span data-stu-id="0b77c-111">At the same time, structured storage enables end users to interact and manage a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

<span data-ttu-id="0b77c-112">L'archiviazione strutturata offre anche altri vantaggi:</span><span class="sxs-lookup"><span data-stu-id="0b77c-112">Structured storage also has other benefits:</span></span>

-   <span data-ttu-id="0b77c-113">**Accesso incrementale**.</span><span class="sxs-lookup"><span data-stu-id="0b77c-113">**Incremental access**.</span></span> <span data-ttu-id="0b77c-114">Se un utente deve accedere a un oggetto all'interno di un file composto, l'utente può caricare e salvare solo tale oggetto, anziché l'intero file.</span><span class="sxs-lookup"><span data-stu-id="0b77c-114">If a user needs access to an object within a compound file, the user can load and save only that object, rather than the entire file.</span></span>
-   <span data-ttu-id="0b77c-115">**Uso multiplo**.</span><span class="sxs-lookup"><span data-stu-id="0b77c-115">**Multiple use**.</span></span> <span data-ttu-id="0b77c-116">Più di un utente finale o un'applicazione può leggere e scrivere contemporaneamente le informazioni nello stesso file composto.</span><span class="sxs-lookup"><span data-stu-id="0b77c-116">More than one end user or application can concurrently read and write information in the same compound file.</span></span>
-   <span data-ttu-id="0b77c-117">**Elaborazione delle transazioni**.</span><span class="sxs-lookup"><span data-stu-id="0b77c-117">**Transaction processing**.</span></span> <span data-ttu-id="0b77c-118">Gli utenti possono leggere o scrivere in file composti COM in modalità transazionale, in cui le modifiche apportate al file vengono memorizzate nel buffer e possono essere successivamente sottoposte a commit nel file o invertite.</span><span class="sxs-lookup"><span data-stu-id="0b77c-118">Users can read or write to COM compound files in transacted mode, where changes made to the file are buffered and can subsequently either be committed to the file or reversed.</span></span>
-   <span data-ttu-id="0b77c-119">**Salvataggi a memoria insufficiente**.</span><span class="sxs-lookup"><span data-stu-id="0b77c-119">**Low-memory saves**.</span></span> <span data-ttu-id="0b77c-120">L'archiviazione strutturata fornisce funzionalità per il salvataggio di file in situazioni di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0b77c-120">Structured storage provides facilities for saving files in low-memory situations.</span></span>

 

 





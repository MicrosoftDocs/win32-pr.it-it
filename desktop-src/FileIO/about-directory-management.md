---
description: Una directory che contiene una o più directory è l'elemento padre della directory o directory contenuta e ogni directory indipendente è un elemento figlio della directory padre. La struttura gerarchica delle directory viene definita albero di directory.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Informazioni sulla gestione delle directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879302"
---
# <a name="about-directory-management"></a><span data-ttu-id="df512-104">Informazioni sulla gestione delle directory</span><span class="sxs-lookup"><span data-stu-id="df512-104">About Directory Management</span></span>

<span data-ttu-id="df512-105">Una directory che contiene una o più directory è l' *elemento padre* della directory o directory contenuta e ogni directory indipendente è un elemento *figlio* della directory padre.</span><span class="sxs-lookup"><span data-stu-id="df512-105">A directory that contains one or more directories is the *parent* of the contained directory or directories, and each contained directory is a *child* of the parent directory.</span></span> <span data-ttu-id="df512-106">La struttura gerarchica delle directory viene definita *albero di directory*.</span><span class="sxs-lookup"><span data-stu-id="df512-106">The hierarchical structure of directories is referred to as a *directory tree*.</span></span>

<span data-ttu-id="df512-107">Il file system NTFS implementa il collegamento logico tra una directory e i file in esso contenuti come *tabella voce di directory*.</span><span class="sxs-lookup"><span data-stu-id="df512-107">The NTFS file system implements the logical link between a directory and the files it contains as a *directory entry table*.</span></span> <span data-ttu-id="df512-108">Quando un file viene spostato in una directory, viene creata una voce nella tabella per il file spostato e il nome del file viene inserito nella voce.</span><span class="sxs-lookup"><span data-stu-id="df512-108">When a file is moved into a directory, an entry is created in the table for the moved file and the name of the file is placed in the entry.</span></span> <span data-ttu-id="df512-109">Quando un file contenuto in una directory viene eliminato, anche il nome e la voce corrispondenti al file eliminato vengono eliminati dalla tabella.</span><span class="sxs-lookup"><span data-stu-id="df512-109">When a file contained in a directory is deleted, the name and entry corresponding to the deleted file is also deleted from the table.</span></span> <span data-ttu-id="df512-110">In una tabella di voci di directory possono esistere più voci per un singolo file.</span><span class="sxs-lookup"><span data-stu-id="df512-110">More than one entry for a single file can exist in a directory entry table.</span></span> <span data-ttu-id="df512-111">Se nella tabella viene creata una voce aggiuntiva per un file, tale voce viene definita *collegamento* reale a tale file.</span><span class="sxs-lookup"><span data-stu-id="df512-111">If an additional entry is created in the table for a file, that entry is referred to as a *hard link* to that file.</span></span> <span data-ttu-id="df512-112">Non esiste alcun limite al numero di collegamenti reali che è possibile creare per un singolo file.</span><span class="sxs-lookup"><span data-stu-id="df512-112">There is no limit to the number of hard links that can be created for a single file.</span></span>

<span data-ttu-id="df512-113">Le directory possono inoltre contenere giunzioni e reparse point.</span><span class="sxs-lookup"><span data-stu-id="df512-113">Directories can also contain junctions and reparse points.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="df512-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="df512-114">In this section</span></span>



| <span data-ttu-id="df512-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="df512-115">Topic</span></span>                                                                                 | <span data-ttu-id="df512-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df512-116">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df512-117">Creazione ed eliminazione di directory</span><span class="sxs-lookup"><span data-stu-id="df512-117">Creating and Deleting Directories</span></span>](creating-and-deleting-directories.md)<br/> | <span data-ttu-id="df512-118">Un'applicazione può creare ed eliminare le directory a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="df512-118">An application can programmatically create and delete directories.</span></span><br/>                          |
| [<span data-ttu-id="df512-119">Handle di directory</span><span class="sxs-lookup"><span data-stu-id="df512-119">Directory Handles</span></span>](obtaining-a-handle-to-a-directory.md)<br/>                 | <span data-ttu-id="df512-120">Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df512-120">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span><br/> |
| [<span data-ttu-id="df512-121">Punti di analisi</span><span class="sxs-lookup"><span data-stu-id="df512-121">Reparse Points</span></span>](reparse-points.md)<br/>                                       | <span data-ttu-id="df512-122">Descrive i reparse point.</span><span class="sxs-lookup"><span data-stu-id="df512-122">Describes reparse points.</span></span><br/>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="df512-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df512-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df512-124">Guida di riferimento alla gestione delle directory</span><span class="sxs-lookup"><span data-stu-id="df512-124">Directory Management Reference</span></span>](directory-management-reference.md)
</dt> </dl>

 

 




